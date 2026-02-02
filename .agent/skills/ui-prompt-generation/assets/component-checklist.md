# Component Specification Checklist

Use this checklist to ensure comprehensive component specifications in UI prompts. Complete coverage prevents missing edge cases and ensures production-ready designs.

---

## Core Component Anatomy

### Visual Structure

- [ ] Container/wrapper specifications
- [ ] Content hierarchy (primary, secondary, tertiary)
- [ ] Icon/image placement and sizing
- [ ] Text content and formatting
- [ ] Spacing (internal padding, external margins)
- [ ] Borders (width, color, style, radius)

### Layout & Positioning

- [ ] Default dimensions (width, height, aspect ratio)
- [ ] Positioning method (relative, absolute, fixed, sticky)
- [ ] Alignment within parent (horizontal, vertical)
- [ ] Content alignment (text, flex, grid)
- [ ] Z-index layering

---

## Interactive States

### Visual States (ALL components)

- [ ] **Default** - Initial appearance
- [ ] **Hover** - Mouse over (desktop only)
- [ ] **Active** - During click/tap
- [ ] **Focus** - Keyboard navigation highlight
- [ ] **Disabled** - Non-interactive state
- [ ] **Loading** - Async operation in progress
- [ ] **Success** - Successful completion
- [ ] **Error** - Invalid or failed state
- [ ] **Warning** - Cautionary state

### Form-Specific States

- [ ] Empty/placeholder
- [ ] Filled/has value
- [ ] Valid/validated
- [ ] Invalid with error message
- [ ] Required indicator
- [ ] Optional indicator (if needed)

### Selection States

- [ ] Unselected
- [ ] Selected/checked
- [ ] Partially selected (indeterminate)
- [ ] Multi-select behavior

---

## Responsive Behavior

### Breakpoint Strategy

- [ ] Mobile (< 640px)
- [ ] Tablet (640-1024px)
- [ ] Desktop (1024px+)
- [ ] Large desktop (1280px+)

### Responsive Adaptations

- [ ] Size adjustments (font, spacing, dimensions)
- [ ] Layout changes (stack, wrap, hide)
- [ ] Content priorities (show/hide elements)
- [ ] Touch target sizes (44px minimum on mobile)
- [ ] Orientation handling (portrait/landscape)

---

## Accessibility

### Keyboard Navigation

- [ ] Tab order logical and clear
- [ ] Focus indicator visible (3px outline minimum)
- [ ] Keyboard shortcuts defined (if applicable)
- [ ] Escape key behavior (for modals/overlays)
- [ ] Enter/Space activation for buttons

### Screen Readers

- [ ] ARIA labels for icons/graphics
- [ ] ARIA roles (button, dialog, alert, etc.)
- [ ] ARIA states (expanded, selected, invalid)
- [ ] Alt text for images
- [ ] Live regions for dynamic content

### Visual Accessibility

- [ ] Color contrast meets WCAG AA (4.5:1 for text)
- [ ] Information not conveyed by color alone
- [ ] Text resizable up to 200%
- [ ] Focus visible without relying on color only
- [ ] Motion can be disabled (prefers-reduced-motion)

---

## Animation & Transitions

### Timing & Easing

- [ ] Duration specified (150ms fast, 300ms standard, 500ms slow)
- [ ] Easing function (easing-smooth default)
- [ ] Delay (if staggered animations)

### Properties Animated

- [ ] Which CSS properties change
- [ ] Transform operations (translate, scale, rotate)
- [ ] Opacity changes
- [ ] Color transitions

### Animation Triggers

- [ ] On mount/entrance
- [ ] On state change
- [ ] On scroll (if scroll-driven)
- [ ] On user interaction
- [ ] On data update

### Motion Considerations

- [ ] Respects prefers-reduced-motion
- [ ] Performance (use transform/opacity for 60fps)
- [ ] Purpose clear (not decorative only)

---

## Content Guidelines

### Text Content

- [ ] Character limits (min/max)
- [ ] Truncation strategy (ellipsis, fade)
- [ ] Multiline behavior
- [ ] Empty content handling
- [ ] Overflow handling

### Images/Media

- [ ] Aspect ratios
- [ ] Fallback/placeholder
- [ ] Loading states
- [ ] Error states (broken image)
- [ ] Lazy loading strategy

---

## Interaction Patterns

### Click/Tap Behavior

- [ ] Single click action defined
- [ ] Double click (if applicable)
- [ ] Long press (mobile)
- [ ] Right click/context menu

### Drag & Drop

- [ ] Draggable indicator
- [ ] Drag preview/ghost
- [ ] Drop zone visual feedback
- [ ] Drop validation

### Gestures (Mobile)

- [ ] Swipe (left, right, up, down)
- [ ] Pinch to zoom
- [ ] Pull to refresh
- [ ] Scroll behavior

---

## Data & State Management

### Data Display

- [ ] Empty state (no data)
- [ ] Zero state (first use)
- [ ] Partial data (incomplete info)
- [ ] Maximum data (overflow handling)
- [ ] Real-time updates

### Error Handling

- [ ] Network error state
- [ ] Validation errors (inline)
- [ ] Server errors (with retry option)
- [ ] Timeout handling
- [ ] Offline state

### Loading Patterns

- [ ] Initial load (skeleton, spinner, placeholder)
- [ ] Lazy load (infinite scroll, pagination)
- [ ] Refresh (pull-to-refresh, button)
- [ ] Background updates (subtle indicators)

---

## Context & Variants

### Size Variants

- [ ] Small (compact, dense layouts)
- [ ] Medium (default)
- [ ] Large (prominent, accessible)

### Style Variants

- [ ] Primary (main action)
- [ ] Secondary (alternative action)
- [ ] Tertiary (subtle action)
- [ ] Ghost (minimal styling)
- [ ] Outline (bordered only)

### Context Variants

- [ ] Default context
- [ ] Success context (green theme)
- [ ] Warning context (yellow theme)
- [ ] Error/danger context (red theme)
- [ ] Info context (blue theme)

---

## Documentation in Prompt

### Complete Example Template

```markdown
[Component Name]

## Visual Structure

- Container: bg-white, radius-lg, shadow-md, padding-lg
- Title: type-scale-5, weight-semibold, neutral-800
- Body: type-scale-3, weight-normal, neutral-600, leading-normal
- Icon: 24px, neutral-500, positioned top-right
- Border: 1px solid neutral-200

## States

Default:

- Appearance: [describe]
- Behavior: [describe]

Hover (desktop):

- Transform: translateY(-4px)
- Shadow: shadow-lg
- Transition: duration-base, easing-smooth

Active:

- Transform: scale(0.98)
- Shadow: shadow-sm

Focus:

- Outline: 3px solid primary-500 with opacity-50
- Outline offset: 2px

Disabled:

- Opacity: opacity-50
- Cursor: not-allowed
- No hover/active states

Loading:

- Spinner: centered, primary-500, 24px
- Text: opacity-50
- Pointer events: none

Error:

- Border: 2px solid error-500
- Icon: error icon, error-600
- Message: type-scale-2, error-600, below component

## Responsive

Mobile (< 640px):

- Width: 100%
- Padding: spacing-md (16px)
- Font size: type-scale-2 (14px)

Tablet (640-1024px):

- Width: 50%
- Padding: spacing-lg (24px)

Desktop (1024px+):

- Width: 33.33%
- Padding: spacing-lg (24px)
- Hover effects: enabled

## Accessibility

- Role: button
- Tab index: 0
- ARIA label: [if icon-only]
- Focus visible: Yes (3px outline)
- Keyboard: Enter/Space activates
- Screen reader: Announces state changes

## Animation

Hover transition:

- Duration: duration-fast (150ms)
- Easing: easing-smooth
- Properties: transform, box-shadow

Entrance animation:

- Type: fade + slide up
- Duration: duration-base (300ms)
- Delay: 0ms (or staggered)

## Content

- Max characters: 100
- Truncation: Ellipsis after 2 lines
- Empty state: "No content available"

## Interactions

- Click: [primary action]
- Right click: [context menu if applicable]
- Swipe (mobile): [dismiss action if applicable]
```

---

## Quick Validation

Before finalizing a component prompt, ask:

1. **Can I see every state?** (hover, active, focus, disabled, loading, error)
2. **Will it work on mobile?** (touch targets, gestures, responsive sizing)
3. **Is it accessible?** (keyboard nav, screen readers, contrast)
4. **What happens when it breaks?** (error states, empty states, overflow)
5. **How does it move?** (animations defined with duration/easing)
6. **What's the context?** (variants, sizes, themes specified)

---

## Common Omissions

### Most Frequently Forgotten

1. **Focus states** - Critical for keyboard navigation
2. **Loading states** - Important for perceived performance
3. **Error states** - Essential for production robustness
4. **Mobile touch targets** - Must be 44px minimum
5. **Animation durations** - Vague "smooth" isn't specific enough
6. **Empty/zero states** - First-time user experience
7. **Disabled state appearance** - Often overlooked
8. **Responsive breakpoint behavior** - Not just "make it responsive"

### Anti-Patterns

❌ "Add hover effect" → Too vague
✅ "Hover: Elevate 4px (translateY(-4px)), shadow-md → shadow-lg, transition duration-base (300ms) easing-smooth"

❌ "Make it work on mobile" → Incomplete
✅ "Mobile (< 640px): Full width, spacing-md padding, type-scale-2 text, 44px min touch target, bottom sheet instead of dropdown"

❌ "Handle errors" → Unspecified
✅ "Error state: 2px error-500 border, error icon (20px, error-600), inline message below (type-scale-2, error-600, 'Please enter a valid email'), shake animation (duration-fast)"

---

## Usage Workflow

1. **Start with structure** - Define visual anatomy
2. **Add all states** - Work through checklist systematically
3. **Specify responsive** - Define breakpoint adaptations
4. **Ensure accessibility** - Keyboard, screen reader, visual
5. **Define animations** - Timing, easing, properties
6. **Document content** - Limits, overflow, empty states
7. **Add interactions** - Click, drag, gestures
8. **Validate completeness** - Use quick validation questions

This checklist transforms vague "create a button" into production-ready component specifications.
