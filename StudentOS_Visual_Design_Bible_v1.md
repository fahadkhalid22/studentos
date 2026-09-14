# StudentOS — Premium Visual Design Bible v1.0

**Status:** Visual direction locked  
**Scope:** Complete visual-design system for the existing StudentOS V1 product and its 82-screen prototype  
**Codename:** `StudentOS` remains temporary; this document must not be treated as a final brand identity  
**Goal:** Transform the functionally complete wireframe into a premium, distinctive academic productivity + AI workspace without changing product logic or scope.

---

# 1. Locked Visual Direction

StudentOS must feel:

**premium · intelligent · energetic · organized · modern · slightly futuristic · academically serious**

It must **not** feel like:

- a university ERP or student portal
- a generic admin dashboard
- a childish education app
- a neon gaming interface
- an over-glassmorphed concept shot
- a clone of Linear, Notion, Raycast, Stripe, or any one reference product
- a page made from endless identical white cards

The locked design decisions are:

| Area | Locked decision |
|---|---|
| Color personality | Indigo + Cyan + Coral |
| Typography | Sora + Inter |
| Iconography | Rounded Duotone |
| Cards / surfaces | Mixed Surfaces |
| Sidebar | Hybrid Premium Sidebar |
| Top bar / search | Command-first Premium |
| Dashboard | Hybrid Editorial + Bento |
| AI Study | Light workspace + premium AI layer |
| Buttons | Premium Hybrid |
| Forms | Premium Adaptive Fields |
| Charts | Premium Intelligent Analytics |
| Status / progress | Layered Status Language |
| Motion | Purposeful Premium Motion |
| Mobile | Adaptive Premium Mobile Dock |
| Illustrations | Selective Premium Illustrations |
| Density | Adaptive Balanced Density |

---

# 2. Core Design Principles

## 2.1 Calm first, expressive second

Normal academic work should remain calm and legible. Color, gradients, glass, and glow are reserved for hierarchy and special moments.

Use richer treatment for:

- AI Study
- Prepare Me for Exam
- Exam Pack
- Focus
- selected states
- progress milestones
- important warnings
- major success moments

Do not use premium effects everywhere. Scarcity is what makes them feel premium.

## 2.2 Information hierarchy before decoration

Every screen must clearly answer:

1. Where am I?
2. What matters most now?
3. What can I do next?
4. What needs my attention?
5. What is secondary?

Visual design must reinforce product priority, not compete with it.

## 2.3 Course identity is persistent

Every course receives one accent color. That color follows the course across:

- course cards
- planner events
- assignment tags
- exam tags
- document chips
- chart legends
- focus sessions
- small course monograms

This creates recognition without requiring users to reread labels repeatedly.

## 2.4 AI is special, but still StudentOS

AI features use stronger violet/cyan light effects and layered surfaces, but still inherit:

- typography
- spacing
- icon family
- radius language
- interaction rules
- accessibility rules

AI must not look like a separate product pasted into StudentOS.

## 2.5 Motion communicates state

Motion should explain:

- selection
- hierarchy
- loading
- progress
- completion
- navigation

Never animate simply because animation is available.

---

# 3. Color System

## 3.1 Core brand-neutral tokens

These are working visual-system colors. They can later be remapped when the final public brand is chosen.

| Token | Hex | Usage |
|---|---:|---|
| `canvas` | `#F7F8FC` | Main app background |
| `canvas-tinted` | `#F4F5FB` | Alternate page background |
| `surface` | `#FFFFFF` | Standard card/input/menu surface |
| `surface-soft` | `#F9FAFC` | Secondary card/table header |
| `surface-raised` | `#FFFFFF` | Modals, command palette, floating dock |
| `sidebar` | `#101322` | Premium dark sidebar |
| `sidebar-raised` | `#171B2E` | Active areas / profile block |
| `text-primary` | `#131722` | Main text |
| `text-secondary` | `#667085` | Secondary text |
| `text-tertiary` | `#98A2B3` | Helper / metadata |
| `text-on-dark` | `#F8FAFC` | Main text on sidebar |
| `text-on-dark-muted` | `#98A2B3` | Sidebar metadata |
| `border` | `#E4E7EC` | Default border |
| `border-strong` | `#D0D5DD` | Strong separation |
| `divider` | `#EAECF0` | Dividers |

## 3.2 Primary Indigo

| Token | Hex |
|---|---:|
| `indigo-50` | `#EEF0FF` |
| `indigo-100` | `#E1E5FF` |
| `indigo-200` | `#C8CEFF` |
| `indigo-300` | `#A5B0FF` |
| `indigo-400` | `#818CF8` |
| `indigo-500` | `#6366F1` |
| `indigo-600` | `#5658DD` |
| `indigo-700` | `#4749BF` |
| `indigo-800` | `#393B99` |
| `indigo-900` | `#2D307B` |

Primary action = `#6366F1`  
Primary hover = `#5658DD`  
Primary pressed = `#4749BF`  
Soft primary surface = `#EEF0FF`

## 3.3 Supporting accents

| Purpose | Main | Soft surface | Strong |
|---|---:|---:|---:|
| Cyan / intelligence | `#22C7E8` | `#E8FAFE` | `#0D9FC0` |
| Violet / AI | `#8B5CF6` | `#F2ECFF` | `#7141DC` |
| Coral / attention | `#F05D6B` | `#FFF0F2` | `#D94654` |
| Emerald / success | `#16B57A` | `#ECFBF4` | `#0E8A5C` |
| Amber / warning | `#F4A62A` | `#FFF7E6` | `#C97D0B` |
| Blue / information | `#3B82F6` | `#EFF6FF` | `#2563EB` |

## 3.4 AI gradients

### AI Primary
`linear-gradient(135deg, #6366F1 0%, #8B5CF6 52%, #22C7E8 100%)`

### AI Soft Surface
`linear-gradient(135deg, rgba(99,102,241,.10), rgba(139,92,246,.08) 48%, rgba(34,199,232,.10))`

### AI Glow
Use 2–3 blurred radial gradients at **6–14% opacity**, never a hard neon glow.

Example:
- Indigo glow: `rgba(99,102,241,.16)`
- Violet glow: `rgba(139,92,246,.13)`
- Cyan glow: `rgba(34,199,232,.12)`

### Focus Dark Gradient
`linear-gradient(145deg, #101322 0%, #171B2E 55%, #1D2440 100%)`

## 3.5 Course color palette

Assign colors automatically, then persist the assignment.

| Course slot | Accent | Soft |
|---|---|---|
| Course 1 | `#6366F1` | `#EEF0FF` |
| Course 2 | `#22C7E8` | `#E8FAFE` |
| Course 3 | `#8B5CF6` | `#F2ECFF` |
| Course 4 | `#16B57A` | `#ECFBF4` |
| Course 5 | `#F4A62A` | `#FFF7E6` |
| Course 6 | `#F05D6B` | `#FFF0F2` |
| Course 7 | `#3B82F6` | `#EFF6FF` |
| Course 8 | `#14B8A6` | `#EDFCFA` |

Course color must not be the only way to identify a course.

---

# 4. Typography

## 4.1 Typeface roles

**Sora**
- hero copy
- page titles
- major section headings
- KPI numbers
- exam readiness
- AI hero headings

**Inter**
- body copy
- navigation
- buttons
- inputs
- table content
- helper text
- metadata
- status labels

## 4.2 Type scale

| Token | Font | Weight | Size / Line height | Usage |
|---|---|---:|---:|---|
| `display-lg` | Sora | 700 | 40 / 48 | Rare hero moments |
| `display-md` | Sora | 700 | 34 / 42 | AI / Exam Pack hero |
| `h1` | Sora | 700 | 30 / 38 | Page title |
| `h2` | Sora | 600 | 24 / 32 | Major section |
| `h3` | Sora | 600 | 20 / 28 | Feature card heading |
| `kpi-lg` | Sora | 700 | 34 / 40 | Primary KPI |
| `kpi-md` | Sora | 700 | 28 / 34 | Standard KPI |
| `body-lg` | Inter | 400 | 17 / 26 | Intro copy |
| `body` | Inter | 400 | 15 / 23 | Default body |
| `body-sm` | Inter | 400 | 14 / 21 | Compact content |
| `label` | Inter | 500 | 14 / 20 | Forms |
| `button` | Inter | 600 | 14 / 20 | Buttons |
| `nav` | Inter | 500 | 14 / 20 | Navigation |
| `caption` | Inter | 400 | 12 / 18 | Metadata |
| `eyebrow` | Inter | 600 | 11 / 16 | Section labels; letter spacing +0.08em |

Do not use more than 3 weights on a single screen unless truly necessary.

---

# 5. Spacing, Radius, Border and Shadow

## 5.1 Spacing scale

`4, 8, 12, 16, 20, 24, 32, 40, 48, 64`

Use:
- 4 = micro alignment
- 8 = icon/text
- 12 = compact internal
- 16 = standard component gap
- 20 = standard card inner gap
- 24 = card padding / section spacing
- 32 = major content separation
- 40/48 = hero sections
- 64 = rare page-level separation

## 5.2 Radius

| Token | Value | Usage |
|---|---:|---|
| `r-sm` | 10px | tags, compact controls |
| `r-md` | 12px | inputs |
| `r-lg` | 16px | standard cards/buttons |
| `r-xl` | 20px | hero cards, command palette |
| `r-2xl` | 24px | AI / focus / premium panels |
| `r-pill` | 999px | badges, chips, dock active item |

## 5.3 Borders

Default: `1px solid #E4E7EC`  
Strong: `1px solid #D0D5DD`  
Selected: `1px solid rgba(99,102,241,.55)`  
AI: `1px solid rgba(99,102,241,.20)`

## 5.4 Shadows

### Card
`0 1px 2px rgba(16,24,40,.04), 0 8px 24px rgba(16,24,40,.04)`

### Hover card
`0 4px 10px rgba(16,24,40,.05), 0 14px 34px rgba(16,24,40,.08)`

### Floating
`0 18px 50px rgba(16,24,40,.14)`

### AI glow shadow
`0 18px 50px rgba(99,102,241,.12)`

Avoid heavy dark drop shadows.

---

# 6. Iconography System

Primary family: **Rounded Duotone**.

Design intent: premium, expressive, friendly without looking childish.

Implementation rule:
- Use one icon family consistently.
- If a chosen icon is unavailable, use the closest semantic icon from the same family.
- Never mix filled Material icons, emoji, Unicode diamonds, and duotone icons on the same UI.

Recommended sizes:
- sidebar: 20px
- top bar: 20px
- button: 18px
- table utility: 16–18px
- KPI: 22–24px
- feature tile: 26–28px
- empty state: 48–64px
- onboarding illustration anchor: 64–80px where an icon is used

Container sizes:
- compact: 32px
- standard: 40px
- KPI: 44px
- feature: 48px

Duotone secondary layer opacity target: **20–35%**.

### Core navigation icon registry

| Element | Semantic icon |
|---|---|
| Dashboard | dashboard-square-01 |
| Planner | calendar-03 / calendar |
| Courses | book-open / books-01 |
| Attendance | calendar-check / user-check |
| GPA / CGPA | graduation-cap / chart-up |
| Focus | timer-01 / target-01 |
| AI Study | sparkle / artificial-intelligence |
| Analytics | chart-up / analytics-01 |
| Notifications | notification-02 / bell |
| Settings | settings-02 |
| Help | help-circle |
| User Profile | user-circle |
| Collapse Sidebar | panel-left-close |
| Expand Sidebar | panel-left-open |
| Sign Out | logout-01 |

### Global utility icons

| Action | Icon |
|---|---|
| Search | search-01 |
| Command shortcut | command |
| Add | plus-sign |
| Upload | upload-04 / cloud-upload |
| Download | download-04 |
| Edit | pencil-edit-02 |
| Delete | delete-02 / trash |
| More | more-vertical-circle-01 |
| Back | arrow-left-02 |
| Forward | arrow-right-02 |
| Expand | arrow-down-01 |
| Breadcrumb | arrow-right-01 |
| Close | cancel-01 |
| Filter | filter |
| Sort | sorting-04 |
| Refresh / Retry | reload |
| Copy | copy-01 |
| External/Open | arrow-up-right-01 |
| Eye | view |
| Eye Off | view-off |
| Lock | lock |
| Key | key-01 |
| Mail | mail-01 |
| User Add | user-add-01 |
| Check | tick-02 |
| Check Circle | checkmark-circle-02 |
| Error | cancel-circle |
| Warning | alert-02 |
| Info | information-circle |

The complete icon inventory is provided in the companion `StudentOS_Icon_Registry.csv`.

---

# 7. App Shell

## 7.1 Hybrid premium sidebar

Desktop width: **252px**  
Collapsed width: **76px**  
Outer page gap: **12px** on 1280+, optional 0 on narrower desktop.

Background: `#101322`  
Internal selected surface: `rgba(99,102,241,.14)`  
Selected text: `#FFFFFF`  
Default text: `#AAB1C2`  
Default icon: `#8F98AD`  
Selected icon: `#A5B0FF`

Navigation item:
- height 46px
- radius 12px
- horizontal padding 12px
- icon 20px
- icon/text gap 11px

Selected state:
- soft indigo capsule
- stronger duotone icon
- optional 3px indigo accent rail
- no giant glow

Hover:
- background `rgba(255,255,255,.045)`
- text shifts toward white
- 180ms

Bottom area:
- Settings
- Help
- compact user profile card
- avatar 36px
- profile chevron

Section labels:
- Inter 600 10–11px
- uppercase
- letter spacing .10em
- muted

## 7.2 Top bar

Height: **72px**  
Canvas integration: top bar may be transparent over page canvas with sticky behavior and subtle backdrop blur only during scroll.

Left:
- breadcrumb when needed
- page title may live in page header rather than inside the bar

Center/right:
- command search
- Quick Add
- notification
- avatar

## 7.3 Command-first search

Desktop width: 360–420px  
Height: 44–46px  
Radius: 14px  
Background: `#FFFFFF`  
Border: `#E4E7EC`

Content:
- 18px search icon
- placeholder
- `Ctrl K` keycap
- optional recent indicator

Focus:
- border `#818CF8`
- 3px soft focus halo `rgba(99,102,241,.10)`

Command palette:
- width 620–700px desktop
- max height 68vh
- radius 20px
- floating shadow
- groups: Quick Actions, Recent, Courses, Assignments, Exams, Documents, AI Study
- item height 48–52px
- left icon 20px
- right metadata / shortcut
- keyboard navigation
- empty state with `search-x`

---

# 8. Buttons

## 8.1 Primary

- height 44px standard, 48px hero
- radius 14px
- fill `#6366F1`
- hover `#5658DD`
- pressed `#4749BF`
- white text
- icon 18px
- gap 8px
- Inter 600 / 14

## 8.2 Secondary

White or soft-tinted surface, neutral border, dark text.

## 8.3 AI Primary

Use only for key AI actions:
- Prepare Me for Exam
- Generate Exam Pack
- Generate Summary where the AI context is dominant

Preferred:
- gradient border or gradient fill
- no more than one dominant gradient button per screen

## 8.4 Danger

Soft coral by default:
- background `#FFF0F2`
- text `#D94654`
- border `rgba(240,93,107,.26)`

Final destructive confirmation can use stronger coral fill.

## 8.5 Icon buttons

40–44px rounded square or circle.  
Tooltip required when meaning is not obvious.

## 8.6 Button motion

Hover: translateY(-1px)  
Press: scale(.98)  
Duration: 140–180ms  
Disabled: no motion

---

# 9. Forms and Inputs

Control height: **50px**  
Radius: **13px**  
Padding: **0 14–16px**  
Label: Inter 500 / 14  
Helper: Inter 400 / 12–13

Default:
- background `#FFFFFF`
- border `#E4E7EC`

Hover:
- border `#D0D5DD`

Focus:
- border `#818CF8`
- ring `0 0 0 3px rgba(99,102,241,.10)`

Error:
- border coral
- error icon
- helper message
- never use color alone

Leading icons only when useful:
- email
- password
- date/time
- search
- course selection
- upload
- location

Do not add an icon to every text field.

Large forms use 2 columns only where fields are naturally paired. Mobile is always single-column.

---

# 10. Cards and Surfaces

## 10.1 Standard card

- surface white
- radius 16px
- border
- 20–24px padding
- card shadow

## 10.2 KPI card

- optional very soft tint
- 44px icon container
- Sora KPI number
- short trend row
- optional micro-sparkline

## 10.3 Interactive card

Hover:
- translateY(-2px)
- stronger shadow
- border shifts slightly toward accent

## 10.4 AI card

- soft AI gradient surface
- subtle gradient border
- 20–24px radius
- controlled glow
- optional abstract node/spark texture at ≤ 8% opacity

## 10.5 Focus card

Dark premium surface:
- midnight gradient
- white text
- soft indigo ring
- cyan/violet accents

## 10.6 Warning card

Use soft amber/coral surface, not a saturated block.

---

# 11. Status, Priority, Progress and Dots

## 11.1 Academic status

| State | Icon | Surface | Text |
|---|---|---|---|
| Safe | shield-check | emerald soft | emerald strong |
| Warning | alert-02 | amber soft | amber strong |
| At Risk | shield-alert | coral soft | coral strong |

Badge height: 28px  
Icon: 14–16px  
Radius: pill

## 11.2 Task status

Completed → check-circle + emerald  
Due Soon → clock + amber  
Overdue → alarm-clock + coral  
Upcoming → calendar + indigo soft

## 11.3 Priority

Use a **dot + label**, not a giant badge.

- High: 8px coral dot
- Medium: 8px amber dot
- Low: 8px cool-blue dot

## 11.4 Notification dot

- diameter: **7px**
- fill: coral or indigo based on context
- ring: 2px matching surrounding surface
- never pulse continuously

## 11.5 Chart legend dot

- diameter: 8px
- aligned optically to label baseline
- same course/series color used in chart

## 11.6 Progress language

Attendance → circular progress  
Exam readiness → premium radial ring  
Assignments → segmented/horizontal completion  
AI generation → multi-stage process  
Course progress → slim bar  
Onboarding → connected stepper  
Study streak → flame + count

---

# 12. Tables and Dense Data

Desktop table:
- header height 44px
- row height 56px standard
- dense option 52px for attendance/history
- horizontal padding 14px
- header surface `#F9FAFC`
- row hover `#FAFBFF`
- selected row `#F3F4FF`
- right-side actions use icon buttons

Headers:
- Inter 600 / 12–13
- muted text
- sort indicator only on sortable columns

Mobile:
- convert unreadable tables to purpose-built cards
- never squeeze 7–10 columns into 390px

---

# 13. Charts and Analytics

## 13.1 Visual rules

- no 3D charts
- minimal grid lines
- no chart junk
- rounded bar caps
- 2–3px line strokes
- hover/focus tooltips
- subtle animated entrance
- course colors persist

## 13.2 Mapping

GPA Trend → smooth line + subtle indigo area  
Study Time → rounded bars  
Attendance → rings + horizontal course comparison  
Assignment Completion → segmented progress / donut  
Exam Readiness → large radial  
Focus History → heatmap / activity strip  
Course Comparison → horizontal bars  
Dashboard KPIs → sparklines

## 13.3 Tooltip

- white raised card
- radius 10px
- subtle shadow
- series dot
- label
- bold value
- date/context
- keyboard accessible where practical

---

# 14. Motion System

Motion tokens:

| Token | Duration | Use |
|---|---:|---|
| `motion-fast` | 140ms | press / tiny feedback |
| `motion-ui` | 180ms | hover / selection |
| `motion-panel` | 220ms | dropdown / command palette |
| `motion-page` | 260ms | route/content transition |
| `motion-card` | 220ms | hover lift |
| `motion-flip` | 400ms | flashcard |
| `motion-progress` | 500–700ms | rings/charts |

Easing:
- standard: `cubic-bezier(.2,.8,.2,1)`
- entrance: `cubic-bezier(.16,1,.3,1)`

Examples:
- nav active pill moves softly
- card hover rises 2px
- button press scales .98
- command palette fades + scales from .98
- quiz answer selection changes border/surface
- unread dot fades on read
- chart draws/rises once
- flashcard uses 3D flip
- Exam Pack revised task updates ring smoothly
- Focus timer ring animates continuously but calmly

Respect reduced-motion preference.

---

# 15. Dashboard Composition

Use **Hybrid Editorial + Bento**, not a uniform grid.

Recommended desktop composition:

1. Page header:
   - greeting
   - supporting context
   - current semester
   - Quick Add / Upload

2. Academic Readiness Hero:
   - one major insight
   - weekly workload/readiness
   - compact progress visualization
   - one action

3. KPI row:
   - GPA
   - Attendance
   - Focus / Study Time

4. Primary split:
   - Today's Flow (wide)
   - Academic Health (narrow)

5. Secondary split:
   - Upcoming Deadlines
   - AI Study

6. Lower section:
   - Upcoming Exams
   - Weekly Progress / Analytics

Avoid displaying every metric above the fold.

Today's Flow should feel like a lightweight timeline, not a table.

---

# 16. AI Study Visual Language

AI Study is a light workspace with a premium AI layer.

Use:
- soft gradient hero
- richer icon containers
- glass only inside selected AI sub-panels
- subtle node/spark patterns
- animated multi-stage processing
- violet/cyan focus accents

Do not use:
- robot mascots
- neon cyberpunk
- constant moving backgrounds
- giant gradients on every card

AI hero:
- 24px radius
- 28–32px padding
- short headline
- one-line value proposition
- Upload Material
- Prepare Me for Exam
- optional credit indicator

---

# 17. Prepare Me for Exam + Exam Pack

This is the signature experience.

## 17.1 Setup journey

Use step language:

1. Select Exam
2. Study Materials
3. Preferences
4. Generate

Visually support the mental model:
**Exam → Knowledge Base → Preparation Strategy → Study Mission**

Stepper:
- connected
- completed = check
- current = indigo/violet
- future = neutral

## 17.2 Generation state

Use staged progress:
- Analyzing Material
- Identifying Important Topics
- Generating Questions
- Creating Flashcards
- Building Study Plan

Never show a fake precise percentage.

Current stage:
- premium icon container
- soft moving gradient edge
- subtle pulse only on current indicator

## 17.3 Exam Pack hero

- course monogram/color
- exam title/date
- days remaining
- readiness ring
- key counts
- recommended study time
- primary CTA: Start Revision

Tabs:
Overview
Important Topics
Short Questions
Long Questions
MCQs
Flashcards
Viva
Study Plan

Tabs can be icon + text on desktop. On mobile, horizontally scrollable.

Important Topics:
- priority dot
- compact explanation
- Mark Revised control
- progress updates visibly

Study Plan:
- vertical journey
- connected line
- day grouping
- task completion animates line/progress

---

# 18. Focus Experience

Normal Focus home stays light.

Active focus session becomes more immersive:
- dark premium canvas/panel
- sidebar/app chrome visually recedes
- large timer
- radial progress
- course color accent
- task/goal beneath timer
- Pause / Finish
- distractions suppressed visually

Do not make it a game screen.

---

# 19. Planner

Desktop:
- Month / Week / List segmented control
- course colors
- compact event chips
- icons only when they add meaning
- today indicator
- clear overdue state

Mobile:
- agenda/list is primary
- calendar summary can remain secondary
- filters in bottom sheet

Event:
- 4px course color rail
- tiny type icon
- title
- time
- status only when useful

---

# 20. Mobile System

## 20.1 Premium adaptive dock

Root navigation:
Home
Planner
Courses
AI Study
More

Dock:
- floating 10–14px above safe-area edge
- surface `rgba(255,255,255,.88)`
- backdrop blur 18–24px
- border `rgba(255,255,255,.65)`
- radius 22px
- subtle floating shadow
- active capsule uses indigo soft surface
- active icon/text indigo
- inactive icons muted
- touch target ≥ 44px

## 20.2 Mobile top bar

Root:
- page title/brand context
- search
- notification

Detail:
- back
- title
- contextual action

## 20.3 More sheet

Attendance  
GPA / CGPA  
Focus  
Analytics  
Notifications  
Settings  
Help  
Sign Out

Use icons and grouped separators.

---

# 21. Illustrations and Empty States

Use selective premium illustrations only.

Allowed contexts:
- auth side panel
- onboarding welcome
- no courses
- no assignments
- no exams
- no documents
- no notifications
- unsupported PDF
- AI success
- Exam Pack completion

Style:
- abstract geometric
- layered academic objects
- soft 3D depth
- premium shadows
- indigo/cyan/coral accents
- no childish student cartoons

Empty-state recipe:
1. icon/illustration
2. short title
3. one-line explanation
4. primary CTA
5. optional secondary action

---

# 22. Authentication and Onboarding

Authentication:
- editorial two-panel desktop composition
- form panel on surface
- subtle abstract academic/AI visual on companion side
- mobile becomes single-panel
- no authenticated app shell

Onboarding:
- focused shell
- connected stepper
- one main task per screen
- progressive disclosure
- course setup uses repeatable structured cards
- finish screen uses a restrained success moment

---

# 23. Accessibility Requirements

- minimum intended touch target: 44px
- visible keyboard focus
- no status communicated through color alone
- icons without visible labels require tooltips / semantics
- form errors placed near fields
- text contrast must remain readable on soft gradients
- do not use low-opacity body text on AI surfaces
- support reduced motion
- command palette keyboard navigable
- tabs keyboard navigable
- modal focus trap and restoration
- charts require textual equivalents / accessible summaries where needed

---

# 24. Responsive Breakpoints

Reference targets:
- 1440 desktop
- 1280 laptop
- 768 tablet
- 390 mobile

Suggested CSS/Flutter layout thresholds:
- ≥ 1280: expanded sidebar + full bento
- 1024–1279: compact grid, still sidebar
- 768–1023: collapsed navigation / reduced columns
- < 768: mobile app shell + premium dock
- 390 target must have no document-level horizontal overflow

Never remove core content to make mobile fit.

---

# 25. Screen-by-Screen Visual Treatment

The companion `StudentOS_82_Screen_Visual_Map.csv` is the authoritative visual map. Summary by module:

## Authentication — AUTH-01 to AUTH-06
Editorial auth shell, premium form surface, soft abstract companion artwork, minimal distractions. Error/success use icon + contextual surface, not giant banners.

## Onboarding — ONB-01 to ONB-07
Connected stepper, spacious forms, one decision cluster per page, abstract premium welcome artwork, restrained finish celebration.

## Dashboard — DASH-01
Highest-quality non-AI screen. Editorial+bento composition, readiness hero, tinted KPI cards, today's timeline, academic health, deadlines, AI Study premium card.

## Semesters — SEM-01 to SEM-04
Balanced academic management UI. Semester cards with timeline/status; create/edit premium adaptive forms; destructive confirmation uses coral system.

## Courses — COURSE-01 to COURSE-04
Course identity colors + monograms. Course Detail uses strong tab system, academic summary cards, upcoming items, document preview, consistent contextual actions.

## Attendance — ATT-01 to ATT-05
Dense but readable. Rings + comparison bars, status chips, mobile course cards, compact history. Never use color alone for risk.

## GPA — GPA-01 to GPA-03
Large KPI + trend line, grade rows/cards, numeric point controls, history visualization. Avoid decorative academic clichés.

## Planner — PLAN-01
Course-color calendar/events, soft segmented controls, premium filter sheet, mobile agenda-first.

## Assignments — ASSIGN-01 to ASSIGN-05
Task-oriented layouts, priority dots, due-state language, completion animation, detail sheet/card, concise forms.

## Exams — EXAM-01 to EXAM-05
Countdown emphasis, stronger Prepare Me for Exam CTA, course identity, study-material context, subtle urgency.

## Focus — FOCUS-01 to FOCUS-04
Light setup → immersive dark active state → calm completion → analytics-oriented history.

## AI Study — AI-01
Premium gradient hero + document library + tool cards. Strongest visual language outside Exam Prep.

## Documents — DOC-01 to DOC-06
Elegant dropzone, visible file metadata, stage-based processing, meaningful unsupported state, clean document detail tabs.

## Summary — SUM-01 to SUM-02
Minimal generator configuration; result uses editorial reading layout with clear concept/definition blocks.

## MCQ — MCQ-01 to MCQ-02
Compact generation controls + premium generated-set summary.

## Quiz — QUIZ-01 to QUIZ-04
Distraction-free. Large answer cards, clear progress, deterministic score, excellent review hierarchy.

## Flashcards — FLASH-01 to FLASH-04
Large tactile card, real flip motion, clean progress, thumb-friendly rating controls, restrained completion moment.

## Prepare Me for Exam — PREP-01 to PREP-06
Signature visual journey. Strong stepper, selected-material cards, strategy controls, transparent credit confirmation, staged generation, premium Exam Pack.

## Analytics — ANA-01 to ANA-02
Premium intelligent analytics: useful charts only, strong tooltips, clear filtering, persistent course colors.

## Notifications — NOTIF-01 to NOTIF-02
Readable feed, 7px unread dot, contextual icons, soft read/unread surface shift, elegant empty state.

## Settings — SET-01 to SET-08
Calm, structured, less decorative. Settings side navigation, adaptive fields, clear security/privacy grouping, disciplined danger zone.

---

# 26. “Single Dot” Registry

This is intentionally explicit.

| Dot | Size | Color | Usage |
|---|---:|---|---|
| Unread notification | 7px | Coral / Indigo | Bell and unread items |
| High priority | 8px | Coral | Priority label |
| Medium priority | 8px | Amber | Priority label |
| Low priority | 8px | Blue | Priority label |
| Chart legend | 8px | Series color | Chart legend |
| Course identity | 8px | Course color | Compact metadata |
| Current AI stage | 8px | Violet/Cyan | Generation step |
| Timeline current | 10px | Indigo | Today / study plan |
| Inactive timeline | 8px | Neutral 300 | Future stage |
| Online/presence | Do not use | — | Not needed in V1 |

---

# 27. Component State Checklist

Every interactive component must define:

- default
- hover
- pressed
- focused
- selected
- disabled
- loading where relevant
- success where relevant
- error where relevant

Every data surface must consider:
- populated
- empty
- loading
- error
- stale/retry where applicable

---

# 28. Design QA Gate

Before approving the premium redesign:

## Visual consistency
- same icon family
- no Unicode placeholder icons
- no emoji as UI iconography
- no random gradients
- radius and shadow tokens respected
- course color persistence verified

## Hierarchy
- one obvious primary action per major screen
- AI actions do not overwhelm academic tasks
- danger actions visually separated
- dashboard not overloaded

## Responsive
- all critical screens verified at 1440/1280/768/390
- no document-level horizontal overflow
- tables convert appropriately
- mobile dock does not cover important content

## Motion
- no unnecessary loops
- reduced-motion supported
- state changes remain understandable without animation

## Accessibility
- focus visible
- contrast checked
- icons labelled semantically
- status not color-only
- touch target ≥ 44px

---

# 29. Figma Structure

Recommended pages:

00 Cover  
01 Visual Direction  
02 Foundations  
03 Color Tokens  
04 Typography  
05 Iconography  
06 Components  
07 Shell + Navigation  
08 Authentication  
09 Onboarding  
10 Dashboard  
11 Academic Core  
12 Planner + Productivity  
13 AI Study  
14 Exam Prep + Exam Pack  
15 Analytics  
16 Settings  
17 Empty / Error / Loading States  
18 Mobile  
19 Motion Specs  
20 Developer Handoff  

Component variants should use properties for:
- size
- state
- icon presence
- status
- theme/surface
- density

---

# 30. Flutter Handoff Rules

Map all styling through tokens / ThemeExtensions rather than hardcoded screen-level values.

Recommended theme groups:
- `AppColors`
- `AppTypography`
- `AppSpacing`
- `AppRadius`
- `AppShadows`
- `AppMotion`
- `CoursePalette`
- `StatusPalette`
- `AiThemeTokens`

Do not hardcode course colors independently on each screen.

For icons, use one wrapper component so family/style/size can be changed globally.

---

# 31. Final Direction Statement

StudentOS should visually communicate:

> “This is my academic command center — calm enough for daily work, intelligent enough to help me think, and premium enough that I want to return.”

The premium feeling must come from:
- hierarchy
- consistency
- typography
- iconography
- purposeful color
- tactile state changes
- excellent spacing
- intelligent information design

—not from adding effects everywhere.

