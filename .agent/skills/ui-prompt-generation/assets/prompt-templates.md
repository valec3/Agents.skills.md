# UI Prompt Templates

Ready-to-use templates for common UI scenarios. Customize with specific patterns from ui-patterns.md and values from design-tokens.md.

---

## Template 1: Landing Page Hero Section

```markdown
# Landing Page Hero

## Purpose

[Describe user goal: e.g., "Convert visitors to sign up for beta"]

## Layout & Structure (Tipo 1, 2)

- Layout: Centered hero with single CTA
- Width: Full viewport width, max-content 1280px centered
- Height: Min 100vh, scroll cue at bottom
- Background: [specify: gradient, image, video, solid color]

## Visual Hierarchy (Tipo 10)

Headline:

- Text: "[Your compelling headline]"
- Typography: type-scale-9 (64px), weight-bold (700), leading-tight (1.1)
- Color: neutral-900 (light mode), neutral-50 (dark mode)
- Mobile: type-scale-7 (40px)

Subheadline:

- Text: "[Supporting copy, 1-2 sentences]"
- Typography: type-scale-4 (20px), weight-normal (400), leading-relaxed (1.75)
- Color: neutral-600 (light mode), neutral-400 (dark mode)
- Max width: 600px
- Mobile: type-scale-3 (16px)

## Primary CTA (Tipo 3, 5)

Button:

- Text: "[Action verb + benefit]"
- Style: Primary variant
- Background: primary-500, hover: primary-600
- Typography: type-scale-4 (20px), weight-semibold (600)
- Padding: spacing-md (16px) vertical, spacing-xl (32px) horizontal
- Border radius: radius-lg (12px)
- Shadow: shadow-lg, hover: shadow-xl
- Animation: duration-fast (150ms), easing-smooth, hover elevate 4px

Secondary CTA (optional):

- Text: "[Alternative action]"
- Style: Ghost variant
- Typography: type-scale-3 (16px), weight-medium (500)
- Color: neutral-600, hover: neutral-800

## Trust Indicators (Tipo 2)

- Position: Below CTAs
- Content: [Logos, testimonial snippets, metrics]
- Style: Muted (neutral-400), small (type-scale-2)
- Layout: Horizontal row, spacing-lg gaps

## Visual Element

- Type: [Mockup, illustration, photo, video]
- Position: [Centered below copy, split screen right side]
- Effect: [Floating with shadow-2xl, parallax subtle]
- Animation: [Reveal on scroll, duration-slow]

## Scroll Indicator

- Type: Animated arrow or text "Scroll to explore"
- Position: Bottom center, spacing-2xl from bottom edge
- Animation: Bounce or pulse, duration-slowest, infinite loop

## Responsive (Tipo 13)

Desktop (1024px+):

- Layout: Split screen if visual element right-aligned
- Spacing: spacing-3xl (64px) vertical

Tablet (640-1024px):

- Layout: Stacked, centered
- Spacing: spacing-2xl (48px) vertical

Mobile (< 640px):

- Layout: Stacked, full width
- Spacing: spacing-xl (32px) vertical
- CTA: Full width buttons, stacked

## Accessibility

- Heading hierarchy: H1 for main headline
- Alt text: [For visual element]
- Focus: Visible on CTA (3px outline, primary-500)
- Contrast: All text meets WCAG AA

## Style (Tipo 11)

- Aesthetic: [Soft minimalism, editorial design, etc.]
- Color palette: [Accent color-driven UI, monochrome base + color highlight]
- Dark mode: [Yes/No, if yes specify adaptations]
```

---

## Template 2: Dashboard Layout

```markdown
# Dashboard Interface

## Purpose

[User goal: e.g., "Monitor key metrics at a glance, filter data, take quick actions"]

## Layout & Structure (Tipo 1, 8)

- Layout: Sidebar + main content area
- Sidebar: 240px fixed width, colapsable to 60px (icons only)
- Main: Flexible width, max 1440px
- Spacing: spacing-lg (24px) gaps between cards

## Navigation (Tipo 4)

Sidebar:

- Background: neutral-900 (always dark)
- Links: type-scale-3 (16px), neutral-400, hover: neutral-100
- Active: primary-500 left border (4px), neutral-100 text
- Icons: 20px, aligned left
- Collapse toggle: Top right, animated hamburger

Top bar:

- Background: white (light mode), neutral-900 (dark mode)
- Height: 64px
- Contents: Search, notifications, profile menu
- Sticky: Yes (z-sticky)

## Dashboard Components (Tipo 8)

### KPI Cards

- Layout: 4 columns (desktop), 2 columns (tablet), 1 column (mobile)
- Card style: Soft cards, radius-lg, padding-lg
- Shadow: shadow-md, hover: shadow-lg
- Content:
  - Label: type-scale-2 (14px), neutral-600, weight-medium
  - Value: type-scale-8 (48px), neutral-900, weight-bold
  - Change indicator: Small badge (success-500 ↑ or error-500 ↓)
  - Trend: Sparkline chart (neutral-400, 40px height)

### Data Table

- Style: Dense layout for power users
- Header: type-scale-2 (14px), weight-semibold, neutral-700, bg-neutral-50
- Rows: Hover bg-neutral-50, spacing-sm padding
- Actions: Contextual, appear on row hover
- Sorting: Click header, visual indicator (arrow icon)
- Filters: Visual filters above table (Tipo 8)
- Pagination: Bottom right, [1] 2 3 ... 10

### Filters Panel (Tipo 8)

- Position: Top of main content, collapsible
- Layout: Horizontal row, wrapping on small screens
- Style: Soft cards or outline cards
- Components:
  - Date range picker
  - Multi-select dropdowns (tag-based UI)
  - Search input
  - "Apply" primary button, "Reset" ghost button

### Charts

- Style: Muted color palette with accent color for highlights
- Grid lines: neutral-200, subtle
- Tooltips: Appear on hover, shadow-xl, type-scale-2
- Legend: Top right, horizontal layout

## States (Tipo 12)

### Empty Dashboard

- Illustration: Centered, 200px height
- Heading: type-scale-5, neutral-800, "No data yet"
- Body: type-scale-3, neutral-600, "Import your first dataset to see metrics"
- CTA: Primary button, "Import Data"

### Loading

- Skeleton: Cards with animated shimmer
- Duration: Show immediately, remove when data loads
- Style: neutral-100 background, neutral-200 shimmer

### Error

- Alert: error-50 background, error-600 border, error icon
- Message: Human language, actionable ("Connection failed. Retry?")
- Action: "Retry" button, secondary variant

### Filters No Results

- Message: "No results match your filters"
- Action: "Clear filters" link
- Style: Centered, neutral-600 text

## Microinteractions (Tipo 5)

- Card hover: Subtle elevation, shadow-lg, duration-fast
- Button press: Scale 0.98
- Inline editing: Click → input appears, focus automatically
- Success feedback: Green checkmark animation, duration-base
- Data refresh: Subtle pulse animation on updated values

## Responsive (Tipo 13)

Desktop (1024px+):

- Sidebar: Full width (240px)
- KPI cards: 4 columns
- Table: Full features

Tablet (640-1024px):

- Sidebar: Collapsible, overlay when open
- KPI cards: 2 columns
- Table: Hide less critical columns
- Filters: Stack vertically

Mobile (< 640px):

- Navigation: Bottom navigation bar (4-5 items)
- KPI cards: 1 column, swipeable horizontal scroll
- Table: Card view instead (each row = card)
- Filters: Bottom sheet

## Accessibility

- Keyboard nav: Full support, logical tab order
- Focus: Visible on all interactive elements
- ARIA live: Announce data updates in real-time
- Screen reader: Announce chart values on focus
- High contrast: Meets WCAG AA

## Animations (Tipo 6)

- Dashboard load: Staggered entrance (100ms delay per card)
- Data update: Fade new values (duration-base)
- Chart: Animate on first load (duration-slow)
- Transitions: All duration-base (300ms), easing-smooth

## Style (Tipo 11)

- Aesthetic: Soft minimalism
- Colors: Muted palette, accent color-driven CTAs
- Dark mode: Support both, toggle in profile menu
```

---

## Template 3: Form Interface

```markdown
# Form Interface: [Form Name]

## Purpose

[User goal: e.g., "Complete checkout", "Create account", "Submit feedback"]

## Layout & Structure (Tipo 1, 3)

- Container: Centered, max-width 600px
- Card: Soft card with padding-2xl (48px)
- Shadow: shadow-lg
- Background: white (light mode), neutral-900 (dark mode)
- Border radius: radius-xl (16px)

## Visual Hierarchy (Tipo 10)

Title:

- Text: "[Form purpose]"
- Typography: type-scale-6 (32px), weight-bold (700)
- Color: neutral-900 (light), neutral-50 (dark)
- Margin bottom: spacing-md

Subtitle (optional):

- Text: "[Additional context or step indicator]"
- Typography: type-scale-3 (16px), neutral-600
- Margin bottom: spacing-xl

## Form Fields

### Text Input

Structure:

- Label: type-scale-3 (16px), weight-medium (500), neutral-700
- Input: type-scale-3, padding-md, radius-md, border 1px neutral-300
- Required indicator: Red asterisk (\*) next to label
- Optional indicator: "(optional)" in neutral-500
- Help text: type-scale-2 (14px), neutral-600, below input

States:

- Default: border neutral-300
- Focus: border primary-500 (2px), shadow-sm (primary with opacity-25)
- Filled: border neutral-400
- Error: border error-500 (2px), error message below
- Disabled: bg-neutral-100, opacity-50, cursor not-allowed
- Success: border success-500, checkmark icon right

Error Message:

- Typography: type-scale-2 (14px), error-600, weight-medium
- Icon: Error icon, 16px, error-600
- Margin top: spacing-xs (4px)

### Textarea

- Same as text input
- Min height: 120px
- Resize: Vertical only
- Character count: Bottom right, type-scale-2, neutral-500

### Select Dropdown

- Same styling as text input
- Chevron icon: Right side, neutral-500, 16px
- Dropdown panel: shadow-xl, radius-md, max-height 300px, scroll
- Options: padding-sm, hover bg-neutral-100, selected bg-primary-50

### Checkbox

- Size: 20px × 20px
- Border: 2px neutral-400, radius-sm
- Checked: bg-primary-500, white checkmark
- Focus: 3px outline, primary-500 with opacity-50
- Label: type-scale-3, neutral-700, clickable

### Radio Button

- Same as checkbox but radius-full (circular)

## Button Group

Primary button:

- Text: "[Submit action]"
- Style: bg-primary-500, hover primary-600, text white
- Typography: type-scale-3, weight-semibold
- Padding: spacing-md vertical, spacing-2xl horizontal
- Full width: On mobile
- Icon: Optional (right side, 20px)
- Loading state: Spinner, "Processing...", disabled

Secondary button:

- Text: "Cancel" or "Back"
- Style: Ghost variant, neutral-600 text
- Position: Left of primary (desktop), above primary (mobile)

## Sections & Steps

Multi-step form:

- Stepper: Top of form, horizontal, visual indicator
- Current step: primary-500, bold
- Completed steps: success-500, checkmark
- Future steps: neutral-300
- Step labels: type-scale-2

Section divider:

- Horizontal line: 1px neutral-200
- Margin: spacing-xl vertical
- Optional heading: type-scale-4, weight-semibold, neutral-800

## Validation (Tipo 5, 12)

Inline validation:

- Trigger: On blur (after user leaves field)
- Success: Subtle green border, checkmark (don't over-celebrate)
- Error: Red border, error message, error icon
- Real-time: For password strength, username availability

Form-level validation:

- Trigger: On submit attempt
- Error summary: Top of form, error-50 bg, error-600 border
- Format: Bulleted list of errors with links to fields
- Auto-focus: First error field

## States (Tipo 12)

Loading:

- Skeleton: For pre-filled forms loading data
- Submit loading: Button spinner, "Processing...", form disabled

Success:

- Replace form with success message
- Icon: Large checkmark, success-500, centered
- Heading: "Success!", type-scale-6
- Body: Confirmation message
- CTA: "Done" or next action button

Error:

- Keep form visible
- Alert: error-50 bg, error-600 border, top of form
- Message: Human-friendly, actionable
- Action: "Try again" or "Contact support"

## Progressive Disclosure

- Start with essential fields only
- "Advanced options" expandable section
- Animation: Smooth height transition, duration-base
- Icon: Chevron right (collapsed), chevron down (expanded)

## Responsive (Tipo 13)

Desktop (1024px+):

- Form: 600px max width, centered
- Buttons: Inline (side-by-side)
- Two-column: Name (first, last) in row

Tablet (640-1024px):

- Form: 90% width
- Buttons: Inline but smaller spacing

Mobile (< 640px):

- Form: Full width, spacing-md padding
- Buttons: Full width, stacked
- All fields: Single column
- Touch targets: 44px minimum
- Sticky CTA: Bottom sheet with primary button

## Accessibility

- Keyboard: Tab order logical, Enter submits
- Labels: Associated with inputs (for/id)
- ARIA: aria-invalid, aria-describedby for errors
- Focus: Visible on all fields (3px outline)
- Autofocus: First field on page load (if appropriate)
- Autocomplete: Enabled (name, email, address, etc.)

## Animations (Tipo 6)

- Field focus: Border color transition, duration-fast
- Error shake: Horizontal shake on validation error, duration-fast
- Success: Checkmark fade in, duration-base
- Step transition: Fade out → fade in, duration-base

## Style (Tipo 11)

- Aesthetic: [Clean, professional, friendly, etc.]
- Spacing: Generous (not cramped)
- Colors: Minimal color, accent on CTAs and feedback
```

---

## Template 4: Navigation System

```markdown
# Navigation System

## Purpose

[User goal: e.g., "Navigate between main sections", "Access key features quickly"]

## Desktop Navigation (Tipo 4)

### Top Navigation Bar

Structure:

- Background: white (light), neutral-900 (dark)
- Height: 64px
- Padding: spacing-md horizontal
- Shadow: shadow-sm
- Sticky: Yes (z-sticky: 1020)

Logo:

- Position: Left side
- Size: 32px height, auto width
- Link: Home page

Main Navigation Links:

- Position: Center or left (after logo)
- Spacing: spacing-lg between items
- Typography: type-scale-3 (16px), weight-medium (500)
- Color: neutral-700 (light), neutral-300 (dark)
- Hover: neutral-900, underline (2px, primary-500, animated)
- Active: primary-500 text, underline

Utility Navigation:

- Position: Right side
- Items: Search, notifications, user menu
- Spacing: spacing-md between items

### Mega Menu (optional)

Trigger: Hover over main link (with 200ms delay)
Structure:

- Container: Full width, shadow-xl, padding-xl
- Background: white (light), neutral-900 (dark)
- Layout: Multi-column grid (3-4 columns)
- Animation: Fade + slide down, duration-base

Content:

- Section headings: type-scale-4, weight-semibold, neutral-900
- Links: type-scale-3, neutral-700, hover primary-500
- Icons: 20px, neutral-500, left of text
- Featured item: Card with image, larger, right column

## Mobile Navigation (Tipo 13)

### Mobile Header

- Background: Same as desktop
- Height: 56px
- Content: Logo (center), hamburger (left), utility icon (right)

### Hamburger Menu

Icon:

- Size: 24px
- Color: neutral-700
- Animation: Transform to X when open, duration-base

Menu Panel:

- Type: Full-screen overlay or slide-in drawer
- Animation: Slide from left, duration-base, easing-smooth
- Background: white (light), neutral-900 (dark)
- Z-index: z-modal (1040)

Navigation Links:

- Layout: Stacked vertically, full width
- Typography: type-scale-4 (20px), weight-medium
- Color: neutral-900 (light), neutral-100 (dark)
- Padding: spacing-md vertical, spacing-lg horizontal
- Separator: 1px neutral-200 between items
- Active: primary-500 left border (4px), bg-primary-50

Nested Items:

- Expandable: Chevron right, click to expand
- Animation: Smooth height transition, duration-base
- Indentation: spacing-lg left padding

### Bottom Navigation (mobile alternative)

- Position: Fixed bottom, full width
- Background: white (light), neutral-900 (dark)
- Shadow: shadow-xl (upward)
- Height: 64px
- Items: 4-5 icons + labels
- Icon size: 24px
- Label: type-scale-1 (12px)
- Active: primary-500 color, bold label
- Tap: Scale 0.95, duration-fast

## Scroll Behavior (Tipo 4, 9)

### Scroll-Aware States

Default (top of page):

- Full height (64px)
- Full logo
- All items visible

Scrolling down:

- Reduce height (56px)
- Smaller logo
- Hide less important items
- Smooth transition: duration-base

Scrolling up:

- Fully visible again
- Smooth slide down: duration-base

### Sticky Behavior

- Always visible (sticky)
- Background: Semi-transparent blur (glassmorphism) on scroll
- Shadow: Increase shadow on scroll (shadow-sm → shadow-md)

## Components

### Search

Desktop:

- Type: Expandable input or always-visible
- Width: 300px (expanded)
- Icon: Magnifying glass, 20px
- Input: type-scale-3, padding-sm, radius-md
- Dropdown: Search suggestions, shadow-xl

Mobile:

- Type: Full-screen overlay when activated
- Animation: Fade in, duration-base
- Input: Large, type-scale-4, centered
- Close button: Top right, X icon

### Notifications

Icon:

- Bell icon, 20px
- Badge: Small red circle with count (if unread)
- Hover: Slight bounce animation

Dropdown:

- Width: 360px (desktop)
- Max height: 400px, scrollable
- Shadow: shadow-xl
- Items: Unread (neutral-50 bg), read (white bg)
- Empty state: Illustration, "No notifications"

### User Menu

Trigger:

- Avatar: 32px circle, user image or initials
- Hover: Ring (2px primary-500)

Dropdown:

- Width: 240px
- Shadow: shadow-xl
- Sections: Profile, settings, logout
- Separator: 1px neutral-200 between sections
- Items: Icon + label, hover bg-neutral-50

## States (Tipo 12)

Loading:

- Skeleton: For navigation items loading dynamically
- Duration: Brief, avoid showing for < 500ms

Error:

- Fallback: Show static navigation items
- Retry: Automatic, silent

## Accessibility

- Keyboard: Full keyboard navigation, Escape closes menus
- Focus: Visible on all items (3px outline)
- ARIA: aria-expanded for dropdowns, aria-current for active page
- Screen reader: Announce menu open/close, active page
- Skip link: "Skip to main content" at very top (visible on focus)

## Animations (Tipo 6)

- Menu open: Fade + slide, duration-base, easing-smooth
- Mega menu: Fade + slide down, duration-base
- Scroll transition: Height/size changes, duration-base
- Hover: Underline slide in, duration-fast

## Responsive

Desktop (1024px+):

- Top navigation with dropdowns/mega menu
- All items visible

Tablet (640-1024px):

- Top navigation
- Some items in hamburger menu
- Mega menu: Simplified or removed

Mobile (< 640px):

- Hamburger menu OR bottom navigation
- Full-screen overlays for search/menu
- Touch-friendly spacing (44px targets)

## Style (Tipo 11)

- Aesthetic: [Clean, modern, minimal]
- Transparency: [Opaque or glassmorphism on scroll]
- Borders: [Subtle bottom border or shadow only]
```

---

## Template 5: Card Component

```markdown
# Card Component: [Card Name]

## Purpose

[What content does this card contain? What action does it support?]

## Visual Structure (Tipo 3)

Container:

- Background: white (light mode), neutral-900 (dark mode)
- Border: [1px solid neutral-200 OR no border for soft card]
- Border radius: radius-lg (12px)
- Padding: spacing-lg (24px)
- Shadow: shadow-md (default), shadow-lg (hover)
- Min height: [if fixed, e.g., 320px]
- Aspect ratio: [if applicable, e.g., 16:9 for media]

## Content Layout

### Media (if applicable)

- Type: Image, video, or illustration
- Position: Top of card
- Aspect ratio: 16:9
- Border radius: radius-lg (top corners only)
- Object fit: Cover
- Placeholder: neutral-200 bg during load
- Fallback: Icon + text if media fails

### Content Area

Padding: spacing-lg (24px)

Title:

- Typography: type-scale-5 (24px), weight-semibold (600)
- Color: neutral-900 (light), neutral-50 (dark)
- Line clamp: 2 lines max, ellipsis

Description:

- Typography: type-scale-3 (16px), weight-normal (400), leading-normal (1.5)
- Color: neutral-600 (light), neutral-400 (dark)
- Line clamp: 3 lines max, ellipsis
- Margin top: spacing-sm (8px)

Metadata:

- Typography: type-scale-2 (14px), neutral-500
- Content: [Date, author, category, etc.]
- Layout: Horizontal row, spacing-md gaps
- Icons: 16px, neutral-500
- Margin top: spacing-md (16px)

### Actions

Position: Bottom of card
Layout: Horizontal row, right-aligned
Spacing: spacing-sm (8px) between buttons

Primary action:

- Button: Primary variant or text link
- Typography: type-scale-3, weight-medium
- Icon: Optional, 16px, right side

Secondary action:

- Button: Ghost variant
- Typography: type-scale-2, weight-medium

## Interactive States (Tipo 5)

### Default

- Appearance: As specified above
- Cursor: default (or pointer if entire card is clickable)

### Hover (desktop)

- Elevation: translateY(-4px)
- Shadow: shadow-lg (from shadow-md)
- Border: If outline card, change to primary-500
- Media: Slight scale (1.05) if image
- Transition: duration-base (300ms), easing-smooth
- Title: Optional color change to primary-500

### Active

- Transform: scale(0.98)
- Shadow: shadow-md

### Focus

- Outline: 3px solid primary-500 with opacity-50
- Outline offset: 2px
- Trigger: Keyboard navigation or entire card is clickable

### Disabled

- Opacity: opacity-50
- Cursor: not-allowed
- No hover effects
- Actions: Disabled state

### Loading

- Skeleton: Entire card is skeleton placeholder
- Media: neutral-200 bg with shimmer
- Text: Gray bars with shimmer animation
- Duration: Show immediately on initial load

### Empty

- No media: Show icon placeholder (48px, neutral-400, centered)
- No content: "No content available" message

## Card Variants

### Elevated Card

- Shadow: shadow-lg by default
- Background: Solid color
- Border: None

### Soft Card

- Shadow: None
- Background: neutral-50 (light), neutral-800 (dark)
- Border: None

### Outline Card

- Shadow: None
- Background: Transparent
- Border: 1px solid neutral-200

### Interactive Card

- Entire card is clickable
- Hover: More prominent elevation
- Cursor: pointer on entire card
- Actions: Progressive disclosure (appear on hover)

## Progressive Disclosure (Tipo 5)

Actions on hover:

- Default: Actions hidden or at opacity-0
- Hover: Actions fade in (opacity-100, duration-fast)
- Position: Overlay on media or bottom of card

## Responsive (Tipo 13)

Desktop (1024px+):

- Width: [e.g., 33.33% in 3-column grid]
- Padding: spacing-lg (24px)
- Hover effects: Enabled

Tablet (640-1024px):

- Width: [e.g., 50% in 2-column grid]
- Padding: spacing-md (16px)
- Hover effects: Enabled

Mobile (< 640px):

- Width: 100% (full width)
- Padding: spacing-md (16px)
- Hover effects: Disabled (use tap)
- Actions: Always visible (no progressive disclosure)
- Media aspect ratio: Optional adjustment (e.g., 4:3 instead of 16:9)

## Accessibility

- Heading: Title is H3 (or appropriate level)
- Focus: Visible outline on card or action buttons
- Keyboard: Tab navigates to actions, Enter activates
- ARIA: role="article" if entire card is content unit
- Alt text: For media images
- Links: Descriptive text (not "Read more")

## Animation (Tipo 6)

Entrance (optional):

- Type: Fade + slide up
- Duration: duration-base (300ms)
- Delay: Staggered (100ms between cards)
- Trigger: On scroll into viewport

Hover transition:

- Properties: transform, box-shadow
- Duration: duration-base (300ms)
- Easing: easing-smooth

## Grid Layout (when used in collection)

Desktop:

- Columns: 3 (or 4 for smaller cards)
- Gap: spacing-lg (24px)
- Layout: CSS Grid or flexbox with wrap

Tablet:

- Columns: 2
- Gap: spacing-md (16px)

Mobile:

- Columns: 1
- Gap: spacing-md (16px)

## Style (Tipo 11)

- Aesthetic: [Soft minimalism, editorial design, etc.]
- Media treatment: [Full-bleed, rounded, with overlay]
- Elevation strategy: [Subtle or prominent shadows]
```

---

## Using Templates

1. **Copy relevant template** - Start with closest match to your need
2. **Customize bracketed sections** - Replace [placeholders] with specific content
3. **Add/remove sections** - Templates are comprehensive; pare down as needed
4. **Reference pattern types** - Use tipo numbers to link to ui-patterns.md
5. **Specify tokens** - Replace generic descriptions with exact token values
6. **Complete checklist** - Use component-checklist.md to ensure completeness

Templates provide structure; patterns provide vocabulary; tokens provide precision. Combine all three for production-ready UI prompts.
