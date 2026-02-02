# UI Prompt Generation Assets

This directory contains comprehensive reference materials for generating professional, complete UI design prompts.

---

## Asset Files

### [ui-patterns.md](./ui-patterns.md)

**Purpose:** Catalog of 14 categories of modern UI design patterns.

**Contains:**

- 140+ specific UI patterns organized by category
- Usage guidelines and pattern combinations
- When to use each pattern type
- Specificity level examples

**Use when:**

- Need to reference specific design patterns by name
- Building a comprehensive prompt requiring multiple pattern types
- Ensuring modern, industry-standard design approaches

**Categories:**

1. Layouts and Visual Structures
2. Hero Sections (Landing/Home)
3. Cards, Containers, and Surfaces
4. Navigation and Flow Structure
5. Microinteractions and Visual Feedback
6. Animations and Movement
7. Content Components
8. Dashboards and SaaS Products
9. Scroll, Interaction, and Rhythm
10. Typography and Visual Hierarchy
11. Visual Styles and Trends
12. States, Errors, and Empty Experiences
13. Mobile-First and Gestures
14. Emotional Experience and Branding

---

### [design-tokens.md](./design-tokens.md)

**Purpose:** Standardized design values for consistent UI specifications.

**Contains:**

- Spacing scale (4px base unit)
- Typography scale (16px base, 1.25 ratio)
- Font weights and line heights
- Comprehensive color system (primary, neutral, semantic)
- Shadow levels
- Border radius values
- Animation durations and easing functions
- Z-index scale
- Responsive breakpoints
- Opacity scale

**Use when:**

- Need precise, reusable design values
- Ensuring consistency across multiple components
- Specifying exact measurements and values
- Building a design system

**Token Format:**

```
category-size: value  (context/usage note)

Example:
spacing-lg: 24px (comfortable section spacing)
type-scale-5: 24px (H3, card titles)
primary-500: #0EA5E9 (base brand color)
```

---

### [component-checklist.md](./component-checklist.md)

**Purpose:** Comprehensive checklist to ensure complete component specifications.

**Contains:**

- Core component anatomy checklist
- All interactive states (default, hover, active, focus, disabled, loading, success, error)
- Responsive behavior requirements
- Accessibility requirements
- Animation specifications
- Content guidelines
- Common omissions and anti-patterns

**Use when:**

- Creating component-level prompts
- Validating completeness before finalizing
- Ensuring no critical states are forgotten
- Preventing common specification gaps

**Workflow:**

1. Start with structure
2. Add all states
3. Specify responsive behavior
4. Ensure accessibility
5. Define animations
6. Document content rules
7. Validate with quick questions

---

### [prompt-templates.md](./prompt-templates.md)

**Purpose:** Ready-to-use templates for common UI scenarios.

**Contains:**

- Template 1: Landing Page Hero Section
- Template 2: Dashboard Layout
- Template 3: Form Interface
- Template 4: Navigation System
- Template 5: Card Component

**Use when:**

- Starting a new prompt from scratch
- Need a structured format quickly
- Want to ensure standard sections are covered
- Building common UI patterns

**Template Structure:**
Each template includes:

- Purpose section (user goal)
- Layout & structure
- Visual hierarchy
- Components and variants
- Interactive states
- Responsive behavior
- Accessibility requirements
- Animations
- Style guidance

**How to use templates:**

1. Copy relevant template
2. Customize [bracketed] sections
3. Add/remove sections as needed
4. Reference tipo numbers for patterns
5. Replace with specific token values
6. Validate with component-checklist.md

---

### [accessibility-guidelines.md](./accessibility-guidelines.md)

**Purpose:** WCAG 2.1 AA compliance reference for accessible UI specifications.

**Contains:**

- WCAG 2.1 Level AA requirements
- Color contrast ratios and checker
- Keyboard navigation patterns
- Screen reader support (ARIA attributes, semantic HTML)
- Form accessibility (labels, errors, required fields)
- Interactive elements (buttons, links, modals)
- Images & media accessibility
- Motion & animation (prefers-reduced-motion)
- Mobile & touch accessibility
- Common accessible patterns (skip links, breadcrumbs, tabs, carousels)
- Testing checklist

**Use when:**

- Ensuring WCAG compliance
- Specifying keyboard navigation
- Defining ARIA attributes
- Creating accessible forms
- Testing accessibility requirements

**Key Sections:**

- Contrast requirements (4.5:1 text, 3:1 UI components)
- Keyboard shortcuts and tab order
- ARIA landmarks, roles, states, descriptions
- Focus indicator specifications (3px minimum)
- Screen reader announcement patterns
- Touch target sizes (44px minimum)

---

### [examples.md](./examples.md)

**Purpose:** Real-world examples demonstrating comprehensive UI prompt generation.

**Contains:**

- Example 1: E-commerce Product Card (comprehensive)
- Example 2: Mobile Navigation Bottom Sheet (mobile-specific)
- Example 3: Dashboard KPI Card (concise shorthand)
- Key patterns demonstrated
- Anti-patterns to avoid
- Prompt quality spectrum (minimal to comprehensive)
- Usage tips

**Use when:**

- Learning prompt structure and detail level
- Need reference examples for similar components
- Understanding token efficiency vs completeness balance
- Avoiding common specification mistakes

**Demonstrates:**

- Progressive detail (purpose → structure → content → states → accessibility)
- Consistent token references
- Complete state coverage
- Responsive strategies
- Accessibility integration
- Animation specifications

---

4. Check [component-checklist.md](./component-checklist.md) → States section for empty/loading/error states

---

## Asset Maintenance

### Adding New Patterns

When you discover a new UI pattern not in ui-patterns.md:

1. Identify which tipo (category) it belongs to
2. Add to appropriate section with clear description
3. Note when to use it
4. Add usage example if non-obvious

### Extending Design Tokens

When project needs tokens not in design-tokens.md:

1. Follow existing naming conventions (category-size format)
2. Maintain consistency with existing scale/ratio
3. Document usage context
4. Add to appropriate section

### Creating New Templates

When you find yourself creating similar prompts repeatedly:

1. Generalize the structure
2. Use [brackets] for customizable sections
3. Reference tipo numbers for patterns
4. Include all sections from component-checklist
5. Add to prompt-templates.md with clear purpose

---

## Reference Order

**For comprehensive prompts:**

1. Start: [prompt-templates.md](./prompt-templates.md) (structure)
2. Enhance: [ui-patterns.md](./ui-patterns.md) (vocabulary)
3. Specify: [design-tokens.md](./design-tokens.md) (precision)
4. Check accessibility: [accessibility-guidelines.md](./accessibility-guidelines.md) (WCAG compliance)
5. Validate: [component-checklist.md](./component-checklist.md) (completeness)
6. Review: [examples.md](./examples.md) (quality reference)

**For quick component prompts:**

1. Start: [component-checklist.md](./component-checklist.md) (ensure coverage)
2. Reference: [design-tokens.md](./design-tokens.md) (exact values)
3. Enhance: [ui-patterns.md](./ui-patterns.md) (specific patterns)
4. Check: [accessibility-guidelines.md](./accessibility-guidelines.md) (compliance)
5. Compare: [examples.md](./examples.md) (similar components)

**For finding inspiration:**

1. Browse: [ui-patterns.md](./ui-patterns.md) (discover patterns)
2. Structure: [prompt-templates.md](./prompt-templates.md) (see examples)
3. Learn: [examples.md](./examples.md) (real-world usage)
4. Implement: Follow comprehensive prompt workflow above

---

## Best Practices

1. **Always specify states** - Use component-checklist.md to ensure all states covered
2. **Use tokens consistently** - Reference design-tokens.md for all measurements
3. **Combine patterns** - Layer multiple tipo categories from ui-patterns.md
4. **Start with templates** - Customize rather than creating from scratch
5. **Ensure accessibility** - Check accessibility-guidelines.md for every component
6. **Validate completeness** - Quick validation questions from component-checklist.md
7. **Reference examples** - Use examples.md to understand detail level and quality
8. **Check contrast** - Use accessibility-guidelines.md color contrast section

---

## See Also

- [../SKILL.md](../SKILL.md) - Main skill documentation
- All 7 asset files work together - reference the Asset Relationships diagram above
