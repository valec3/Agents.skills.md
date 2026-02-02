# Accessibility Guidelines for UI Prompts

Quick reference for ensuring accessible UI specifications. Use when generating prompts to ensure WCAG compliance and inclusive design.

---

## WCAG 2.1 Level AA Requirements

### Color Contrast

```
Normal text (< 18px):     4.5:1 minimum
Large text (≥ 18px):      3:1 minimum
UI components:            3:1 minimum
Icons (informational):    3:1 minimum
```

**In prompts, specify:**

```
Text: neutral-800 on white background (contrast ratio 12.63:1, WCAG AAA)
Button: primary-500 bg with white text (contrast 4.5:1, WCAG AA)
Disabled text: neutral-400 on white (3.2:1, meets minimum for disabled state)
```

**Check contrasts:**

- Primary-500 (#0EA5E9) on white: 3.26:1 ❌ (Too low for text, OK for UI components)
- Primary-600 (#0284C7) on white: 4.52:1 ✅ (Meets AA for normal text)
- Neutral-800 (#262626) on white: 12.63:1 ✅ (Meets AAA)

---

## Keyboard Navigation

### Tab Order

- [ ] Logical flow (top to bottom, left to right)
- [ ] Skip links before main navigation
- [ ] Modal traps focus until closed
- [ ] No keyboard traps (can always escape)

**In prompts, specify:**

```
Tab order:
1. Skip to main content link (visible on focus)
2. Logo (if linked)
3. Main navigation (left to right)
4. Search input
5. User menu
6. Main content
7. Footer navigation

Keyboard shortcuts:
- Tab: Next element
- Shift+Tab: Previous element
- Enter/Space: Activate button/link
- Escape: Close modal/menu
- Arrow keys: Navigate within menu/list
```

### Focus Indicators

**Required:**

- Visible on all interactive elements
- Min 3px outline
- High contrast (3:1 against background)
- Not removed by CSS (`outline: none` only if custom focus style provided)

**In prompts, specify:**

```
Focus state:
- Outline: 3px solid primary-500 (meets 3:1 contrast)
- Outline offset: 2px (separation from element)
- Border radius: Match element (radius-md)
- Animation: Fade in, duration-fast (150ms)
- Z-index: Ensure visible above adjacent elements
```

---

## Screen Reader Support

### ARIA Attributes

**Landmarks:**

```html
role="banner" → Site header role="navigation" → Nav menus (use
<nav>
  ) role="main" → Main content (use
  <main>
    ) role="complementary" → Sidebars (use
    <aside>) role="contentinfo" → Footer role="search" → Search form</aside>
  </main>
</nav>
```

**Interactive:**

```html
role="button" → Click/tap actions (use
<button>
  ) role="link" → Navigation (use
  <a
    >) role="dialog" → Modals role="alert" → Important messages role="status" →
    Status updates role="tablist/tab" → Tab interfaces</a
  >
</button>
```

**States:**

```html
aria-expanded="true/false" → Collapsible content aria-selected="true/false" →
Selected item aria-checked="true/false" → Checkboxes/radios aria-disabled="true"
→ Disabled elements aria-invalid="true" → Form errors aria-required="true" →
Required fields aria-hidden="true" → Hidden from screen readers
```

**Descriptions:**

```html
aria-label="Descriptive text" → Override element text aria-labelledby="id" →
Reference another element aria-describedby="id" → Additional description
alt="Descriptive text" → Image descriptions
```

**In prompts, specify:**

```
Button:
- Element: <button>
- ARIA label: "Close modal" (if icon-only)
- ARIA expanded: "false" (default), "true" (when menu open)

Form input:
- Label: Associated via for/id
- ARIA required: "true"
- ARIA invalid: "true" (when error)
- ARIA describedby: Link to error message ID

Modal:
- Role: dialog
- ARIA modal: "true"
- ARIA labelledby: Link to modal title ID
- Focus trap: First focusable element on open
```

### Live Regions

For dynamic content updates:

```html
aria-live="polite" → Announce when convenient (notifications)
aria-live="assertive" → Announce immediately (errors, alerts) aria-atomic="true"
→ Read entire region on change
```

**In prompts, specify:**

```
Toast notification:
- Role: status or alert
- ARIA live: "polite" (success) or "assertive" (error)
- ARIA atomic: "true"
- Message: Clear, actionable text

Loading indicator:
- ARIA live: "polite"
- ARIA busy: "true" (during load), "false" (after)
- Message: "Loading data, please wait"

Form validation:
- ARIA live: "assertive" (for errors)
- Linked via aria-describedby to input
```

---

## Semantic HTML

### Use Correct Elements

❌ **Bad:**

```html
<div onclick="submit()">Submit</div>
<span class="heading">Title</span>
<div class="link">Click here</div>
```

✅ **Good:**

```html
<button type="submit">Submit</button>
<h2>Title</h2>
<a href="/page">View details</a>
```

### Heading Hierarchy

```
<h1> - Page title (one per page)
  <h2> - Main sections
    <h3> - Subsections
      <h4> - Sub-subsections
```

**In prompts, specify:**

```
Typography hierarchy:
- Page title: <h1>, type-scale-8 (48px)
- Section headings: <h2>, type-scale-6 (32px)
- Card titles: <h3>, type-scale-5 (24px)
- Subsections: <h4>, type-scale-4 (20px)

Note: Do not skip levels (no h1 → h3)
```

---

## Forms

### Labels

- [ ] Every input has associated label
- [ ] Use `<label for="id">` or wrap input
- [ ] Placeholder is NOT a substitute for label

**In prompts, specify:**

```
Text input:
- Label: <label for="email">Email address</label>
  - Typography: type-scale-3, weight-medium, neutral-700
  - Position: Above input, margin-bottom spacing-xs
- Input: id="email", aria-required="true"
- Required indicator: Red asterisk (*), aria-label="required"
- Help text: aria-describedby="email-help"
  - ID: "email-help"
  - Text: "We'll never share your email"
```

### Error Messages

- [ ] Visible and programmatically linked (aria-describedby)
- [ ] Clear, specific, actionable
- [ ] Announced to screen readers (aria-live)

**In prompts, specify:**

```
Error state:
- Input: aria-invalid="true", aria-describedby="email-error"
- Error message:
  - ID: "email-error"
  - Role: alert (or aria-live="assertive")
  - Text: "Please enter a valid email address (example@domain.com)"
  - Icon: Error icon with aria-hidden="true" (decorative)
  - Color: error-600, meets contrast requirements
```

### Required Fields

```
Method 1: Asterisk
- Visual: Red * next to label
- Hidden text: <span class="sr-only">required</span>
- ARIA: aria-required="true" on input

Method 2: Text indicator
- Visual: "(required)" next to label
- Color: error-600 or neutral-600
- ARIA: aria-required="true" on input
```

---

## Interactive Elements

### Buttons

**In prompts, specify:**

```
Button:
- Element: <button> (not <div> or <a>)
- Type: "button" (default), "submit" (forms), "reset"
- Text: Descriptive ("Save changes" not "Submit")
- Icon-only: aria-label="Close modal"
- Disabled: disabled attribute + aria-disabled="true"
- Loading: aria-busy="true", text "Loading..."

Touch target:
- Min size: 44px × 44px (mobile)
- Padding: Sufficient for target size
- Spacing: Min 8px between targets
```

### Links

**In prompts, specify:**

```
Link:
- Element: <a href="...">
- Text: Descriptive ("View product details" not "Click here")
- External: aria-label="Opens in new tab" if target="_blank"
- Icon: Decorative icons aria-hidden="true"
- Visited: Different color (but maintain contrast)

Underline:
- Default: Underline or other non-color indicator
- Hover: Additional styling OK
- Color alone: Insufficient for accessibility
```

### Modals/Dialogs

**In prompts, specify:**

```
Modal:
- Container: role="dialog", aria-modal="true"
- Title: aria-labelledby="modal-title-id"
- Close button: aria-label="Close", first or last focusable element

Focus management:
- On open: Focus first element (close button or first input)
- During: Trap focus within modal
- On close: Return focus to trigger element

Keyboard:
- Escape: Close modal
- Tab: Navigate within modal (trap)

Backdrop:
- Visual: bg-black, opacity-50
- Click: Close modal (announce to screen reader)
- Inert: Content behind modal not interactive
```

---

## Images & Media

### Images

**In prompts, specify:**

```
Decorative images:
- Alt: alt="" (empty, not omitted)
- ARIA: aria-hidden="true"

Informative images:
- Alt: Descriptive text (what's in image, its purpose)
- Length: Concise (< 125 characters if possible)

Complex images (charts, diagrams):
- Alt: Brief description
- Long description: aria-describedby to detailed text or <details>

Image buttons:
- Alt: Action ("Delete item" not "Trash icon")
```

### Video/Audio

**In prompts, specify:**

```
Video:
- Captions: For all speech and sound effects
- Transcript: Full text alternative
- Controls: Keyboard accessible, labeled

Audio:
- Transcript: Full text alternative
- Controls: Keyboard accessible, labeled

Autoplay:
- Avoid if possible
- If necessary: Muted, pause button, respects prefers-reduced-motion
```

---

## Motion & Animation

### Reduced Motion

**In prompts, specify:**

```
Animation:
- Default: Full animation (duration-base, easing-smooth)
- Reduced motion: Instant or subtle fade only
  - Media query: @media (prefers-reduced-motion: reduce)
  - Duration: duration-instant (0ms) or duration-fast (150ms max)
  - Transform: None or minimal
  - Effect: Fade only (opacity changes OK)

Example:
Button hover:
- Default: Elevate 4px, shadow-lg, transition 300ms
- Reduced motion: Shadow-lg, transition 0ms (instant)
```

### Animation Guidelines

- [ ] Not sole indicator of action (provide text/color)
- [ ] Can be paused (if looping/long duration)
- [ ] No more than 3 flashes per second (seizure risk)
- [ ] Respects prefers-reduced-motion

---

## Mobile & Touch

### Touch Targets

**In prompts, specify:**

```
All interactive elements:
- Min size: 44px × 44px (WCAG 2.1 AAA) or 48px × 48px (Material Design)
- Spacing: Min 8px between targets
- Padding: Add padding if visual smaller than target

Small elements:
- Button text: 16px, padding-md (16px) = 48px height ✅
- Icon-only: 24px icon, padding spacing-sm (12px) = 48px ✅
- Link in text: Increase line height and padding
```

### Gestures

- [ ] All actions available via tap (no swipe-only)
- [ ] Complex gestures have alternatives
- [ ] Pinch-to-zoom not disabled (unless app-specific reason)

---

## Color & Visual Design

### Don't Rely on Color Alone

❌ **Bad:**

```
Error: Red border only
Success: Green background only
Required: Red asterisk only (no label)
```

✅ **Good:**

```
Error: Red border + error icon + error message
Success: Green background + checkmark + "Success!" text
Required: Red asterisk + aria-required="true" + "required" text
```

### Text on Images

- [ ] Sufficient contrast maintained
- [ ] Overlay if needed (bg-black, opacity-50)
- [ ] Alternative if contrast can't be achieved

**In prompts, specify:**

```
Hero with background image:
- Overlay: bg-black, opacity-60 (creates 8:1 contrast for white text)
- Text: white, weight-bold, shadow-lg (additional readability)
- Alt: Ensure content understandable without image
```

---

## Common Patterns

### Skip Links

**In prompts, specify:**

```
Skip link:
- Position: First focusable element in <body>
- Text: "Skip to main content"
- Href: #main (link to main content ID)
- Visibility: Hidden by default, visible on focus
- Style:
  - Default: position absolute, left -9999px OR opacity-0, pointer-events-none
  - Focus: position absolute, top 0, left 0, z-index z-tooltip (1070), bg-primary-500, color white, padding-sm, radius-md
```

### Breadcrumbs

**In prompts, specify:**

```
Breadcrumbs:
- Container: <nav aria-label="Breadcrumb">
- List: <ol> (ordered list)
- Items: <li>
- Current page: aria-current="page"
- Separator: aria-hidden="true" (decorative)

Example:
<nav aria-label="Breadcrumb">
  <ol>
    <li><a href="/">Home</a></li>
    <li><a href="/products">Products</a></li>
    <li aria-current="page">Item Name</li>
  </ol>
</nav>
```

### Tabs

**In prompts, specify:**

```
Tabs:
- Tab list: role="tablist"
- Each tab: role="tab", aria-selected="true/false", aria-controls="panel-id"
- Panel: role="tabpanel", aria-labelledby="tab-id"
- Keyboard:
  - Arrow left/right: Navigate between tabs
  - Tab: Move to panel content
  - Space/Enter: Activate tab

Active tab:
- aria-selected="true"
- Distinct visual (primary-500 border, bold text)
- Panel: Not hidden

Inactive tabs:
- aria-selected="false"
- Panel: hidden attribute
```

### Carousels

**In prompts, specify:**

```
Carousel:
- Container: role="region", aria-label="Featured items"
- Auto-play: Avoid or provide pause button
- Pause button: aria-label="Pause carousel"
- Navigation:
  - Prev/Next: aria-label="Previous slide" / "Next slide"
  - Indicators: role="group", aria-label="Slides"
  - Current: aria-current="true"
- Keyboard:
  - Arrow left/right: Navigate slides
  - Tab: Move to controls then content
- Screen reader: Announce current slide ("Slide 2 of 5")
```

---

## Testing Checklist

### Quick Manual Tests

1. **Keyboard only:** Can you complete all tasks?
2. **Screen reader:** Is content announced correctly?
3. **200% zoom:** Does layout still work?
4. **Contrast:** Check with browser DevTools or contrast checker
5. **Color blind:** Use color blind simulation tool
6. **Reduced motion:** Test with OS setting enabled

### Automated Testing

- axe DevTools (browser extension)
- Lighthouse (Chrome DevTools)
- WAVE (web accessibility evaluation tool)
- Pa11y (command-line tool)

### Screen Reader Testing

- NVDA (Windows, free)
- JAWS (Windows, paid)
- VoiceOver (macOS/iOS, built-in)
- TalkBack (Android, built-in)

---

## In Prompts: Accessibility Shorthand

For efficiency in prompts, use this shorthand:

```
[Component Name] - Accessibility:
- Semantic: <button>, <nav>, <main> (appropriate HTML)
- Keyboard: Tab order logical, Enter/Space activates, Escape closes
- Focus: 3px outline, primary-500, offset 2px
- ARIA: [specific attributes for this component]
- Contrast: All text/UI 4.5:1 minimum
- Touch: 44px minimum targets, 8px spacing
- Motion: Respects prefers-reduced-motion
- Screen reader: [announce behavior]
```

Then expand critical sections as needed for complexity.

---

## Resources

- WCAG 2.1 Guidelines: https://www.w3.org/WAI/WCAG21/quickref/
- ARIA Authoring Practices: https://www.w3.org/WAI/ARIA/apg/
- WebAIM Contrast Checker: https://webaim.org/resources/contrastchecker/
- A11y Project Checklist: https://www.a11yproject.com/checklist/

Use these guidelines in every UI prompt to ensure inclusive, accessible designs.
