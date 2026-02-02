# UI Prompt Generation Workflow

Visual guide to using the ui-prompt-generation skill and its assets.

---

## Complete Workflow Diagram

```
┌─────────────────────────────────────────────────────────────────┐
│                    START: User UI Requirement                    │
└──────────────────────────┬──────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│  STEP 1: Choose Starting Point                                   │
│  ┌──────────────┐  ┌──────────────┐  ┌────────────────────┐   │
│  │ New Project? │  │ Component?   │  │ Need Inspiration?  │   │
│  │ → Templates  │  │ → Checklist  │  │ → Patterns        │   │
│  └──────────────┘  └──────────────┘  └────────────────────┘   │
└──────────────────────────┬──────────────────────────────────────┘
                           │
         ┌─────────────────┼─────────────────┐
         │                 │                 │
         ▼                 ▼                 ▼
┌────────────────┐ ┌───────────────┐ ┌──────────────────┐
│ prompt-        │ │ component-    │ │ ui-patterns.md   │
│ templates.md   │ │ checklist.md  │ │                  │
│                │ │               │ │ Browse patterns  │
│ Copy template  │ │ Use checklist │ │ Choose tipos     │
└───────┬────────┘ └───────┬───────┘ └────────┬─────────┘
        │                  │                  │
        └──────────────────┼──────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│  STEP 2: Add Pattern Vocabulary                                 │
│                                                                  │
│  ui-patterns.md → Reference specific tipos                      │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐           │
│  │ Tipo 1      │  │ Tipo 5      │  │ Tipo 11     │           │
│  │ Layouts     │  │ Microinter. │  │ Styles      │           │
│  └─────────────┘  └─────────────┘  └─────────────┘           │
└──────────────────────────┬──────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│  STEP 3: Specify Exact Values                                   │
│                                                                  │
│  design-tokens.md → Use standardized tokens                     │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐        │
│  │ spacing-lg   │  │ type-scale-5 │  │ primary-500  │        │
│  │ = 24px       │  │ = 24px       │  │ = #0EA5E9    │        │
│  └──────────────┘  └──────────────┘  └──────────────┘        │
└──────────────────────────┬──────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│  STEP 4: Ensure Accessibility                                   │
│                                                                  │
│  accessibility-guidelines.md → Check requirements               │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐           │
│  │ Contrast    │  │ Keyboard    │  │ ARIA        │           │
│  │ 4.5:1 min   │  │ Tab order   │  │ Attributes  │           │
│  └─────────────┘  └─────────────┘  └─────────────┘           │
└──────────────────────────┬──────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│  STEP 5: Validate Completeness                                  │
│                                                                  │
│  component-checklist.md → Ensure all sections covered           │
│  ✓ Visual states (8 states)                                    │
│  ✓ Responsive behavior                                         │
│  ✓ Accessibility requirements                                  │
│  ✓ Animation specifications                                    │
│  ✓ Content guidelines                                          │
└──────────────────────────┬──────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│  STEP 6: Quality Check                                          │
│                                                                  │
│  examples.md → Compare to real-world examples                   │
│  - Detail level appropriate?                                    │
│  - All patterns demonstrated?                                   │
│  - Avoiding anti-patterns?                                      │
└──────────────────────────┬──────────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────────┐
│                  RESULT: Production-Ready Prompt                 │
└─────────────────────────────────────────────────────────────────┘
```

---

## Asset Relationships Diagram

```
                     ┌────────────────────┐
                     │  SKILL.md          │
                     │  (Main Guide)      │
                     └─────────┬──────────┘
                               │ refers to
                ┌──────────────┼──────────────┐
                │              │              │
                ▼              ▼              ▼
        ┌──────────────┐ ┌──────────────┐ ┌──────────────┐
        │ Templates    │ │ Patterns     │ │ Tokens       │
        │ Structure    │ │ Vocabulary   │ │ Precision    │
        └──────┬───────┘ └──────┬───────┘ └──────┬───────┘
               │                │                │
               └────────────────┼────────────────┘
                                │
                ┌───────────────┼───────────────┐
                │               │               │
                ▼               ▼               ▼
        ┌──────────────┐ ┌──────────────┐ ┌──────────────┐
        │ Checklist    │ │ A11y Guide   │ │ Examples     │
        │ Completeness │ │ Compliance   │ │ Reference    │
        └──────────────┘ └──────────────┘ └──────────────┘
                                │
                                ▼
                     ┌────────────────────┐
                     │  README.md         │
                     │  (Navigation)      │
                     └────────────────────┘
```

---

## Quick Decision Tree

```
                    Need to create UI prompt?
                             │
                             ▼
                    What are you creating?
                             │
        ┌────────────────────┼────────────────────┐
        │                    │                    │
        ▼                    ▼                    ▼
  Full Page/Section    Single Component     Dashboard/SaaS
        │                    │                    │
        ▼                    ▼                    ▼
  Templates #1,2,4     Checklist first     Template #2
  + Patterns 1-14      + Patterns 3,5      + Patterns 1,8
        │                    │                    │
        └────────────────────┼────────────────────┘
                             │
                             ▼
               Add design tokens for precision
                             │
                             ▼
              Check accessibility guidelines
                             │
                             ▼
                Validate with checklist
                             │
                             ▼
                   Compare to examples
                             │
                             ▼
                        Done! ✓
```

---

## Complexity vs Detail Matrix

```
Complexity  │
           │
High       │  Template #2        Full Examples
           │  (Dashboard)        (E-commerce Card)
           │       │                    │
           │       ▼                    ▼
           │  All patterns      Complete checklist
           │  All tokens        Full accessibility
           │  All states        All animations
           │
Medium     │  Template #3        Concise Example
           │  (Forms)            (KPI Card)
           │       │                    │
           │       ▼                    ▼
           │  Key patterns       Essential states
           │  Core tokens        Key accessibility
           │  Critical states    Main animations
           │
Low        │  Basic Template     Shorthand
           │  + Patterns         + Tokens
           │       │                    │
           │       ▼                    ▼
           │  Structure          Quick spec
           │  + Vocabulary       + Validation
           │
           └────────────────────────────────────► Detail Level
                Low           Medium         High
```

---

## State Coverage Checklist (Visual)

```
Interactive Component States - Must Cover All:

┌─────────────┐  ┌─────────────┐  ┌─────────────┐
│  Default    │  │   Hover     │  │   Active    │
│  ✓ Always   │  │  ✓ Desktop  │  │  ✓ During   │
│    present  │  │    only     │  │    click    │
└─────────────┘  └─────────────┘  └─────────────┘

┌─────────────┐  ┌─────────────┐  ┌─────────────┐
│   Focus     │  │  Disabled   │  │  Loading    │
│  ✓ Keyboard │  │ ✓ Inactive  │  │  ✓ Async    │
│    nav      │  │   state     │  │    action   │
└─────────────┘  └─────────────┘  └─────────────┘

┌─────────────┐  ┌─────────────┐
│   Error     │  │  Success    │
│  ✓ Failed   │  │ ✓ Completed │
│    action   │  │   action    │
└─────────────┘  └─────────────┘

Plus: Empty state (if applicable)
```

---

## Responsive Breakpoint Visual

```
Mobile First Approach:

┌────────────────────────────────────────────────────────┐
│  < 640px (Mobile)                                      │
│  ┌────────────────┐                                    │
│  │ Single Column  │  ← Start here                     │
│  │ Full Width     │                                    │
│  │ 44px+ Touch    │                                    │
│  └────────────────┘                                    │
└────────────────────────────────────────────────────────┘
                 │ @media (min-width: 640px)
                 ▼
┌────────────────────────────────────────────────────────┐
│  640-1024px (Tablet)                                   │
│  ┌────────┐  ┌────────┐                               │
│  │  Two   │  │ Column │                               │
│  │ Column │  │ Layout │                               │
│  └────────┘  └────────┘                               │
└────────────────────────────────────────────────────────┘
                 │ @media (min-width: 1024px)
                 ▼
┌────────────────────────────────────────────────────────┐
│  1024px+ (Desktop)                                     │
│  ┌─────┐  ┌─────┐  ┌─────┐  ┌─────┐                 │
│  │ 4   │  │ Col │  │ Grid│  │ Max │                 │
│  │ Col │  │ Layo│  │ Ful │  │ Feat│                 │
│  └─────┘  └─────┘  └─────┘  └─────┘                 │
└────────────────────────────────────────────────────────┘
```

---

## Token Usage Pattern

```
Instead of arbitrary values:
❌ "16px spacing"
❌ "#0EA5E9 color"
❌ "300ms transition"

Use semantic tokens:
✓ "spacing-md (16px)"
✓ "primary-500 (#0EA5E9)"
✓ "duration-base (300ms)"

Benefits:
┌────────────┐    ┌────────────┐    ┌────────────┐
│ Consistent │ →  │  Scalable  │ →  │ Maintainable│
│   System   │    │   Design   │    │    Code     │
└────────────┘    └────────────┘    └────────────┘
```

---

## Accessibility Integration Pattern

```
Not an afterthought:         Integrated throughout:

┌──────────────┐            ┌──────────────┐
│ Visual Design│            │ Visual Design│
└──────────────┘            │ + Semantic   │
       │                    │ + ARIA       │
       ▼                    │ + Keyboard   │
┌──────────────┐            │ + Contrast   │
│ Add A11y     │            │ + Touch      │
│ Later        │            └──────────────┘
└──────────────┘                   │
       │                           ▼
       ▼                    ┌──────────────┐
❌ Incomplete               │  Complete    │
❌ Retrofit                 │  Prompt  ✓   │
❌ Forgotten                └──────────────┘
```

---

## Example: Button Specification Journey

```
Level 1: "Create a button"
   │
   ▼ (Add template structure)
Level 2: "Button with text, color, size"
   │
   ▼ (Add pattern vocabulary)
Level 3: "Primary button, hover state, rounded"
   │
   ▼ (Add design tokens)
Level 4: "Button: primary-500, spacing-md, radius-md, hover: primary-600"
   │
   ▼ (Add all states from checklist)
Level 5: "+ focus, disabled, loading, active states"
   │
   ▼ (Add accessibility)
Level 6: "+ keyboard nav, ARIA, contrast check"
   │
   ▼ (Add animations)
Level 7: "+ duration-fast, easing-smooth, reduced-motion"
   │
   ▼ (Validate completeness)
Level 8: Production-Ready Specification ✓
```

---

## File Size Reference

```
Asset Files (by size):

ui-patterns.md              ████████████ (Largest - reference)
design-tokens.md            ██████████
accessibility-guidelines.md ██████████
examples.md                 ████████
prompt-templates.md         ███████
component-checklist.md      ██████
README.md                   ████ (You are here)

Usage frequency:

templates.md     ████████████ (Start point)
patterns.md      ███████████
tokens.md        ███████████
checklist.md     ██████████ (Validation)
a11y-guide.md    ████████
examples.md      ██████ (Reference)
```

---

## Summary: The UI Prompt Generation Method

1. **Structure** (Templates) → What sections to include
2. **Vocabulary** (Patterns) → What patterns to reference
3. **Precision** (Tokens) → What exact values to use
4. **Compliance** (Accessibility) → What standards to meet
5. **Completeness** (Checklist) → What to validate
6. **Quality** (Examples) → What level to achieve

Result: Professional, comprehensive, production-ready UI specifications.
