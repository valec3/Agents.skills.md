# UI Design Patterns Reference

Comprehensive catalog of modern web UI patterns organized by category. Reference these when generating design prompts for consistency and completeness.

---

## Tipo 1: Layouts y Estructuras Visuales

**When to use:** Establishing overall page structure and content flow.

- **Masonry layout** - Pinterest-style variable-height grid
- **Bento grid** - Japanese lunchbox-inspired segmented layout
- **Asymmetrical grid** - Intentionally unbalanced for visual interest
- **Z-pattern layout** - Natural reading flow (logo → CTA → content → footer)
- **F-pattern layout** - Left-aligned scanning pattern for text-heavy content
- **Split screen layout** - Two equal vertical sections
- **Stacked sections** - Full-width sections stacked vertically
- **Full-bleed sections** - Content extending to viewport edges
- **Card-based layout** - Contained content units in grid
- **Responsive column stacking** - Multi-column → single column on mobile

---

## Tipo 2: Hero Sections (Landing / Home)

**When to use:** First impression, above-the-fold messaging.

- **Centered hero with single CTA** - Focused conversion, minimal distraction
- **Hero con background video** - Immersive brand storytelling
- **Hero con mockup flotante** - Product-led with floating device mockup
- **Hero dividido** (copy + visual) - Split screen, text left/image right
- **Hero con scroll cue** - Downward arrow indicating more content
- **Hero con headline oversized** - Typography-dominant, minimal other elements
- **Hero minimalista sin imagen** - Text-only, ultra-clean
- **Hero con ilustración editorial** - Custom illustration as focal point
- **Hero con trust indicators visibles** - Logos, testimonials, metrics immediately visible

---

## Tipo 3: Tarjetas, Contenedores y Superficies

**When to use:** Grouping related content, creating visual hierarchy.

- **Cards elevadas** - Drop shadow, floating appearance
- **Soft cards (sin bordes)** - Subtle background color only
- **Glassmorphism** - Frosted glass effect, backdrop blur
- **Neumorphism suave** - Soft shadows, embossed/extruded appearance
- **Outline cards** - Border only, no fill
- **Interactive cards (hover expand)** - Grow/elevate on hover
- **Cards con media dominante** - Large image/video with minimal text
- **Cards con acciones progresivas** - Reveal actions on hover/focus
- **Cards skeleton state** - Loading placeholder with animated shimmer

---

## Tipo 4: Navegación y Estructura de Flujo

**When to use:** Wayfinding, site hierarchy, user orientation.

- **Top navigation sticky** - Fixed at top during scroll
- **Navigation con scroll-aware states** - Changes style/size on scroll
- **Mega menu visual** - Large dropdown with images, categories
- **Bottom navigation mobile** - Thumb-friendly mobile nav bar
- **Sidebar colapsable** - Expandable drawer, common in dashboards
- **Breadcrumbs contextuales** - Current location in hierarchy
- **Navigation por tabs** - Horizontal tabs for related sections
- **Progressive disclosure navigation** - Show more options as needed

---

## Tipo 5: Microinteracciones y Feedback Visual

**When to use:** Providing immediate user feedback, improving perceived performance.

- **Hover affordances claros** - Visual cue that element is interactive
- **Button press states** - Subtle scale/shadow change on click
- **Focus states visibles** - Clear keyboard navigation indicators
- **Loading skeletons** - Content placeholder during load
- **Success / error inline feedback** - Immediate validation messages
- **Animated state transitions** - Smooth changes between states
- **Microcopy contextual** - Helpful hints at point of interaction
- **Subtle motion feedback** - Small animations confirming actions
- **Empty states ilustrados** - Friendly visuals when no content exists

---

## Tipo 6: Animaciones y Movimiento (Conceptual)

**When to use:** Adding polish, guiding attention, storytelling.

- **Scroll-driven animations** - Elements animate based on scroll position
- **Parallax sutil** - Background moves slower than foreground
- **Staggered entrance animations** - Items appear sequentially with delay
- **Reveal on scroll** - Content fades in when entering viewport
- **Motion-based hierarchy** - Important elements move first/faster
- **Page transition animations** - Smooth between-page animations
- **Depth motion (z-axis)** - Elements moving forward/backward
- **Natural easing motion** - Organic, non-linear timing functions
- **Attention-guided motion** - Animation directing eye to key element

---

## Tipo 7: Componentes de Contenido

**When to use:** Organizing and presenting detailed information.

- **Accordions animados** - Expandable sections with smooth height transition
- **Expandable sections** - Click to reveal more content
- **Carousels horizontales** - Standard horizontal sliding content
- **Carousels inclinados** - Angled/3D perspective carousel
- **Timeline vertical** - Chronological events along vertical line
- **Stepper visual** - Multi-step process indicator
- **Feature comparison tables** - Side-by-side product/plan comparison
- **Sticky side content** - Sidebar that follows scroll
- **Content clustering** - Related items grouped visually

---

## Tipo 8: Dashboards y Productos SaaS

**When to use:** Data-heavy applications, admin interfaces, analytics.

- **Data cards** - Metrics in contained card format
- **KPI highlights** - Key numbers prominently displayed
- **Progressive data disclosure** - Summary → details on interaction
- **Visual filters** - Tag-based, checkbox, or dropdown filtering
- **Inline editing** - Edit directly in table/list without modal
- **Contextual actions** - Actions appear on hover/selection
- **Empty dashboard states** - Onboarding when no data exists
- **Dense vs breathable layouts** - Compact power user vs spacious casual
- **Modular dashboard blocks** - Draggable/rearrangeable widgets

---

## Tipo 9: Scroll, Interacción y Ritmo

**When to use:** Controlling content pacing, improving reading flow.

- **Overscroll effects** - Bounce/stretch at scroll boundaries
- **Scroll snapping** - Snap to section boundaries
- **Section-based scrolling** - Full-screen sections, one per scroll
- **Sticky sections narrativas** - Pin section while content scrolls over
- **Scroll hijacking controlado** - Custom scroll behavior (use sparingly)
- **Long-form scrollytelling** - Narrative with scroll-triggered visuals
- **Anchor-based navigation** - Jump to page sections
- **Scroll progress indicators** - Visual bar showing page position

---

## Tipo 10: Tipografía y Jerarquía Visual

**When to use:** Establishing content hierarchy, improving readability.

- **Oversized headings** - Exceptionally large display text (72px+)
- **Variable font usage** - Dynamic weight/width adjustments
- **Tight headline + relaxed body** - Compact headers, generous body line height
- **Visual rhythm spacing** - Consistent vertical spacing scale
- **Line-length control** - Optimal 50-75 characters per line
- **Typographic scale clara** - Defined size progression (e.g., 1.25 ratio)
- **Contrast-driven hierarchy** - Size, weight, color differentiation
- **Text + icon pairing** - Icons enhancing text meaning
- **Minimal font pairing** - Max 2 typefaces, multiple weights

---

## Tipo 11: Estilos Visuales y Tendencias

**When to use:** Establishing visual identity, brand alignment.

- **Soft minimalism** - Clean, ample whitespace, subtle colors
- **Editorial design influence** - Magazine-style layouts, bold typography
- **Brutalismo controlado** - Raw, brutalist elements with usability
- **Neo-skeuomorphism ligero** - Subtle real-world material hints
- **Dark mode-first design** - Designed for dark, adapted to light
- **Muted color palettes** - Desaturated, sophisticated tones
- **Accent color-driven UI** - Neutral base + vibrant accent
- **High-contrast UI** - Strong black/white contrast
- **Monochrome base + color highlight** - Grayscale with selective color

---

## Tipo 12: Estados, Errores y Experiencias Vacías

**When to use:** Handling edge cases, errors, and empty states gracefully.

- **Empty states educativos** - Explain why empty, what to do next
- **Zero-data onboarding** - First-time user guidance
- **Error states humanos** - Friendly, actionable error messages
- **Offline states claros** - Explicit offline mode indicators
- **Permission request states** - Explain why permission needed
- **Confirmation states visuales** - Visual success feedback
- **Undo affordances** - Clear way to reverse actions
- **Non-blocking warnings** - Notifications that don't interrupt flow

---

## Tipo 13: Mobile-First y Gestos

**When to use:** Touch interfaces, mobile-specific interactions.

- **Bottom sheets** - Modal that slides up from bottom
- **Swipeable cards** - Horizontal swipe to dismiss/action
- **Pull-to-refresh feedback** - Visual indicator during pull-to-refresh
- **Thumb-friendly spacing** - 44px+ touch targets, bottom-heavy layout
- **Gesture hints visuales** - Subtle cues for swipe/pinch actions
- **Floating action buttons contextuales** - Primary action, bottom-right
- **One-handed navigation** - Key actions in thumb reach zone
- **Progressive reveal mobile** - Minimized, expand on demand

---

## Tipo 14: Experiencia Emocional y Branding

**When to use:** Creating emotional connection, brand differentiation.

- **Delight moments** - Unexpected pleasant interactions
- **Brand motion consistency** - Animation style matching brand personality
- **Visual storytelling** - Illustrations/photos telling brand story
- **Illustration systems** - Cohesive illustration style throughout
- **Iconography cohesion** - Consistent icon style (outline/filled/duotone)
- **Tone-aware UI** - Interface reflecting brand voice
- **Personality-driven UI elements** - Unique design elements expressing brand
- **Emotional hierarchy** - Visual emphasis on emotionally important content

---

## Usage Guidelines

### Combining Patterns

Most interfaces combine multiple pattern types:

```
Landing Page = Tipo 1 (Layout) + Tipo 2 (Hero) + Tipo 3 (Cards) + Tipo 10 (Typography)
Dashboard = Tipo 1 (Layout) + Tipo 8 (Dashboard) + Tipo 5 (Microinteractions) + Tipo 12 (States)
Mobile App = Tipo 13 (Mobile) + Tipo 4 (Navigation) + Tipo 5 (Feedback) + Tipo 12 (States)
```

### Pattern Selection

1. Start with Layout (Tipo 1) - establish structure
2. Add component patterns (Tipos 3, 7, 8) - build content
3. Layer interactions (Tipos 5, 6) - add life
4. Handle states (Tipo 12) - cover edge cases
5. Apply style (Tipos 10, 11) - visual identity

### Specificity Levels

- **Low specificity:** "Use cards" → Any card pattern from Tipo 3
- **Medium specificity:** "Use soft cards with hover expand" → Specific patterns
- **High specificity:** "Use glassmorphism cards (backdrop-blur-lg, bg-white/10) with hover expand (scale-105, shadow-xl, transition 300ms ease-out)"
