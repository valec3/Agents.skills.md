# Design Tokens Reference

Standardized design values for consistent UI generation. Use these tokens in prompts to ensure system-wide coherence.

---

## Spacing Scale

Base unit: `4px`

```
spacing-xs:   4px   (tight gaps, icon padding)
spacing-sm:   8px   (compact spacing)
spacing-md:   16px  (default element spacing)
spacing-lg:   24px  (comfortable section spacing)
spacing-xl:   32px  (prominent section gaps)
spacing-2xl:  48px  (major section separation)
spacing-3xl:  64px  (hero/landing page spacing)
spacing-4xl:  96px  (maximum section gaps)
```

**Usage:**

```
Component padding: spacing-md (16px)
Card gaps in grid: spacing-lg (24px)
Section separation: spacing-3xl (64px)
```

---

## Typography Scale

Base size: `16px` (body text)
Scale ratio: `1.25` (Major Third)

```
type-scale-1:  12px   (0.75rem)   - Captions, labels, meta
type-scale-2:  14px   (0.875rem)  - Small text, secondary info
type-scale-3:  16px   (1rem)      - Body text (BASE)
type-scale-4:  20px   (1.25rem)   - Large body, subheadings
type-scale-5:  24px   (1.5rem)    - H3, card titles
type-scale-6:  32px   (2rem)      - H2, section headings
type-scale-7:  40px   (2.5rem)    - H1, page titles
type-scale-8:  48px   (3rem)      - Display text
type-scale-9:  64px   (4rem)      - Hero headlines
type-scale-10: 80px   (5rem)      - Oversized display
```

### Font Weights

```
weight-thin:      100
weight-light:     300
weight-normal:    400 (body text default)
weight-medium:    500 (emphasis)
weight-semibold:  600 (subheadings)
weight-bold:      700 (headings)
weight-extrabold: 800 (display text)
weight-black:     900 (hero text)
```

### Line Heights

```
leading-tight:   1.1   (headlines, large display)
leading-snug:    1.3   (subheadings)
leading-normal:  1.5   (body text - default)
leading-relaxed: 1.75  (comfortable reading)
leading-loose:   2.0   (very spacious)
```

**Usage:**

```
Hero headline: type-scale-9 (64px), weight-bold (700), leading-tight (1.1)
Body paragraph: type-scale-3 (16px), weight-normal (400), leading-normal (1.5)
Button text: type-scale-3 (16px), weight-semibold (600)
```

---

## Color System

### Semantic Colors

```css
/* Primary - Brand identity, main CTAs */
primary-50:   #F0F9FF
primary-100:  #E0F2FE
primary-500:  #0EA5E9  (base)
primary-600:  #0284C7  (hover)
primary-700:  #0369A1  (active)
primary-900:  #0C4A6E  (dark mode base)

/* Neutral - Text, backgrounds, borders */
neutral-50:   #FAFAFA  (light mode bg)
neutral-100:  #F5F5F5  (subtle bg)
neutral-200:  #E5E5E5  (borders)
neutral-400:  #A3A3A3  (muted text)
neutral-600:  #525252  (secondary text)
neutral-800:  #262626  (primary text)
neutral-900:  #171717  (dark mode bg)
neutral-950:  #0A0A0A  (deepest dark)

/* Success - Confirmations, positive states */
success-50:   #F0FDF4
success-500:  #22C55E  (base)
success-600:  #16A34A  (hover)

/* Error - Errors, destructive actions */
error-50:     #FEF2F2
error-500:    #EF4444  (base)
error-600:    #DC2626  (hover)

/* Warning - Cautions, alerts */
warning-50:   #FFFBEB
warning-500:  #F59E0B  (base)
warning-600:  #D97706  (hover)

/* Info - Informational states */
info-50:      #EFF6FF
info-500:     #3B82F6  (base)
info-600:     #2563EB  (hover)
```

### Usage Patterns

```
Background (light): neutral-50 or white
Background (dark): neutral-900 or neutral-950
Primary text (light): neutral-800
Primary text (dark): neutral-100
Secondary text (light): neutral-600
Secondary text (dark): neutral-400
Borders (light): neutral-200
Borders (dark): neutral-700
Primary CTA: primary-500, hover: primary-600
Success message: success-500 background, success-700 text
```

---

## Shadows

```css
shadow-sm:  0 1px 2px rgba(0,0,0,0.05)
            /* Subtle depth, small elements */

shadow-md:  0 4px 6px rgba(0,0,0,0.07)
            /* Default card elevation */

shadow-lg:  0 10px 15px rgba(0,0,0,0.1)
            /* Prominent cards, modals */

shadow-xl:  0 20px 25px rgba(0,0,0,0.15)
            /* Floating elements, dropdowns */

shadow-2xl: 0 25px 50px rgba(0,0,0,0.25)
            /* Maximum elevation, hero elements */

shadow-inner: inset 0 2px 4px rgba(0,0,0,0.06)
              /* Pressed/inset appearance */
```

**Usage:**

```
Default card: shadow-md
Hover card: shadow-lg
Floating action button: shadow-xl
Dropdown menu: shadow-xl
Pressed button: shadow-inner
```

---

## Border Radius

```
radius-none:  0px      (sharp corners)
radius-sm:    4px      (subtle rounding)
radius-md:    8px      (standard UI elements)
radius-lg:    12px     (cards, containers)
radius-xl:    16px     (prominent cards)
radius-2xl:   24px     (large containers)
radius-full:  9999px   (pills, circular elements)
```

**Usage:**

```
Buttons: radius-md (8px)
Cards: radius-lg (12px)
Input fields: radius-md (8px)
Avatar: radius-full (circular)
Pill badge: radius-full
```

---

## Animation Durations

```
duration-instant:  0ms      (immediate, no animation)
duration-fast:     150ms    (quick interactions, hovers)
duration-base:     300ms    (standard transitions)
duration-slow:     500ms    (deliberate, prominent changes)
duration-slower:   700ms    (page transitions)
duration-slowest:  1000ms   (storytelling animations)
```

**Usage:**

```
Hover effect: duration-fast (150ms)
State transition: duration-base (300ms)
Modal open/close: duration-slow (500ms)
Page transition: duration-slower (700ms)
```

---

## Easing Functions

```css
easing-linear:     linear
                   /* Constant speed, mechanical */

easing-in:         cubic-bezier(0.4, 0.0, 1.0, 1.0)
                   /* Starts slow, ends fast (entering) */

easing-out:        cubic-bezier(0.0, 0.0, 0.2, 1.0)
                   /* Starts fast, ends slow (exiting) */

easing-in-out:     cubic-bezier(0.4, 0.0, 0.2, 1.0)
                   /* Slow start and end, fast middle */

easing-smooth:     cubic-bezier(0.4, 0.0, 0.2, 1.0)
                   /* Natural motion (RECOMMENDED DEFAULT) */

easing-bounce:     cubic-bezier(0.68, -0.55, 0.265, 1.55)
                   /* Playful overshoot */

easing-spring:     cubic-bezier(0.175, 0.885, 0.32, 1.275)
                   /* Natural spring physics */
```

**Usage:**

```
Default transitions: easing-smooth
Hover effects: easing-out
Modal entrance: easing-in
Modal exit: easing-out
Playful interactions: easing-bounce
```

---

## Z-Index Scale

```
z-base:      0     (default layer)
z-dropdown:  1000  (dropdowns, tooltips)
z-sticky:    1020  (sticky headers)
z-overlay:   1030  (modal overlays)
z-modal:     1040  (modal content)
z-popover:   1050  (popovers above modals)
z-toast:     1060  (notifications)
z-tooltip:   1070  (tooltips - highest)
```

**Usage:**

```
Sticky nav: z-sticky (1020)
Modal backdrop: z-overlay (1030)
Modal content: z-modal (1040)
Toast notification: z-toast (1060)
```

---

## Breakpoints

```
breakpoint-sm:   640px   (mobile landscape, small tablets)
breakpoint-md:   768px   (tablets)
breakpoint-lg:   1024px  (laptops, small desktops)
breakpoint-xl:   1280px  (desktops)
breakpoint-2xl:  1536px  (large desktops)
```

**Mobile-first approach:**

```
Default: Mobile (< 640px)
sm+: Small devices and up
md+: Tablets and up
lg+: Laptops and up
xl+: Desktops and up
```

**Usage:**

```
Single column → Two columns at breakpoint-md (768px)
Two columns → Three columns at breakpoint-lg (1024px)
Collapsed nav → Full nav at breakpoint-lg (1024px)
```

---

## Opacity Scale

```
opacity-0:    0%     (invisible)
opacity-5:    5%     (barely visible)
opacity-10:   10%    (subtle overlay)
opacity-25:   25%    (muted background)
opacity-50:   50%    (half transparent)
opacity-75:   75%    (mostly opaque)
opacity-90:   90%    (near opaque)
opacity-100:  100%   (fully opaque)
```

**Usage:**

```
Modal overlay: bg-black with opacity-50
Disabled state: opacity-50
Glassmorphism: bg-white with opacity-10
Hover state increase: opacity-100 to opacity-90 for images
```

---

## Usage in Prompts

### Example: Complete Button Specification

```
Primary Button Design Tokens:

Typography:
- Size: type-scale-3 (16px)
- Weight: weight-semibold (600)
- Transform: Uppercase

Colors:
- Background: primary-500 (#0EA5E9)
- Hover background: primary-600 (#0284C7)
- Active background: primary-700 (#0369A1)
- Text: white (neutral-50)

Spacing:
- Padding vertical: spacing-sm (8px)
- Padding horizontal: spacing-lg (24px)

Visual:
- Border radius: radius-md (8px)
- Shadow default: shadow-md
- Shadow hover: shadow-lg

Animation:
- Duration: duration-fast (150ms)
- Easing: easing-smooth
- Properties: background-color, box-shadow, transform

States:
- Hover: Lift by 2px, shadow-lg
- Active: Scale 0.98
- Focus: 3px outline, primary-500 with opacity-50
- Disabled: opacity-50, cursor not-allowed
```

### Example: Card Component

```
Card Design Tokens:

Container:
- Background: neutral-50 (light mode), neutral-900 (dark mode)
- Border: 1px solid neutral-200 (light), neutral-700 (dark)
- Border radius: radius-lg (12px)
- Padding: spacing-lg (24px)
- Shadow: shadow-md default, shadow-lg on hover

Typography:
- Title: type-scale-5 (24px), weight-semibold (600), neutral-800
- Body: type-scale-3 (16px), weight-normal (400), neutral-600
- Line height: leading-normal (1.5)

Spacing:
- Title to body: spacing-sm (8px)
- Body to CTA: spacing-md (16px)

Animation:
- Hover transition: duration-base (300ms)
- Easing: easing-smooth
- Transform: translateY(-4px) on hover
```

---

## Token Customization

When tokens don't exist for your specific need:

```
❌ Avoid: Arbitrary values
"Use 23px spacing and #1E40AF color"

✅ Prefer: Nearest token with justification
"Use spacing-lg (24px) for prominent separation,
primary-700 (#0369A1) for high-contrast CTA"

✅ Acceptable: Extend token system
"Add spacing-5xl (128px) for extra-large hero sections,
maintaining 4px base unit"
```

---

## Token Benefits in Prompts

1. **Consistency:** All components use same values
2. **Clarity:** Semantic names communicate intent
3. **Efficiency:** Reference tokens instead of specific values
4. **Maintainability:** Single source of truth for design system
5. **Scalability:** Easy to adjust entire system

Use tokens liberally in prompts for professional, cohesive design specifications.
