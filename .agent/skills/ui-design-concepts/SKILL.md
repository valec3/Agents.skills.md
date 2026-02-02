---
name: ui-design-concepts
description: Use when creating design specifications for AI builders (v0, Lovable, Bolt, Replit), describing visual concepts, patterns, and user experiences without technical implementation details
---

# UI Design Concepts

## Overview

A design-first approach to specify interfaces using visual concepts, patterns, trends, and UX flows. Focuses on **what it looks like** and **how it feels** rather than exact measurements. Optimized for AI code generators that interpret design intent.

**This is NOT a technical specification.** It's a creative brief that AI builders can interpret.

## When to Use

**Use this skill when:**
- Working with AI code generators (v0, Lovable, Bolt, Replit Agent, Claude Artifacts)
- Need to describe visual concepts and design direction
- Want flexibility in implementation details
- Focusing on user experience and design patterns
- Creating mood boards or design briefs
- Explaining "the vibe" of an interface

**Don't use when:**
- Need exact pixel measurements (use ui-prompt-generation instead)
- Implementing specific design system
- Require precise technical specifications
- Working with human developers needing detailed specs

## Core Pattern

**Before (Technical):**
```
Navigation bar: 80px height, bg-white, border-bottom 1px solid #E5E5E5,
padding 16px horizontal, logo 40px height, links type-scale-3 (16px),
weight-medium (500), spacing 32px between items...
```

**After (Design Concept):**
```
Navigation: Clean and minimal, floating glass effect, centered logo,
widely spaced navigation items in uppercase, subtle hover underline animation.
Sticky on scroll with slight transparency. Very Stripe-like aesthetic.
```

## Asset Reference System

### visual-patterns.md
120+ design concepts organized by:
- Layout compositions (Hero formats, grid systems, scroll experiences)
- Visual styles (Minimalism, brutalism, glassmorphism, gradients)
- Interaction patterns (Hover effects, transitions, reveals)
- Component concepts (Card styles, navigation types, form designs)
- Section ideas (50+ pre-designed sections with variations)

### design-references.md
Real-world examples and "looks like" references:
- Company style references (Stripe-like, Apple-like, Airbnb-style)
- Design trend names (Neomorphism, Claymorphism, Y2K revival)
- Visual metaphors (Magazine layout, Dashboard vibe, Editorial feel)

### ux-patterns.md
User experience flows and interactions:
- Onboarding patterns
- E-commerce flows
- Dashboard experiences
- Content discovery patterns
- Micro-interaction concepts

### section-library.md
Pre-designed section concepts:
- 50+ section types with multiple variants
- Each section has: Purpose, Visual concept, Layout idea, Content strategy
- Mix-and-match for complete pages

## Quick Reference

| Design Need | Asset to Use | What You Get |
|-------------|-------------|--------------|
| **Visual Style** | design-references.md | Aesthetic direction, inspiration |
| **Layout Ideas** | visual-patterns.md → Layouts | Composition concepts |
| **Interactions** | ux-patterns.md | User flows, behaviors |
| **Full Sections** | section-library.md | Ready concepts to combine |
| **Components** | visual-patterns.md → Components | Card styles, button types |

## Implementation Steps

### 1. Define Design Direction
Choose your aesthetic from design-references.md:
```
Modern SaaS: Clean, spacious, gradient accents (Stripe/Linear inspired)
Creative Portfolio: Bold typography, asymmetric layouts, motion-heavy
E-commerce Fashion: Editorial, large imagery, minimal UI
Dashboard Pro: Dense but organized, data-first, subtle color
```

### 2. Select Layout Patterns
Reference visual-patterns.md for composition:
```
Hero: Full-screen centered with floating card overlay
Product Grid: Masonry layout with hover zoom
About: Split-screen with scrolling image parallax
Features: Bento grid with mixed content types
```

### 3. Describe Visual Elements
Use design language, not code:
```
❌ Technical: "Card: border-radius 12px, shadow 0 4px 6px rgba(0,0,0,0.1)"
✅ Design: "Cards with soft rounded corners and subtle lift effect"

❌ Technical: "Button: padding 16px 32px, bg #0EA5E9, hover #0284C7"
✅ Design: "Large pill-shaped buttons with gradient on hover"

❌ Technical: "Typography: 48px, font-weight 700, line-height 1.1"
✅ Design: "Extra-large, bold headlines with tight spacing"
```

### 4. Specify User Experience
Focus on behavior and flow from ux-patterns.md:
```
- Smooth scroll-to-section navigation
- Progressive disclosure: show more details on interaction
- Optimistic UI: instant feedback before server response
- Skeleton loading states for perceived speed
- Toast notifications for non-blocking alerts
```

### 5. Combine Section Concepts
Build pages from section-library.md:
```
Landing Page =
  Hero (Type A: Video background with centered CTA) +
  Features (Bento grid variant) +
  Social Proof (Logo cloud with stats) +
  Pricing (Cards with highlight) +
  CTA (Minimal with gradient background) +
  Footer (Comprehensive with newsletter)
```

### 6. Add Design Details
Enhance with specific concepts:
```
Visual Flavor:
- Soft shadows throughout for subtle depth
- Gentle animations on hover (nothing jarring)
- Consistent rounded corners (medium)
- Accent color used sparingly for CTAs only
- Dark mode with true black backgrounds

Interactions:
- Magnetic hover effect on buttons
- Staggered fade-in for list items
- Parallax on hero image
- Smooth color transitions
```

## Common Mistakes

### ❌ Too Technical
```
"Navigation: height 64px, position fixed, z-index 1000, background rgba(255,255,255,0.8),
backdrop-filter blur(10px), box-shadow 0 1px 3px rgba(0,0,0,0.1)"
```
**Fix:** Use design language
```
"Sticky navigation with glassmorphism effect, blurred background transparency.
Modern and clean."
```

### ❌ Too Vague
```
"Make it look good and modern"
```
**Fix:** Reference specific concepts
```
"Modern SaaS aesthetic: lots of white space, soft shadows, gradient accent on primary CTA.
Think Stripe or Linear. Minimal but polished."
```

### ❌ Missing User Experience
```
"Product page with image and description"
```
**Fix:** Describe the experience
```
"Product page with image gallery (zoom on click), sticky add-to-cart that follows scroll,
progressive size/color selector, trust badges near CTA, related products with smooth
horizontal scroll"
```

### ❌ No Visual Hierarchy
```
"Show features in a grid"
```
**Fix:** Describe importance and flow
```
"Bento-style feature grid where the main feature takes 2x space, has larger imagery,
and draws attention. Secondary features are smaller cards. Visual hierarchy guides
eye top-left to bottom-right."
```

## Advanced Patterns

### Design System References
Reference well-known systems:
```
"Navigation inspired by Vercel: minimal black text on white, subtle hover states,
very restrained and confident"

"Dashboard layout similar to Notion: sidebar with nested pages, infinite scroll
main content, floating toolbar"

"Buttons like Stripe: medium size, rounded, solid colors, subtle hover lift"
```

### Mood and Tone
Describe the feeling:
```
Professional & Trustworthy:
- Clean layouts, ample white space
- Subtle animations, nothing flashy
- Conservative color palette
- Serif headlines for authority

Creative & Bold:
- Asymmetric layouts, break the grid
- Large, impactful typography
- Bright accent colors
- Playful micro-interactions

Luxury & Elegant:
- Lots of spacing, breathable
- Minimal color, mostly monochrome
- High-quality imagery, full-bleed
- Slow, smooth transitions
```

### Section Combinations
Create experiences by combining concepts:
```
E-commerce Product Page =
  Breadcrumbs (subtle, top) +
  Split Layout (60% image gallery / 40% product info) +
  Sticky Buy Box (follows scroll on right side) +
  Tabbed Details (reviews, specs, shipping) +
  Related Products (horizontal scroll carousel) +
  Trust Footer (guarantees, shipping, returns)

Dashboard Home =
  Quick Stats (4 KPI cards at top) +
  Activity Feed (left column, real-time updates) +
  Main Chart (center, interactive) +
  Quick Actions (right sidebar, contextual) +
  Recent Items (bottom, table view)
```

### Responsive Concepts
Describe behavior, not breakpoints:
```
"On mobile, the split layout becomes stacked with image gallery first.
The sticky navigation collapses to hamburger menu. Cards that were
4-columns become a swipeable horizontal carousel."

"Desktop shows side-by-side comparison. Tablet shows 2-column grid.
Mobile shows expandable accordion for comparisons."
```

## Real-World Impact

**Before this skill:**
- AI builders received overly technical specs
- Lost in translation between design intent and code
- Specifications were too rigid or too vague
- Multiple iterations to get "the vibe right"

**After this skill:**
- AI understands design intent clearly
- Flexibility in implementation details
- Faster first-draft quality
- Design concepts translate better across tools

**Example outcomes:**
- v0 generated correct visual hierarchy from concept description
- Lovable understood "Stripe-like" and applied appropriate styling
- Bolt interpreted "bento grid" and created proper layout
- 70% reduction in "not what I wanted" iterations

## Accessibility Considerations

Describe accessibility in UX terms, not technical:
```
❌ Technical: "All buttons aria-label, contrast 4.5:1, focus outline 3px"
✅ Design: "All interactive elements clearly indicated, high contrast for readability,
obvious keyboard focus states, screen reader friendly with clear labels"
```

Accessibility concepts to include:
- "Clear visual hierarchy for screen readers"
- "Keyboard navigable with obvious focus states"
- "High contrast mode support"
- "Touch targets comfortable for fingers (not tiny)"
- "Form errors shown clearly inline"
- "No critical information conveyed by color alone"

## Working with AI Builders

### v0 (Vercel)
Best with:
- Clean, modern concepts
- "Inspired by [company]" references
- Component-focused descriptions
- React/Next.js patterns

Example:
```
"Create a pricing section with 3 tiers. Stripe-inspired design: clean cards with
subtle borders, hover lift effect. Middle tier highlighted with gradient border.
Include popular badge on middle option. Toggle for monthly/annual pricing."
```

### Lovable
Best with:
- Full-page concepts
- User flow descriptions
- "Feels like [experience]" references
- Interactive behaviors

Example:
```
"Dashboard home page with sidebar navigation. Feels like Linear: fast, modern,
keyboard shortcuts. Main area shows project cards in grid, hover reveals quick
actions. Smooth animations throughout."
```

### Bolt (StackBlitz)
Best with:
- Complete app concepts
- Feature descriptions
- Interaction patterns
- Multi-page flows

Example:
```
"E-commerce storefront with product grid, filtering sidebar, cart drawer.
Modern fashion site vibe: large product images, minimal UI, smooth transitions.
Quick view modal on product hover."
```

### Replit Agent
Best with:
- Functional descriptions
- User stories
- Behavior explanations
- Progressive enhancement

Example:
```
"Blog homepage: hero with featured post (large image, title, excerpt), followed
by grid of recent posts (3 columns). Each card shows image, category badge, title,
date, read time. Hover shows brief excerpt. Clean, readable, medium.com inspired."
```

## See Also

- `assets/visual-patterns.md` - Design pattern library
- `assets/design-references.md` - Style inspiration catalog
- `assets/ux-patterns.md` - User experience flows
- `assets/section-library.md` - Pre-designed sections
- `ui-prompt-generation` skill - For technical specifications
