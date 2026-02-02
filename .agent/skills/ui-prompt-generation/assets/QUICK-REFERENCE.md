# UI Prompt Generation - Quick Reference Card

One-page guide for rapid UI prompt generation.

---

## 🎯 When to Use This Skill

- Generating prompts for web UI design or AI design tools
- Specifying components, layouts, or full interfaces
- Creating design briefs for frontend development
- Ensuring design consistency and completeness

---

## 📁 Asset Files (7 Total)

| File                                                             | Purpose                                     | Use When                   |
| ---------------------------------------------------------------- | ------------------------------------------- | -------------------------- |
| **[ui-patterns.md](./ui-patterns.md)**                           | 140+ design patterns, 14 categories         | Need pattern vocabulary    |
| **[design-tokens.md](./design-tokens.md)**                       | Standardized values (spacing, colors, etc.) | Need exact measurements    |
| **[prompt-templates.md](./prompt-templates.md)**                 | 5 ready-to-use templates                    | Starting new prompt        |
| **[component-checklist.md](./component-checklist.md)**           | Completeness validation                     | Ensuring nothing forgotten |
| **[accessibility-guidelines.md](./accessibility-guidelines.md)** | WCAG 2.1 AA compliance                      | Ensuring accessibility     |
| **[examples.md](./examples.md)**                                 | Real-world complete examples                | Learning/comparing quality |
| **[workflow-visual.md](./workflow-visual.md)**                   | Visual diagrams and flowcharts              | Understanding process      |

---

## ⚡ 5-Step Quick Process

```
1. STRUCTURE   → Start with template (templates.md)
2. VOCABULARY  → Add patterns (ui-patterns.md - tipos 1-14)
3. PRECISION   → Specify tokens (design-tokens.md)
4. COMPLIANCE  → Check accessibility (accessibility-guidelines.md)
5. VALIDATE    → Use checklist (component-checklist.md)
```

---

## 🔑 Key Pattern Categories (Tipos)

Quick reference to ui-patterns.md categories:

1. **Layouts** - Masonry, bento grid, asymmetrical
2. **Hero Sections** - Centered, split, with video
3. **Cards** - Elevated, glassmorphism, soft
4. **Navigation** - Sticky, mega menu, bottom nav
5. **Microinteractions** - Hover, focus, loading states
6. **Animations** - Scroll-driven, parallax, staggered
7. **Content Components** - Accordions, carousels, timelines
8. **Dashboards** - KPI cards, filters, data tables
9. **Scroll Behavior** - Scroll snap, sticky sections
10. **Typography** - Oversized headings, hierarchy
11. **Visual Styles** - Minimalism, dark mode, brutalism
12. **States** - Empty, error, loading, success
13. **Mobile** - Bottom sheets, gestures, thumb-friendly
14. **Emotional** - Delight moments, brand personality

---

## 🎨 Essential Design Tokens

### Spacing (4px base)

```
spacing-sm:  8px   spacing-md:  16px   spacing-lg:  24px
spacing-xl: 32px   spacing-2xl: 48px   spacing-3xl: 64px
```

### Typography (16px base, 1.25 ratio)

```
type-scale-1:  12px  (captions)       weight-normal:    400
type-scale-2:  14px  (small text)     weight-medium:    500
type-scale-3:  16px  (body - BASE)    weight-semibold:  600
type-scale-5:  24px  (H3)             weight-bold:      700
type-scale-6:  32px  (H2)
type-scale-8:  48px  (display)
type-scale-9:  64px  (hero)
```

### Colors

```
primary-500:  #0EA5E9  (brand)     neutral-800:  #262626  (text)
primary-600:  #0284C7  (hover)     neutral-600:  #525252  (secondary)
success-500:  #22C55E              error-500:    #EF4444
```

### Animation

```
duration-fast: 150ms  (hover)      easing-smooth: cubic-bezier(0.4, 0, 0.2, 1)
duration-base: 300ms  (standard)   shadow-md:     0 4px 6px rgba(0,0,0,0.07)
duration-slow: 500ms  (major)      radius-md:     8px
```

---

## ✅ 8 Required Interactive States

Every interactive component MUST specify:

1. ✓ **Default** - Initial appearance
2. ✓ **Hover** - Mouse over (desktop only)
3. ✓ **Active** - During click/tap
4. ✓ **Focus** - Keyboard navigation (3px outline minimum)
5. ✓ **Disabled** - Non-interactive state
6. ✓ **Loading** - Async operation
7. ✓ **Error** - Failed/invalid state
8. ✓ **Success** - Successful completion

Plus: **Empty state** (if applicable)

---

## ♿ Accessibility Quick Checks

### WCAG AA Minimums

- **Text contrast:** 4.5:1 (normal), 3:1 (large 18px+)
- **UI components:** 3:1 contrast
- **Touch targets:** 44px × 44px minimum
- **Focus indicator:** 3px visible outline

### Required Attributes

- **Semantic HTML:** Use `<button>`, `<nav>`, `<main>`, etc.
- **ARIA labels:** For icon-only buttons
- **Alt text:** For all informative images
- **aria-live:** For dynamic content updates
- **Keyboard nav:** Tab order, Enter/Space, Escape

### Quick Test

Can you complete all tasks with:

- ✓ Keyboard only?
- ✓ 200% zoom?
- ✓ Screen reader?
- ✓ In grayscale (no color)?

---

## 📱 Responsive Breakpoints

```
Mobile:   < 640px   (default, mobile-first)
Tablet:   640-1024px
Desktop:  1024px+
Large:    1280px+

Always specify behavior at each breakpoint!
```

---

## 🚫 Common Mistakes to Avoid

❌ "Make it modern" → ✅ "Soft minimalism, muted palette, oversized headings"
❌ "Add a button" → ✅ Specify all 8 states + accessibility
❌ "16px spacing" → ✅ "spacing-md (16px)"
❌ Missing hover state → ✅ Include hover for desktop
❌ No responsive plan → ✅ Define mobile, tablet, desktop
❌ Forgot accessibility → ✅ Check every component

---

## 📋 Templates Available

1. **Landing Page Hero** - Full-page hero section
2. **Dashboard Layout** - SaaS/admin interface
3. **Form Interface** - Complete form with validation
4. **Navigation System** - Desktop + mobile nav
5. **Card Component** - Reusable card pattern

Each template includes: Purpose, Layout, States, Responsive, Accessibility, Animations

---

## 🎓 Quality Levels

### Level 1 (Unusable)

"Create a button"

### Level 2 (Basic)

"Blue button, 16px text, rounded"

### Level 3 (Structured)

"Button: primary-500 bg, white text, spacing-md padding, radius-md, hover darker"

### Level 4 (Production-Ready) ⭐

Complete spec with:

- All 8 states defined
- Design tokens used
- Accessibility included
- Responsive specified
- Animations detailed

**Aim for Level 4!**

---

## 🔄 Quick Workflow for Components

```
1. Start → component-checklist.md (structure)
2. Add  → ui-patterns.md Tipo 5 (microinteractions)
3. Specify → design-tokens.md (exact values)
4. Check → accessibility-guidelines.md (compliance)
5. Compare → examples.md (quality reference)
```

---

## 🔄 Quick Workflow for Pages

```
1. Start → prompt-templates.md (template 1 or 2)
2. Add → ui-patterns.md (multiple tipos)
3. Specify → design-tokens.md (consistency)
4. Check → accessibility-guidelines.md (semantic HTML, ARIA)
5. Validate → component-checklist.md (completeness)
```

---

## 💡 Pro Tips

1. **Start with template** - Don't write from scratch
2. **Reference tipos by number** - "Use Tipo 5 (Microinteractions)"
3. **Always use tokens** - Avoid arbitrary values
4. **Mobile-first** - Specify mobile, then enhance for desktop
5. **States are critical** - Never skip the 8 required states
6. **Accessibility is not optional** - Check every component
7. **Compare to examples** - Match quality level in examples.md

---

## 🎯 One-Sentence Summary

**Use structured templates, pattern vocabulary (tipos), and design tokens to create complete, accessible, production-ready UI specifications.**

---

## 📚 Full Documentation

- Main skill: [../SKILL.md](../SKILL.md)
- Assets overview: [README.md](./README.md)
- Visual guide: [workflow-visual.md](./workflow-visual.md)

---

## ⚡ Ultra-Quick Start

1. Open [prompt-templates.md](./prompt-templates.md)
2. Copy relevant template
3. Customize [bracketed] sections
4. Add tipos from [ui-patterns.md](./ui-patterns.md)
5. Replace with tokens from [design-tokens.md](./design-tokens.md)
6. Validate with [component-checklist.md](./component-checklist.md)
7. Done! ✓

**Estimated time for production-ready prompt: 10-15 minutes**

---

Print this page for quick reference while generating UI prompts!
