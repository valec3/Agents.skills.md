# UI Prompt Examples

Real-world examples demonstrating the ui-prompt-generation skill in action. Use these as reference for quality and completeness.

---

## Example 1: E-commerce Product Card

### Simple (Before Skill)

```
Create a product card with image, title, price, and add to cart button.
```

### Comprehensive (After Skill)

```markdown
# E-commerce Product Card

## Purpose

Display product information and enable quick add-to-cart action in grid layout.

## Layout & Structure (Tipo 3)

Container:

- Background: white (light mode), neutral-900 (dark mode)
- Border: 1px solid neutral-200 (light), neutral-700 (dark)
- Border radius: radius-lg (12px)
- Padding: 0 (image full-bleed), spacing-lg (24px) for content area
- Shadow: shadow-md (default), shadow-xl (hover)
- Min height: 420px
- Aspect ratio: 3:4 overall card

## Components

### Product Image

- Position: Top, full width
- Aspect ratio: 1:1
- Object fit: Cover
- Border radius: radius-lg radius-lg 0 0 (top corners only)
- Placeholder: neutral-200 bg, icon (shopping bag, 48px, neutral-400)
- Hover: Scale 1.05, transition duration-base (300ms)

### Badge (Sale/New)

- Position: Absolute, top-right, spacing-sm (8px) inset
- Background: error-500 (sale) or success-500 (new)
- Text: type-scale-1 (12px), weight-bold, white, uppercase
- Padding: spacing-xs vertical, spacing-sm horizontal
- Border radius: radius-sm (4px)
- Shadow: shadow-md

### Content Area

Padding: spacing-lg (24px)

Category:

- Typography: type-scale-2 (14px), weight-medium, neutral-500, uppercase
- Letter spacing: 0.05em
- Margin bottom: spacing-xs (4px)

Title:

- Typography: type-scale-4 (20px), weight-semibold (600), neutral-900
- Line clamp: 2 lines, ellipsis
- Margin bottom: spacing-sm (8px)
- Hover: Color primary-500, transition duration-fast

Rating:

- Layout: Horizontal, stars + count
- Stars: 5 star icons, 16px, warning-500 (filled), neutral-300 (empty)
- Count: type-scale-2 (14px), neutral-600, "(127 reviews)"
- Margin bottom: spacing-md (16px)

Price:

- Layout: Horizontal, current + original if on sale
- Current: type-scale-5 (24px), weight-bold (700), neutral-900
- Original (sale): type-scale-3 (16px), weight-normal, neutral-500, strikethrough
- Save amount: type-scale-2, error-600, "Save $20"
- Margin bottom: spacing-md (16px)

### Action Buttons

Layout: Horizontal row, spacing-sm gap

Add to Cart:

- Style: Primary button
- Background: primary-500, hover: primary-600, active: primary-700
- Text: type-scale-3 (16px), weight-semibold, "Add to Cart"
- Icon: Shopping cart, 18px, left side
- Padding: spacing-sm vertical, spacing-lg horizontal
- Border radius: radius-md (8px)
- Full width: On mobile
- Loading: Spinner + "Adding...", disabled

Wishlist:

- Style: Outline button (icon-only)
- Border: 2px neutral-300, hover: primary-500
- Icon: Heart, 20px, neutral-600, hover/active: primary-500 (filled)
- Size: 40px × 40px (square)
- Border radius: radius-md
- ARIA label: "Add to wishlist"

## Interactive States (Tipo 5)

Default:

- Shadow: shadow-md
- Image: Normal scale

Hover (desktop):

- Container: translateY(-8px), shadow-xl, transition duration-base (300ms)
- Image: Scale 1.05
- Title: Color primary-500
- Add to Cart: Background primary-600, shadow-lg

Active:

- Container: translateY(-4px), scale 0.99
- Shadow: shadow-lg

Focus:

- Outline: 3px solid primary-500 with opacity-50
- Outline offset: 2px

Loading (Add to Cart):

- Button: Spinner (primary-500 on white), text "Adding...", disabled
- Pointer events: none on entire card

Success (Added to Cart):

- Button: Background success-500, text "Added!", checkmark icon
- Duration: 2 seconds, then revert
- Toast: "Product added to cart" notification

Error (Out of Stock):

- Badge: "Out of Stock", neutral-500 bg
- Add to Cart: Replaced with "Notify Me" button, secondary variant
- Price: Opacity opacity-50

## Responsive (Tipo 13)

Desktop (1024px+):

- Grid: 4 columns, spacing-lg (24px) gap
- Hover effects: Enabled
- Image aspect: 1:1

Tablet (640-1024px):

- Grid: 3 columns, spacing-md (16px) gap
- Image aspect: 1:1

Mobile (< 640px):

- Grid: 2 columns, spacing-sm (8px) gap
- Padding: spacing-md (16px)
- Title: type-scale-3 (16px), 2 lines
- Price: type-scale-4 (20px)
- Add to Cart: Full width, spacing-sm padding
- Wishlist: Top-right absolute position, overlay on image

## Accessibility

- Heading: Title is H3
- Link: Entire card clickable (to product page), title is link text
- Button: "Add to Cart" separate button, doesn't trigger card link
- ARIA:
  - Card: role="article"
  - Wishlist: aria-label="Add [product name] to wishlist"
  - Rating: aria-label="Rated 4.5 out of 5 stars, 127 reviews"
- Keyboard: Tab to card (outline), Enter opens product, Tab to buttons
- Focus: Visible on card and buttons

## Animation (Tipo 6)

Entrance (grid):

- Type: Fade + slide up
- Duration: duration-base (300ms)
- Delay: Staggered (50ms per card, max 300ms)
- Trigger: On scroll into viewport
- Easing: easing-smooth

Hover transition:

- Properties: transform, box-shadow
- Duration: duration-base (300ms)
- Easing: easing-smooth

Add to Cart feedback:

- Type: Button background color change
- Duration: duration-fast (150ms)
- Success: Scale 1.05 → 1, duration-base

## Style (Tipo 11)

- Aesthetic: Soft minimalism
- Image treatment: Full-bleed, slight zoom on hover
- Elevation: Progressive (hover elevates significantly)
- Colors: Minimal, product image dominant, accent on CTA
```

**Token efficiency:** ~450 words. Complete specification for production-ready component.

---

## Example 2: Mobile Navigation Bottom Sheet

### Simple (Before Skill)

```
Create a mobile bottom navigation with 4 icons.
```

### Comprehensive (After Skill)

```markdown
# Mobile Bottom Navigation

## Purpose

Provide thumb-friendly primary navigation for mobile users (< 640px only).

## Layout & Structure (Tipo 4, 13)

Container:

- Position: Fixed bottom, full width (100vw)
- Background: white (light mode), neutral-900 (dark mode)
- Height: 72px (includes safe area)
- Padding: spacing-sm (8px) top, max(spacing-sm, env(safe-area-inset-bottom)) bottom
- Border top: 1px solid neutral-200 (light), neutral-700 (dark)
- Shadow: shadow-xl (upward shadow: 0 -4px 12px rgba(0,0,0,0.1))
- Z-index: z-sticky (1020)

Navigation Items:

- Layout: Horizontal flex, space-evenly, 4 items
- Width: Each item 25% (4 items) or 20% (5 items)

## Individual Item

Structure:

- Layout: Vertical flex, centered
- Padding: spacing-sm (8px) vertical
- Touch target: Full item area, min 48px height
- Cursor: pointer

Icon:

- Size: 24px
- Color: neutral-600 (inactive), primary-500 (active)
- Margin bottom: spacing-xs (4px)

Label:

- Typography: type-scale-1 (12px), weight-medium (500)
- Color: neutral-600 (inactive), primary-500 (active)
- Text align: center
- Line height: 1.2

## Navigation Items Content

Item 1 - Home:

- Icon: Home icon
- Label: "Home"
- Link: "/"

Item 2 - Explore:

- Icon: Compass icon
- Label: "Explore"
- Link: "/explore"

Item 3 - Create:

- Icon: Plus icon
- Label: "Create"
- Action: Opens bottom sheet modal (not link)
- Special: Larger icon (28px), elevated button (circular bg)

Item 4 - Notifications:

- Icon: Bell icon
- Label: "Notices"
- Link: "/notifications"
- Badge: Red dot (8px, error-500) if unread count > 0
  - Position: Absolute, top-right of icon
  - With count: 16px circle, white text, type-scale-1
  - Max display: "9+" for counts ≥ 10

Item 5 - Profile:

- Icon: User avatar (24px circle)
- Label: "Profile"
- Link: "/profile"
- Active indicator: 2px border, primary-500

## Interactive States (Tipo 5)

Inactive:

- Icon: neutral-600
- Label: neutral-600
- Background: transparent

Active:

- Icon: primary-500
- Label: primary-500, weight-semibold (600)
- Indicator: 3px height bar above item, primary-500, full width
- Animation: Fade in, duration-fast (150ms)

Tap:

- Scale: 0.95
- Duration: duration-fast (150ms)
- Feedback: Haptic vibration (if supported)

Focus (keyboard nav):

- Outline: 3px solid primary-500 with opacity-50
- Inset: Yes (within item bounds)

Disabled:

- Opacity: opacity-50
- Cursor: not-allowed
- No interaction

## Special: Create Button (Elevated)

Style:

- Background: primary-500 circular (48px diameter)
- Icon: Plus, 28px, white
- Position: Slightly elevated (-8px translateY)
- Shadow: shadow-xl
- No label OR label below in smaller text

Tap:

- Scale: 0.9
- Shadow: shadow-lg
- Opens: Bottom sheet modal with create actions

## Bottom Sheet Modal (for Create)

Trigger: Tap Create button

Sheet:

- Background: white (light), neutral-900 (dark)
- Border radius: radius-2xl radius-2xl 0 0 (top corners)
- Padding: spacing-xl (32px)
- Max height: 80vh
- Shadow: shadow-2xl
- Animation: Slide up from bottom, duration-base (300ms)

Backdrop:

- Background: bg-black, opacity-50
- Click: Close sheet
- Z-index: z-overlay (1030)

Handle:

- Width: 48px
- Height: 4px
- Background: neutral-300
- Border radius: radius-full
- Position: Top center, spacing-md from top
- Purpose: Visual affordance for dragging

Content:

- Heading: "Create new", type-scale-5, weight-semibold
- Actions: List of buttons (photo, video, text post, etc.)
- Close: X button, top-right

Gesture:

- Swipe down: Close sheet
- Drag handle: Visual feedback during drag

## Responsive

Show when:

- Viewport width: < 640px (mobile only)

Hide when:

- Viewport width: ≥ 640px (use top navigation instead)
- Display: none at breakpoint-sm (640px)

Safe Areas:

- Bottom padding: max(spacing-sm, env(safe-area-inset-bottom))
- Purpose: iPhone notch/gesture bar clearance

## Accessibility

Keyboard:

- Tab: Navigate items left to right
- Shift+Tab: Navigate right to left
- Enter/Space: Activate item
- Focus: Visible outline

ARIA:

- Container: <nav aria-label="Primary navigation">
- Items: <a> or <button> (semantic HTML)
- Active: aria-current="page"
- Badge: aria-label="5 unread notifications"

Screen Reader:

- Announce: "Primary navigation"
- Items: "Home, current page" or "Notifications, 5 unread"
- Create: "Create new post, button, opens menu"

Touch:

- Targets: Full item area, 48px+ height ✅
- Spacing: Items separated, no accidental taps
- Feedback: Haptic + visual (scale)

## Animation (Tipo 6)

Item activation:

- Active indicator: Slide in from center, duration-fast
- Icon/label color: Fade transition, duration-fast
- Scale: 0.95 on tap, duration-fast, easing-smooth

Bottom sheet:

- Enter: translateY(100%) → translateY(0), duration-base
- Exit: translateY(0) → translateY(100%), duration-base
- Backdrop: opacity 0 → 0.5, duration-base
- Easing: easing-smooth

Reduced motion:

- Item activation: Instant color change, no scale
- Sheet: Fade in/out, duration-fast (150ms)

## States (Tipo 12)

Loading (initial):

- Show skeleton: 4 neutral-200 circles + rectangles
- Duration: < 500ms, avoid showing for quick loads

Offline:

- Indicator: Small offline badge, top of navigation
- Text: "Offline", type-scale-1, neutral-600
- Links: Disabled or cached-only navigation

Error (link failure):

- Toast: "Can't navigate right now", error-50 bg
- Duration: 3 seconds
- Don't disable navigation (allow retry)

## Style (Tipo 11)

- Aesthetic: Soft minimalism, icon-first
- Colors: Neutral base, primary accent for active
- Shadows: Upward shadow for floating appearance
- Spacing: Generous touch targets, clear separation

## Notes

- Always visible on mobile (never scrolls away)
- Consider 5th item carefully (usability research shows 4 is optimal)
- Test on devices with notches/gestures (iPhone, Android gesture nav)
```

**Token efficiency:** ~550 words. Complete mobile-specific component specification.

---

## Example 3: Dashboard KPI Card (Concise)

### Using Shorthand for Efficiency

```markdown
# Dashboard KPI Card

## Purpose

Display single metric with trend indicator and sparkline chart.

## Structure (Tipo 8 - Data cards)

- Card: Soft card, padding-lg, radius-lg, shadow-md hover: shadow-lg
- Layout: Vertical stack, spacing-md gaps
- Min height: 140px

## Content

Label: type-scale-2, neutral-600, weight-medium, "Total Revenue"
Value: type-scale-8 (48px), weight-bold, neutral-900, "$12,450"
Change:

- Badge: +12.3%, type-scale-2, weight-semibold
- Success (positive): success-50 bg, success-700 text, ↑ icon
- Error (negative): error-50 bg, error-700 text, ↓ icon
  Sparkline:
- 40px height, neutral-400 line, success-500 fill (positive trend)
- Tooltip on hover: Show exact value, shadow-xl

## States

- Loading: Skeleton (neutral-200 shimmer)
- Error: "Data unavailable", error icon, neutral-600, "Retry" link
- No change: Badge neutral-100 bg, neutral-700 text, "—" instead of arrow

## Responsive

- Desktop: 25% width (4 columns)
- Tablet: 50% width (2 columns)
- Mobile: 100% width, type-scale-7 (40px) value

## Accessibility

- Heading: Label is H3
- ARIA: Value has aria-live="polite" for updates
- Change: aria-label="Increased by 12.3 percent"
- Chart: aria-label="Revenue trend: increasing"

## Animation

- Entrance: Fade + slide up, staggered (100ms delay between cards)
- Value update: Count up animation, duration-slow (500ms), easing-smooth
- Hover: Elevate 4px, duration-fast

Tokens: spacing-md, type-scale-8, shadow-md, success-500, neutral-600, radius-lg, duration-fast
```

**Token efficiency:** ~180 words. Concise yet complete for simple component.

---

## Key Patterns Demonstrated

### Pattern 1: Progressive Detail

Start with **purpose**, add **structure**, specify **content**, define **states**, ensure **accessibility**.

### Pattern 2: Token References

Consistently use design tokens: `spacing-md (16px)`, `type-scale-5 (24px)`, `primary-500`, `duration-base (300ms)`.

### Pattern 3: State Coverage

Always include: default, hover, active, focus, disabled, loading, error, success, empty.

### Pattern 4: Responsive Strategy

Specify breakpoint behaviors: desktop, tablet, mobile with different layouts/sizes.

### Pattern 5: Accessibility Integration

Not afterthought - integrated throughout: semantic HTML, ARIA, keyboard, screen reader, touch targets.

### Pattern 6: Animation Specification

Always include: duration, easing, properties, trigger, reduced-motion alternative.

---

## Anti-Patterns (What NOT to Do)

### ❌ Vague Specifications

```
"Make it look good"
"Use nice colors"
"Add some animations"
```

### ❌ Missing States

```
# Button
- Background: blue
- Text: white
- Padding: 16px
```

(Where are hover, focus, disabled, loading states?)

### ❌ No Measurements

```
"Big heading with small subtext"
"Some spacing between elements"
```

(Specify: type-scale-8 (48px), spacing-lg (24px))

### ❌ Color Without Contrast

```
"Light gray text on white background"
"Blue on blue gradient"
```

(Check contrast ratios, specify tokens)

### ❌ Desktop-Only Thinking

```
"4-column grid with sidebar"
```

(What happens on mobile? Specify responsive behavior)

### ❌ No Accessibility

```
"Icon-only button"
"Click here link"
"Auto-playing video"
```

(Add aria-label, descriptive text, controls)

---

## Prompt Quality Spectrum

### Level 1: Minimal (Unusable)

```
"Create a button"
```

### Level 2: Basic (Incomplete)

```
"Create a blue button that says 'Submit' with rounded corners"
```

### Level 3: Structured (Better)

```
"Submit button:
- Background: primary-500
- Text: white, 16px, semibold
- Padding: 12px 24px
- Border radius: 8px
- Hover: darker blue"
```

### Level 4: Comprehensive (This Skill)

```
"Submit Button:

Structure:
- Element: <button type="submit">
- Typography: type-scale-3 (16px), weight-semibold (600)
- Padding: spacing-md (16px) vertical, spacing-2xl (48px) horizontal
- Border radius: radius-md (8px)

States:
- Default: bg-primary-500, text white, shadow-md
- Hover: bg-primary-600, shadow-lg, translateY(-2px), duration-fast
- Active: bg-primary-700, scale 0.98
- Focus: 3px outline primary-500 opacity-50, offset 2px
- Disabled: opacity-50, cursor not-allowed, no hover
- Loading: Spinner (white), text 'Submitting...', disabled

Responsive:
- Desktop: inline, auto width
- Mobile: full width (100%)

Accessibility:
- Keyboard: Enter/Space activates
- Screen reader: Announces state changes
- ARIA: aria-busy='true' when loading

Animation:
- Hover: All properties duration-fast (150ms), easing-smooth
- Reduced motion: Instant color change only
```

---

## Usage Tips

1. **Start with template** - Use [prompt-templates.md](./prompt-templates.md)
2. **Add pattern references** - Include tipo numbers from [ui-patterns.md](./ui-patterns.md)
3. **Specify tokens** - Use exact values from [design-tokens.md](./design-tokens.md)
4. **Validate completeness** - Check against [component-checklist.md](./component-checklist.md)
5. **Ensure accessibility** - Reference [accessibility-guidelines.md](./accessibility-guidelines.md)

These examples demonstrate production-ready specifications that eliminate ambiguity and reduce back-and-forth clarification.
