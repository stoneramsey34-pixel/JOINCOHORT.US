# COHORT_DESIGN.md

## Design Philosophy

Cohort should feel smooth, calm, and clean when opened. Not crowded. Not clinical. Not corporate. It is a tool built by a clinician for clinicians — it should feel like it understands the user's world. Every design decision should reduce anxiety, not add to it. The experience of opening Cohort should feel like a breath of fresh air in an otherwise stressful licensure journey.

---

## Color System

### Light Mode (Default)

| Role | Name | Hex |
|---|---|---|
| Primary Accent | Cohort Terracotta | `#DE7356` |
| Background | Warm Cream | `#FAF9F5` |
| Surface / Cards | Soft Cream | `#F4F3EE` |
| Body Text | Deep Slate | `#141413` |
| Muted Text | Soft Mid Gray | `#B1ADA1` |
| UI Elements / Borders | Mid Gray | `#B0AEA5` |
| Destructive / Error | Red | `#D14545` |
| Success / Approved | Soft Sage | `#5A8F6E` |

### Dark Mode

| Role | Hex |
|---|---|
| Background | `#1A1917` |
| Surface / Cards | `#242220` |
| Body Text | `#FAF9F5` |
| Muted Text | `#B1ADA1` |
| Primary Accent | `#DE7356` (same) |
| UI Elements / Borders | `#3A3835` |
| Destructive / Error | `#EF6B6B` |
| Success / Approved | `#7AB893` |

### Rules
- Light mode is the default — users can switch to dark mode
- Cohort Terracotta `#DE7356` is used for: primary buttons, active navigation states, progress indicators, links, and key highlights
- Never use pure white (`#FFFFFF`) or pure black (`#000000`) — always use warm cream and deep slate equivalents
- Backgrounds are always warm, never cold or blue-tinted
- Chart and data visualization colors are defined separately per chart — never use generic template defaults

### Accessibility — Color Contrast (WCAG AA Required)
- All text-on-background combinations must meet WCAG AA contrast ratios: 4.5:1 for normal text, 3:1 for large text and UI components
- Deep Slate `#141413` on Warm Cream `#FAF9F5` — passes AA for all text sizes
- Cohort Terracotta `#DE7356` on Warm Cream `#FAF9F5` — does NOT pass AA for normal text. Use only for large text (18px+), UI elements (3:1 ratio), or as a background with white/cream text
- For primary buttons, use terracotta as the background with cream `#FAF9F5` text — this combination passes AA for large text
- Muted gray text `#B1ADA1` is for non-essential labels only. Never use for required reading content
- All color choices must be validated with a contrast checker before deployment

---

## Typography

### Font Pairing
- **Headings:** Fraunces — a warm, humanist variable serif. Used for page titles, section headers, and hero text. Conveys professionalism with a human touch.
- **Body / UI:** Inter — the most readable sans-serif for screens. Used for all body text, labels, buttons, navigation, form fields, and everything else.

### Type Scale
| Element | Font | Weight | Size |
|---|---|---|---|
| Page Title (H1) | Fraunces | 600 | 28–32px |
| Section Header (H2) | Fraunces | 600 | 22–24px |
| Subsection (H3) | Inter | 600 | 18px |
| Body | Inter | 400 | 15–16px |
| Label / Caption | Inter | 500 | 13px |
| Button | Inter | 500 | 14px |
| Navigation | Inter | 500 | 14px |

### Rules
- Never use more than two fonts — Fraunces and Inter only
- Headings use Fraunces, everything else uses Inter
- Line height for body text: 1.6 — open and readable, never cramped
- Letter spacing on headings: slightly loose — never tight
- Never use font sizes below 13px — accessibility requirement

---

## Brand Voice — How Cohort Sounds in Writing

Cohort writes to its users like a peer — another clinician who has been through the journey. Warm. Direct. No fluff. No corporate buzzwords. No condescension.

### Voice Principles
- **Peer to peer.** Cohort is not a brand talking down to a user — it is a colleague sitting next to them
- **Warm but never saccharine.** Encouraging without being patronizing
- **Direct.** Say what you mean. Don't bury the point
- **Honest.** If something is hard, acknowledge it. Don't pretend everything is easy
- **No buzzwords.** No "leverage," "synergy," "empower," "journey" (unless contextually accurate), or any other corporate filler
- **No em dashes** in product copy. Use regular punctuation
- **Short copy.** When in doubt, cut the sentence in half

### Examples

**Onboarding welcome — bad:**
"Welcome to Cohort! We're so excited to empower you on your transformative licensure journey toward becoming a fully-licensed clinician!"

**Onboarding welcome — good:**
"Welcome. Let's get your hours in order."

**Hour approval notification — bad:**
"Great news! Your supervisor has successfully approved your recent hour submission."

**Hour approval notification — good:**
"Dr. Smith approved 8 hours."

**Error message — bad:**
"Oops! Something went wrong. Please try again later."

**Error message — good:**
"That didn't save. Check your connection and try again."

---

## Layout and Spacing

### Philosophy
Open and airy. Generous whitespace. Content should breathe. Never pack elements together. When in doubt, add more space not less.

### Mobile-First
Cohort is designed mobile-first. Every screen, component, and feature is designed for a phone first, then adapted for larger screens. The mobile experience is the primary experience, not an afterthought.

### Responsive Breakpoints (Standard)
- **Mobile:** `< 768px`
- **Tablet:** `768px – 1024px`
- **Desktop:** `> 1024px`

### Spacing Scale (base-8)
- `4px` — tight internal padding
- `8px` — small gaps between related elements
- `16px` — standard component padding
- `24px` — section spacing within a page
- `32px` — spacing between major sections
- `48px` — page-level vertical rhythm
- `64px` — large section separators

### Cards and Containers
- Cards have `16–24px` internal padding
- Cards use a soft border (`1px solid #B0AEA5` at low opacity) or a subtle shadow — never both
- Cards never feel cramped — content inside has room to breathe
- Rounded corners: `12px` border radius on cards, `8px` on buttons and inputs, `6px` on badges

---

## Navigation

### Desktop (Top Bar)
- Fixed top navigation bar
- Logo / wordmark on the left
- Primary navigation links centered or left-aligned
- User account / settings on the right
- Height: `56–64px`
- Background: matches surface color with a subtle border bottom
- Active state: terracotta underline or terracotta text color

### Mobile (Bottom Bar)
- Fixed bottom navigation bar
- 4–5 icon-based navigation items
- Active item uses terracotta color
- Labels below icons — always labeled, never icon-only (accessibility)
- Height: `56–64px` plus safe area inset
- Background: matches surface color with a subtle top border

### Navigation Items (Phase 1)
- Dashboard
- My Hours
- Licensure Progress
- Supervisors
- Settings

---

## Supervisor View vs Supervisee View

The supervisor view must look visually distinct from the supervisee view so a user always knows which mode they are in.

### Visual Differentiation
- **Supervisor view** uses a subtle dark-mode-inverted accent on the navigation bar — a thin slate-colored band that signals "you are in supervisor mode"
- **Supervisor view** dashboards prioritize the list of supervisees and pending approvals
- **Supervisee view** dashboards prioritize the user's own progress, hour totals, and licensure step tracker
- A clear text label in the top-right of the nav bar always indicates current view: "Supervisor View" or "My Account"
- If a user has both roles (rare but possible), they can switch between them with a visible toggle

---

## Components

### Buttons
- **Primary:** Terracotta background `#DE7356`, cream text `#FAF9F5`, `8px` radius
- **Secondary:** Transparent background, terracotta border and text
- **Outline:** Subtle border, muted text — for low-emphasis actions
- **Destructive:** Red background for irreversible actions
- All buttons: `Inter 500`, `14px`, `8–16px` horizontal padding, `10–12px` vertical padding
- Hover states: slightly darker shade of the button color — never a jarring change
- Focus state: visible outline ring meeting WCAG AA contrast — required for keyboard accessibility
- No sharp square buttons anywhere in the app
- Minimum touch target: `44x44px` for accessibility

### Form Inputs
- Border: `1px solid #B0AEA5`
- Border radius: `8px`
- Focus state: terracotta border `#DE7356` plus visible focus ring
- Background: `#FAF9F5` (warm cream) in light mode, `#242220` in dark mode — never pure white
- Placeholder text: muted gray `#B1ADA1`
- Error state: red border with error message AND error icon below the field (color is never the only signal)
- All inputs have visible labels above them — never placeholder-only

### Progress Bars
- Used for hour tracking progress toward licensure requirements
- Track background: `#F4F3EE` (light) or `#3A3835` (dark)
- Fill color: terracotta `#DE7356`
- Height: `8px` — visible but not oversized
- Rounded ends
- Always accompanied by a text label showing exact numbers (e.g. "342 / 500 hours")
- Feel encouraging, not clinical — progress should feel like momentum

### Cards
- Background: `#F4F3EE` (light) or `#242220` (dark)
- Border radius: `12px`
- Subtle shadow: `0 1px 4px rgba(0,0,0,0.06)`
- Internal padding: `20–24px`
- Never use heavy drop shadows

### Badges / Status Pills
- `Pending` — gray background, muted text, optional clock icon
- `Approved` — soft sage background, dark sage text, checkmark icon
- `Flagged` — soft red background, dark red text, flag icon
- Border radius: `999px` (fully rounded pill)
- Font: `Inter 500`, `12–13px`
- Status badges always include both color AND icon — color is never the sole indicator (accessibility)

### Empty States

Empty states are designed intentionally because new users land on empty everything. Every empty state has three parts:

1. **A clear visual** — a soft illustration or icon, never a stock image
2. **A short message in plain language** — what is this screen and why is it empty
3. **A single clear next action** — a button or link to do the next obvious thing

### Examples

- **Empty Hours Log:** "No hours yet. Log your first session to get started." with a "Log Hours" button
- **Empty Supervisor List:** "You haven't added any supervisors yet." with an "Invite Supervisor" button
- **Empty Licensure Tracker:** Shows the first step with a "Mark Started" call to action

---

## Loading States

- **Skeleton screens** preferred over spinners for content loading
- **Spinners** only for short actions (button submits, save confirmations)
- **Full page loading** never lasts more than 2 seconds. If it does, show progressive content
- **Loading text** for screen readers — "Loading your hour log" — never silent

---

## Iconography
- Use **Lucide Icons** — clean, consistent, open source, works with React
- Icon size: `18–20px` for UI, `16px` for inline use
- Icons always paired with a label in navigation — never icon-only
- Icon color matches surrounding text color — never decorative random colors

---

## Data Visualization
- Used for hour progress, licensure step completion, and supervisor relationship timelines
- Keep charts simple — no unnecessary complexity
- Preferred chart types: progress bars, donut charts for category breakdown, simple bar charts for historical hours
- Chart colors: define a specific Cohort palette for charts
- Charts must be readable in both light and dark mode
- Charts must be accessible — include text labels, data tables as alternatives, and ARIA descriptions for screen readers
- Always include axis labels and legends — never assume the user knows what they're looking at

---

## Motion and Interaction
- Transitions: `150–200ms ease` — fast enough to feel snappy, slow enough to feel smooth
- No jarring jumps or instant state changes
- Page transitions: subtle fade — nothing dramatic
- Loading states: skeleton screens preferred over spinners where possible
- Respect `prefers-reduced-motion` — disable non-essential animations for users who have requested reduced motion (accessibility)
- Never use motion that feels like it's showing off — motion serves function only

---

## Accessibility Standards

This section reinforces and details what is committed to in COHORT.md.

### WCAG 2.1 Level AA Compliance
- All color contrast ratios meet 4.5:1 for normal text, 3:1 for large text and UI components
- All interactive elements have visible focus indicators
- All actions can be completed via keyboard alone
- All images and icons have meaningful alt text or are marked decorative
- All form fields have associated labels
- Page structure uses semantic HTML headings in logical order
- Status and error messages do not rely on color alone — always paired with text or icons
- Users can zoom to 200% without breaking layout
- Reduced motion is respected
- All ARIA roles and attributes are used correctly where needed

---

## Tone and Feel Summary
Cohort should feel like it was designed by someone who has been through the licensure process and understands the stress of it. Every screen should communicate: "you are on track, you are making progress, we have you covered." Clean. Warm. Trustworthy. Professional without being cold.

---

## What Cohort Should Never Look Like
- A generic SaaS dashboard with cold blue tones
- A medical or clinical records system
- A student homework tracker
- An AI chatbot interface
- Anything that feels templated, generic, or rushed

---

*All design decisions must reference this document. When in doubt, choose the option that feels warmer, cleaner, more accessible, and less crowded.*
