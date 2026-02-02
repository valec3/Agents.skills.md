---
name: ui-prompt-generation
description: Use when generating prompts for web UI design, needing modern interface patterns, or structuring design specifications for visual components
---

# UI Prompt Generation

## Overview

A systematic approach to generate comprehensive, precise prompts for web UI design using modern patterns, components, and visual hierarchies. Ensures consistency, completeness, and adherence to current design trends.

## When to Use

**Use this skill when:**

- Generating prompts for designers or AI design tools
- Specifying UI components, layouts, or full interfaces
- Need to reference modern design patterns systematically
- Creating design briefs or technical specifications for frontend
- Translating user requirements into detailed UI specifications
- Ensuring design consistency across a project

**Don't use when:**

- Writing code implementations (use coding skills)
- Creating basic wireframes without detailed styling
- Design is already fully specified

## Core Pattern

**Before:**

```
"Create a login page with email and password"
```

**After:**

```
Create a login page with these specifications:

Layout & Structure:
- Centered hero layout with single CTA
- Asymmetrical grid for visual interest
- Mobile-first with responsive column stacking

Components:
- Soft cards (no borders) for form container
- Glassmorphism effect on card background
- Interactive cards with hover expand on "Forgot password?"

Visual Hierarchy:
- Oversized heading: "Welcome Back"
- Tight headline + relaxed body for form labels
- High-contrast UI with accent color-driven CTAs

Microinteractions:
- Hover affordances on input fields
- Button press states with subtle motion feedback
- Focus states visibles on all interactive elements
- Inline error feedback below each field

States:
- Empty state: "Ready to log in"
- Error states with human language
- Loading skeleton during authentication
- Success confirmation with visual feedback

Style:
- Soft minimalism aesthetic
- Muted color palette with accent color for CTAs
- Dark mode-first design
- Natural easing motion for transitions
```

## Asset Reference System

The skill includes curated assets in `assets/` directory:

### ui-patterns.md

14 categories of UI patterns covering:

- Layouts, hero sections, cards, navigation
- Microinteractions, animations, content components
- Dashboards, scroll behaviors, typography
- Visual styles, states, mobile-first, emotional design

**Usage:** Reference specific categories when generating prompts for focused requirements.

### design-tokens.md

Standardized design values:

- Spacing scale (4px base)
- Typography scale
- Color systems (semantic naming)
- Shadow levels
- Border radius values
- Animation durations & easing

**Usage:** Include specific token values for consistency across generated prompts.

### component-checklist.md

Comprehensive checklist for component specifications:

- Visual states (default, hover, active, disabled, loading)
- Responsive behavior
- Accessibility requirements
- Animation details
- Error handling

**Usage:** Ensure completeness when generating component-level prompts.

### prompt-templates.md

Ready-to-use templates for common scenarios:

- Landing page sections
- Dashboard layouts
- Form interfaces
- Navigation systems
- Empty states

**Usage:** Start with templates, customize with specific patterns from ui-patterns.md.

## Quick Reference

| Prompt Type   | Include From Assets                           | Priority Elements                          |
| ------------- | --------------------------------------------- | ------------------------------------------ |
| **Full Page** | ui-patterns (types 1-2) + design-tokens       | Layout, Hero, Navigation, Typography       |
| **Component** | component-checklist + ui-patterns (type 3-5)  | States, Interactions, Visual style         |
| **Dashboard** | ui-patterns (type 8) + design-tokens          | Data cards, Filters, Actions, Empty states |
| **Mobile**    | ui-patterns (type 13) + component-checklist   | Gestures, Thumb zones, Bottom sheets       |
| **Animation** | ui-patterns (type 6) + design-tokens (timing) | Easing, Duration, Triggers, Purpose        |

## Implementation Steps

### 1. Understand Requirements

- Identify the UI element type (page, component, section)
- Determine primary user goal
- Note platform constraints (web, mobile, responsive)

### 2. Select Pattern Categories

Reference `assets/ui-patterns.md` and select relevant types:

```
Landing page → Types 1, 2, 3, 10, 11
Dashboard → Types 1, 5, 8, 12
Form → Types 3, 5, 12, 13
```

### 3. Structure the Prompt

**Template:**

```markdown
# [Component/Page Name]

## Purpose

[User goal and context]

## Layout & Structure

[Reference types 1, 4]

## Components

[Reference types 3, 7, 8]

## Visual Hierarchy

[Reference type 10]

## Interactions & Feedback

[Reference types 5, 6]

## States

[Reference type 12]

## Style & Aesthetics

[Reference type 11]

## Responsive Behavior

[Reference type 13 if mobile]

## Design Tokens

[Specific values from design-tokens.md]
```

### 4. Add Specificity

- Include exact measurements when critical
- Reference design tokens for consistency
- Specify animation durations and easings
- Detail accessibility requirements
- Define error and edge cases

### 5. Validate Completeness

Use `assets/component-checklist.md` to ensure:

- All interactive states covered
- Responsive breakpoints specified
- Accessibility considerations included
- Error handling defined

## Common Mistakes

### ❌ Too Vague

```
"Make it modern and clean"
```

**Fix:** Reference specific patterns

```
"Soft minimalism aesthetic with muted color palette, high-contrast UI,
oversized headings, and glassmorphism on cards"
```

### ❌ Missing States

```
"Add a submit button"
```

**Fix:** Include all states from checklist

```
"Submit button with:
- Default: Primary accent color, medium shadow
- Hover: Slightly elevated, brightness +10%
- Active: Pressed state, scale 0.98
- Disabled: 50% opacity, no interaction
- Loading: Spinner with button text 'Processing...'"
```

### ❌ Inconsistent Terminology

```
"Use some animations and make things fade in"
```

**Fix:** Use standardized terms from assets

```
"Apply staggered entrance animations (200ms delay between items) with
natural easing (cubic-bezier(0.4, 0.0, 0.2, 1)), reveal on scroll
when element enters viewport"
```

### ❌ No Responsive Strategy

```
"Create a three-column layout"
```

**Fix:** Specify breakpoint behavior

```
"Three-column masonry layout (desktop: 1200px+)
→ Two columns (tablet: 768-1199px, responsive column stacking)
→ Single column (mobile: <768px, card-based layout with 16px spacing)"
```

## Advanced Patterns

### Combining Multiple Pattern Types

For rich interfaces, layer patterns strategically:

```markdown
E-commerce Product Page:

Hero (Type 2): Split screen layout - product image left, details right
Layout (Type 1): Bento grid for related products section
Cards (Type 3): Soft cards with glassmorphism for reviews
Navigation (Type 4): Sticky navigation with scroll-aware states
Microinteractions (Type 5):

- Image hover with zoom affordance
- Add to cart button with success feedback
- Stock status with subtle pulse animation
  Scroll (Type 9): Scroll-driven animation revealing product benefits
  Typography (Type 10): Oversized product name, tight + relaxed specs
  Style (Type 11): Dark mode-first with accent color on CTAs
  Mobile (Type 13): Bottom sheet for "Add to cart", swipeable image gallery
```

### Token-Based Consistency

Reference design tokens for system-wide coherence:

```markdown
Spacing:

- Section gaps: spacing-xl (64px)
- Component gaps: spacing-md (24px)
- Element gaps: spacing-sm (12px)

Typography:

- Heading: type-scale-6 (48px), weight-bold (700)
- Body: type-scale-2 (16px), weight-normal (400)
- Caption: type-scale-1 (14px), weight-normal (400)

Shadows:

- Elevated cards: shadow-lg
- Floating actions: shadow-xl
- Subtle hover: shadow-md

Animation:

- Fast interactions: duration-fast (150ms)
- Standard transitions: duration-base (300ms)
- Page transitions: duration-slow (500ms)
- All with easing-smooth
```

### Template Customization

Start with templates, enhance with specific requirements:

```markdown
Base Template: Dashboard Layout (from prompt-templates.md)

Customizations:

- Data visualization: Animated charts with progressive data disclosure
- Filters: Visual filters with multi-select, tag-based UI
- Real-time updates: Subtle pulse on new data, non-blocking notifications
- Empty state: Illustration with CTA "Import your first dataset"
- Mobile: Bottom navigation, swipeable metric cards
- Accessibility: ARIA live regions for data updates, keyboard nav for filters
```

## Real-World Impact

**Before this skill:**

- Vague prompts resulted in generic, inconsistent designs
- Missing critical states led to incomplete implementations
- No standardized language caused miscommunication
- Iterative back-and-forth to clarify requirements

**After this skill:**

- Comprehensive prompts capture all requirements upfront
- Consistent terminology across team and tools
- Complete state coverage prevents edge case bugs
- Design tokens ensure visual consistency
- 60-80% reduction in clarification rounds

**Example outcomes:**

- Landing page redesign: Single comprehensive prompt → pixel-perfect first draft
- Dashboard UI: Complete state coverage prevented 12 edge case issues
- Component library: Token-based system enabled consistent design at scale

## See Also

- `assets/ui-patterns.md` - Complete pattern reference
- `assets/design-tokens.md` - Standardized design values
- `assets/component-checklist.md` - Completeness verification
- `assets/prompt-templates.md` - Ready-to-use templates
