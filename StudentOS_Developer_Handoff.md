# StudentOS — Developer Handoff Quick Reference

Use `StudentOS_Master_Wireframe_Spec.md` as the product/UX source of truth. Use `StudentOS_Clickable_Wireframe.html` as the executable mid-fidelity reference for screen composition, state transitions, responsive behavior, and critical flows. Internal screen IDs below are design-traceability IDs; production Flutter routing should remain semantic rather than copying numeric design IDs.

## Implemented Prototype Contract

- **82 / 82 required named screens/states are purpose-built.** No required screen uses the former generic requirements renderer.
- Shells are deliberately separated into **Authentication**, **Onboarding**, and **Authenticated Application** structures.
- The prototype is self-contained and uses JavaScript/in-memory mock data (plus limited `localStorage`) only for UX validation. It does not require production authentication, Supabase, AI, PDF parsing, or notification services.
- Desktop application navigation is Dashboard, Planner, Courses, Attendance, GPA / CGPA, Focus, AI Study, Analytics, Notifications, with Settings, Help, and User Profile below.
- Mobile navigation is Home, Planner, Courses, AI Study, More. More contains Attendance, GPA / CGPA, Focus, Analytics, Notifications, Settings, Help, and Sign Out.
- Major state transitions are visible in the UI rather than toast-only: assignment completion, attendance/grade saves, focus pause/resume, quiz selection/scoring, flashcard flip/rating, notification read state, Exam Pack revision/study-plan progress, deletion, document processing, and AI-generation stages.
- Edit-form cancellation uses an unsaved-changes confirmation. Destructive actions use confirmation patterns. Recoverable offline save failures preserve the current form and expose Retry/Back UI.
- All overlays are keyboard-dismissable, receive an accessible name, trap focus while open, and restore focus after close.

## Semantic Flutter Route / State Map

The rows marked “confirmation state” or “empty state” do not have to become separate production URLs; they may be modal/state variants owned by the semantic parent route.

| Design ID | Screen / State | Suggested semantic Flutter route/state |
|---|---|---|
| `AUTH-01` | Login | `/login` |
| `AUTH-02` | Sign Up | `/signup` |
| `AUTH-03` | Email Verification | `/verify-email` |
| `AUTH-04` | Forgot Password | `/forgot-password` |
| `AUTH-05` | Reset Password | `/reset-password` |
| `AUTH-06` | Authentication Error | `/auth/error` |
| `ONB-01` | Welcome | `/onboarding` |
| `ONB-02` | Profile | `/onboarding/profile` |
| `ONB-03` | Academic Setup | `/onboarding/academic` |
| `ONB-04` | Semester | `/onboarding/semester` |
| `ONB-05` | Courses | `/onboarding/courses` |
| `ONB-06` | Preferences | `/onboarding/preferences` |
| `ONB-07` | Finish | `/onboarding/finish` |
| `DASH-01` | Dashboard | `/dashboard` |
| `SEM-01` | Semester List | `/semesters` |
| `SEM-02` | Create Semester | `/semesters/new` |
| `SEM-03` | Edit Semester | `/semesters/:semesterId/edit` |
| `SEM-04` | Delete Semester | `/semesters/:semesterId (delete confirmation state)` |
| `COURSE-01` | Courses | `/courses` |
| `COURSE-02` | Add Course | `/courses/new` |
| `COURSE-03` | Edit Course | `/courses/:courseId/edit` |
| `COURSE-04` | Course Detail | `/courses/:courseId` |
| `ATT-01` | Attendance Overview | `/attendance` |
| `ATT-02` | Course Attendance | `/courses/:courseId/attendance` |
| `ATT-03` | Add Attendance | `/courses/:courseId/attendance/new` |
| `ATT-04` | Edit Attendance | `/courses/:courseId/attendance/:recordId/edit` |
| `ATT-05` | Delete Record | `/courses/:courseId/attendance/:recordId (delete confirmation state)` |
| `GPA-01` | GPA Dashboard | `/gpa` |
| `GPA-02` | Add / Edit Grade | `/gpa/grades/:courseId/edit` |
| `GPA-03` | GPA History | `/gpa/history` |
| `PLAN-01` | Planner | `/planner` |
| `ASSIGN-01` | List | `/assignments` |
| `ASSIGN-02` | Add Assignment | `/assignments/new` |
| `ASSIGN-03` | Detail | `/assignments/:assignmentId` |
| `ASSIGN-04` | Edit | `/assignments/:assignmentId/edit` |
| `ASSIGN-05` | Delete | `/assignments/:assignmentId (delete confirmation state)` |
| `EXAM-01` | Exam List | `/exams` |
| `EXAM-02` | Add Exam | `/exams/new` |
| `EXAM-03` | Exam Detail | `/exams/:examId` |
| `EXAM-04` | Edit Exam | `/exams/:examId/edit` |
| `EXAM-05` | Delete Exam | `/exams/:examId (delete confirmation state)` |
| `FOCUS-01` | Focus Home | `/focus` |
| `FOCUS-02` | Active | `/focus/session` |
| `FOCUS-03` | Complete | `/focus/session/complete` |
| `FOCUS-04` | History | `/focus/history` |
| `AI-01` | AI Study Home | `/ai-study` |
| `DOC-01` | Upload | `/documents/upload` |
| `DOC-02` | Uploading | `/documents/:documentId/uploading` |
| `DOC-03` | Processing | `/documents/:documentId/processing` |
| `DOC-04` | Failed | `/documents/:documentId/error` |
| `DOC-05` | Scanned PDF Unsupported | `/documents/:documentId/unsupported` |
| `DOC-06` | Document Detail | `/documents/:documentId` |
| `SUM-01` | Summary Generator | `/documents/:documentId/summary/new` |
| `SUM-02` | Summary Result | `/summaries/:summaryId` |
| `MCQ-01` | Generator | `/documents/:documentId/mcqs/new` |
| `MCQ-02` | Generated Set | `/mcq-sets/:setId` |
| `QUIZ-01` | Quiz | `/quizzes/:setId` |
| `QUIZ-02` | Submit Confirmation | `/quizzes/:setId/submit` |
| `QUIZ-03` | Results | `/quizzes/:attemptId/results` |
| `QUIZ-04` | Review | `/quizzes/:attemptId/review` |
| `FLASH-01` | Generator | `/documents/:documentId/flashcards/new` |
| `FLASH-02` | Deck | `/flashcards/:deckId` |
| `FLASH-03` | Study | `/flashcards/:deckId/study` |
| `FLASH-04` | Complete | `/flashcards/:deckId/complete` |
| `PREP-01` | Start | `/exam-prep` |
| `PREP-02` | Materials | `/exam-prep/:examId/materials` |
| `PREP-03` | Preferences | `/exam-prep/:examId/preferences` |
| `PREP-04` | AI Credit Confirmation | `/exam-prep/:examId/confirm` |
| `PREP-05` | Generating | `/exam-prep/:examId/generating` |
| `PREP-06` | Exam Pack | `/exam-prep/:examId/pack` |
| `ANA-01` | Analytics | `/analytics` |
| `ANA-02` | Study Detail | `/analytics/study` |
| `NOTIF-01` | Notifications | `/notifications` |
| `NOTIF-02` | Empty | `/notifications (empty state)` |
| `SET-01` | Profile | `/settings/profile` |
| `SET-02` | Academic | `/settings/academic` |
| `SET-03` | Notifications | `/settings/notifications` |
| `SET-04` | AI Usage | `/settings/ai-usage` |
| `SET-05` | Privacy & Data | `/settings/privacy` |
| `SET-06` | Security | `/settings/security` |
| `SET-07` | Account | `/settings/account` |
| `SET-08` | Delete Account | `/settings/account/delete` |

## Core Data Entities

- `UserProfile`
- `AcademicPreferences`
- `Semester`
- `Course`
- `AttendanceRecord`
- `GradeRecord`
- `Assignment`
- `Exam`
- `FocusSession`
- `StudyDocument`
- `SummaryResult`
- `MCQSet`, `MCQQuestion`, `QuizAttempt`
- `FlashcardDeck`, `Flashcard`, `FlashcardSession`
- `ExamPack`, `ExamPackTopic`, `ExamPackStudyTask`
- `Notification`
- `AIUsageEvent`

## Deterministic Product Logic

```text
attendance% = attended / held * 100
where held excludes cancelled classes

semester_gpa = Σ(grade_point * credit_hours) / Σ(credit_hours)
cgpa = Σ(all quality points) / Σ(all attempted credits)

overdue = now > due_at AND assignment.status != completed
quiz_score = correct_answers / total_questions * 100
```

AI may generate summaries, questions, flashcards, revision recommendations, and Exam Pack content. It must **not** calculate attendance %, GPA, CGPA, overdue state, or final quiz scores.

## Responsive Implementation Contract

- **Desktop 1440 / 1280:** full sidebar, top bar, cards, tables, and multi-column layouts.
- **Tablet 768:** compact/collapsed navigation and reduced grids while preserving all actions.
- **Mobile 390:** top app bar plus bottom navigation; single-column forms; large controls; tables that would become unreadable convert to cards; Planner favors agenda/list behavior; Quiz shows one question at a time; Flashcards use a large thumb-friendly card; Exam Pack preserves all eight sections through horizontally scrollable tabs.
- Minimum intended touch target is approximately **44px**.
- Mobile content must not be removed simply to fit the viewport.

## Exam Preparation / Exam Pack State Model

`Exam Detail → Select Exam → Select Materials → Preferences → AI Credit Confirmation → Generating → Exam Pack`

Generation uses stage progression rather than invented percentages. Exam Pack contains real switchable sections for Overview, Important Topics, Short Questions, Long Questions, MCQs, Flashcards, Viva, and Study Plan. `Mark Revised`, expandable answers, quiz links, flashcard links, study-task completion, revision progress, and credit-confirmed regeneration all mutate visible prototype state.

## Backend / Async Mapping Guidance

Prototype timers simulate backend-dependent operations. In Flutter, map them to repository/service states such as `idle → loading/uploading/processing → success` or `failure`. Preserve form values across recoverable failure. Do not expose service-role credentials, AI provider secrets, database credentials, or private system keys in the client. Uploaded documents are private and deletable. Baseline V1 explicitly does **not** support OCR for scanned/image-only PDFs.

## Validation Evidence for This Handoff

The completed HTML was browser-tested in headless Chromium after implementation:

- 82 / 82 required routes rendered without page errors.
- 82 / 82 required routes have explicit purpose-built renderers; generic required screens = 0.
- Master interaction registry: **195 interactions**; all 195 labels are represented in implementation source, and conditional/state-only controls were independently exercised.
- The 16 requested critical flows passed (18 executable assertions, including multi-stage upload/summary and complete exam-prep generation).
- Responsive audit: 19 critical screens × 4 widths (1440, 1280, 768, 390) with no document-level horizontal overflow.
- Accessibility screen audit: 82 / 82 screens passed the implemented form-label, control-name, and one-primary-heading checks; overlay keyboard focus management is implemented.
- Conditional-interaction audit passed pause/resume, Planner add menu, quiz submit state, flashcard rating/navigation, Exam Pack section actions, unsaved changes, dialog naming, and offline save failure/retry.

These are prototype-validation results, not a substitute for Flutter widget tests, integration tests, screen-reader testing on target operating systems, or production backend/security testing.
