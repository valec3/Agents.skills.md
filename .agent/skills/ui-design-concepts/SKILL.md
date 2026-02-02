---
name: ui-design-concepts
description: Use when creating design specifications for AI builders (v0, Lovable, Bolt, Replit), describing visual concepts, patterns, and user experiences without technical implementation details
---

# UI Design Concepts

## Overview

**UI Design Concepts IS the definition of Application Structure, User Flow, and Functional Capabilities.**

This skill is for describing **WHAT the app does and HOW it works**, not just how it looks. It focuses on Navigation structure, Module breakdown, User Interactions, and Business Logic flows.

**Core Principle:** Functionality First. Describe the sidebar modules, dashboard widgets, and modal interactions before mentioning colors.

## When to Use

**Use this skill when:**
- Defining **Application Architecture** and Module Breakdown
- Describing **User Journeys**, Business Logic, and Conditional Flows
- Specifying **Navigational Structures** (Sidebar vs Topbar, Breadcrumbs)
- Defining **Interaction Models** (Modals, Drawers, Toasts, Empty States)
- The user asks for "How it works" or "What features it has"

**Don't use when:**
- The user needs specific Tailwind classes or CSS variables (use `ui-prompt-generation`)
- You are writing the code yourself
- Exact pixel perfection is required

## Core Pattern

**Before (Vague):**
> "Make it look cool and modern."

**After (Standardized):**
> **[Agent quietly generates `results/concept.txt`]**
> "Design Concept: Modern SaaS Dashboard
> - **Aesthetic**: Minimalist & Professional (Ref: `design-references.md`).
> - **Layout**: Bento Grid (Ref: `visual-patterns.md`).
> - **Key Flow**: Optimistic UI updates with toast notifications (Ref: `ux-patterns.md`).
> - **Inspiration**: Linear's dark mode, high contrast, subtle borders."

## Implementation

**CRITICAL RULE: OUTPUT MUST BE A PLAIN TEXT `.txt` FILE IN `results/`.**
**NEVER** use Markdown syntax (no `#`, no `**`, no `[ ]`, no code blocks) inside the `.txt` file.
**ALWAYS** use clean Plain Text formatting:
- Use UPPERCASE for section headers.
- Use indentation for hierarchy.
- Use simple text labels.

### Phase 1: Inspiration & Reference
1.  **Analyze Request**: What is the *feeling*? (Professional, Playful, Luxury?).
2.  **Load Assets (MANDATORY)**: You **MUST** use `view_file` on these files:
    -   `assets/design-references.md` (Find the aesthetic archetypes)
    -   `assets/visual-patterns.md` (Select layout compositions)
    -   `assets/ux-patterns.md` (Define interaction behaviors)
    -   `assets/section-library.md` (Assemble page structure)

### Phase 2: Synthesis
Combine the selected elements into a cohesive narrative.
-   **Visual Style**: Define the mood (e.g., "Glassmorphism with heavy blur").
-   **Composition**: Describe how elements "sit" on the page (e.g., "Masonry grid").
-   **Motion**: Describe how things move (e.g., "Staggered fade-ins").

### Phase 3: Delivery
1.  **Write File**: Save the narrative to `results/<descriptive-name>.txt`.
2.  **Notify**: Tell the user "Concept generated: `results/<filename>.txt`".

## Common Mistakes

### ❌ Being Technical
**Bad**: "Use `border-radius: 8px`."
**Good**: "The modal must strictly close when clicking the backdrop to allow quick exit."
**Fix**: If you are writing numbers or describing "vibes", swtich skills. Describe **BEHAVIOR**.

### ❌ Name-Dropping Without Context
**Bad**: "Make it like Apple."
**Good**: "Apple-style aesthetic: heavy use of white space, large typography, and premium product photography."
**Fix**: Explain *why* the reference works using `design-references.md`.

### ❌ Chat Dump
**Bad**: Outputting the concept narrative in the chat window.
**Good**: Silent file generation.
**Fix**: Ensure `results/` is the target.

## Quick Reference

| Asset | Purpose |
| :--- | :--- |
| **`design-references.md`** | **REQUIRED**. Styles, vibes, and real-world inspirations. |
| **`visual-patterns.md`** | **REQUIRED**. Layouts, grids, and component styles. |
| **`ux-patterns.md`** | **REQUIRED**. Interactions, flows, and behaviors. |
| **`section-library.md`** | Ready-made sections to build pages fast. |
