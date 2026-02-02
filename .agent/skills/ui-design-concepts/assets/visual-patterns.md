# Visual Design Patterns

Design concepts organized by category. Use these to describe "how it looks" without technical specifications.

---

## LAYOUT COMPOSITIONS

### Centered Everything
Single column, content centered horizontally and vertically, generous white space around all elements.
**Feel**: Minimal, confident, focused
**Works for**: Landing pages, simple forms, focused messages

### Split Screen
Content divided 50/50 or 60/40 left/right, clear visual separation between sections.
**Feel**: Balanced, modern, professional
**Works for**: Product + description, form + info, before/after

### Sidebar Layout
Fixed sidebar (left or right) with main content area, sidebar typically navigation or filters.
**Feel**: App-like, organized, functional
**Works for**: Dashboards, catalogs, documentation

### Bento Grid
Mixed-size grid layout where some cells are larger, creating visual hierarchy while maintaining structure.
**Feel**: Dynamic, modern, Apple-esque
**Works for**: Features, portfolios, mixed content types

### Masonry / Pinterest Style
Columns with variable height items, content flows naturally without rigid rows.
**Feel**: Organic, visual-first, exploratory
**Works for**: Image galleries, portfolios, content feeds

### Card Grid
Uniform cards in responsive grid, consistent sizing across items.
**Feel**: Organized, clean, predictable
**Works for**: Products, blog posts, team members, features

### Hero + Sections
Full-viewport hero at top, followed by distinct full-width sections stacked vertically.
**Feel**: Story-driven, narrative, marketing-focused
**Works for**: Landing pages, product pages, marketing sites

### Floating Panels
Content in floating card/panel elements over background, depth created through shadows/layers.
**Feel**: Modern, airy, dimensional
**Works for**: Dashboards, modals, feature callouts

### Asymmetric Layout
Intentionally off-balance composition, elements positioned deliberately "wrong" for visual interest.
**Feel**: Creative, bold, attention-grabbing
**Works for**: Creative agencies, portfolios, artistic sites

### Magazine Layout
Editorial-style with varied column counts, intentional white space, pull quotes, mixed image sizes.
**Feel**: Sophisticated, editorial, content-rich
**Works for**: Articles, case studies, storytelling

---

## VISUAL STYLES

### Glassmorphism
Frosted glass effect, semi-transparent elements with blur, light borders, often colorful backgrounds behind.
**Vibe**: Modern, depth, airy
**Elements**: Cards, navbars, modals, overlays

### Neomorphism (Soft UI)
Soft shadows creating subtle 3D effect, elements appear "pressed into" or "raised from" background, typically monochromatic.
**Vibe**: Soft, tactile, subtle
**Elements**: Buttons, cards, inputs
**Note**: Accessibility concerns, use carefully

### Claymorphism
Rounded, chunky elements with soft shadows, playful 3D appearance, often colorful.
**Vibe**: Playful, friendly, 3D
**Elements**: Buttons, icons, illustrations

### Brutalism
Raw, unstyled appearance, harsh contrasts, unconventional layouts, intentionally "undesigned".
**Vibe**: Bold, rebellious, avant-garde
**Elements**: Typography-heavy, stark colors, unusual grids

### Minimalism
Maximum restraint, limited colors (often grayscale), generous white space, typography-focused.
**Vibe**: Clean, elegant, confident
**Elements**: Everything simplified to essence

### Gradient Overload
Vibrant gradients everywhere, colorful, energetic, often with animation.
**Vibe**: Energetic, modern, attention-grabbing
**Elements**: Backgrounds, buttons, text, accents

### Swiss/International Style
Grid-based, clean typography, asymmetric layouts, limited color palette, often red/black/white.
**Vibe**: Professional, timeless, structured
**Elements**: Typography, grids, minimal graphics

### Flat Design
No shadows or gradients, solid colors, simple shapes, iconography-focused.
**Vibe**: Modern, clean, straightforward
**Elements**: Icons, buttons, UI elements

### Material Design
Google's design system, elevation through shadows, bold colors, responsive animations, card-based.
**Vibe**: Structured, colorful, consistent
**Elements**: Cards, FABs, ripple effects, elevation

### Dark Mode
Dark background (not pure black), light text, reduced eye strain, often with accent colors.
**Vibe**: Modern, dramatic, easier on eyes
**Elements**: Everything inverted thoughtfully

---

## COMPONENT CONCEPTS

### Hero Sections
- **Full-screen immersive**: Background image/video, centered content, minimal UI
- **Split hero**: Content left, visual right (or reversed)
- **Centered with floating**: Centered text, product image floating/overlapping
- **Minimal text-only**: Just typography, no images, extra-large headline
- **Interactive preview**: Live product demo or animation as hero

### Navigation
- **Sticky transparent**: Starts transparent, becomes solid on scroll
- **Mega menu**: Dropdown reveals organized grid of links/content
- **Hamburger to X**: Mobile menu icon that animates
- **Bottom tab bar**: Mobile-first, fixed bottom navigation
- **Sidebar drawer**: Slide-in navigation panel from left/right
- **Breadcrumbs**: Horizontal path showing location hierarchy

### Cards
- **Hover lift**: Card elevates on hover with shadow increase
- **Tilt on hover**: Subtle 3D rotation following cursor
- **Expand on click**: Card grows to reveal more content
- **Flip card**: Rotate to show back side with different content
- **Glass card**: Frosted glass effect with backdrop blur
- **Outlined minimal**: Just border, no background, clean

### Buttons
- **Gradient fill**: Colorful gradient background
- **Outlined ghost**: Transparent with border, fills on hover
- **Pill-shaped**: Fully rounded ends
- **Icon + text**: Icon inside button with label
- **Expanding**: Width increases on hover showing more text
- **Morphing**: Shape changes on interaction
- **Pulsing**: Subtle pulse animation to draw attention

### Forms
- **Floating labels**: Label moves up when input focused
- **Inline validation**: Real-time feedback as you type
- **Multi-step wizard**: Progress indicator, steps revealed sequentially
- **Auto-complete**: Suggestions appear as you type
- **Password strength**: Visual indicator of password quality
- **File upload drag-drop**: Drag zone with preview

### Modals/Overlays
- **Center modal**: Darkened backdrop, centered content box
- **Slide-in panel**: Drawer from right/left
- **Bottom sheet**: Slides up from bottom (mobile-friendly)
- **Fullscreen takeover**: Covers entire viewport
- **Lightbox**: Image viewer with navigation
- **Toast notification**: Small temporary message (corner)

### Tables/Data
- **Zebra striping**: Alternating row colors
- **Sticky header**: Column headers stay visible on scroll
- **Expandable rows**: Click to reveal detail
- **Sortable columns**: Click header to sort
- **Filterable**: Input above columns to filter
- **Card view toggle**: Switch between table and card grid

---

## INTERACTION PATTERNS

### Hover States
- **Shadow increase**: Element lifts on hover
- **Color shift**: Background/text color changes
- **Underline appear**: Line slides in under text
- **Scale up**: Element grows slightly
- **Glow effect**: Soft glow around element
- **Cursor change**: Pointer transforms (e.g., custom cursor)

### Click/Tap Feedback
- **Ripple effect**: Circular animation from tap point (Material)
- **Button press**: Element "pushes down" briefly
- **Color flash**: Quick color change confirming action
- **Checkmark animation**: Animated check appearing
- **Shake**: Brief shake for errors
- **Bounce**: Elastic bounce after click

### Scroll Interactions
- **Parallax**: Elements move at different speeds
- **Fade in on scroll**: Content appears as you reach it
- **Sticky elements**: Nav/headers stick to top
- **Scroll progress**: Bar showing page read progress
- **Infinite scroll**: New content loads automatically
- **Scroll snap**: Sections snap into place
- **Scroll-triggered animations**: Elements animate when visible

### Loading States
- **Skeleton screens**: Gray placeholder shapes of content
- **Pulse animation**: Element pulses while loading
- **Spinner**: Circular loading indicator
- **Progress bar**: Linear bar showing completion
- **Shimmer effect**: Moving gradient suggesting loading
- **Dots animation**: 3 dots bouncing/fading

### Transitions
- **Slide in/out**: Content slides from direction
- **Fade in/out**: Opacity change
- **Scale in/out**: Grows from center or shrinks
- **Rotate in**: Spinning entrance
- **Blur transition**: One view blurs while next sharpens
- **Wipe**: New content wipes across old

### Microinteractions
- **Like button heart**: Empty to filled with bounce
- **Toggle switch**: Slide animation
- **Checkbox check**: Animated checkmark
- **Star rating**: Fill/unfill with hover preview
- **Counter increment**: Number ticks up animated
- **Copy to clipboard**: Button shows "Copied!" feedback

---

## TYPOGRAPHY CONCEPTS

### Headline Styles
- **Oversized hero**: Massive display text, dominant
- **Gradient text**: Text with gradient fill
- **Outlined/stroked**: Just outline of letters
- **Mixed sizes**: Words at different sizes for emphasis
- **All caps bold**: Uppercase heavy weight
- **Serif elegant**: Classic serif for sophistication

### Text Hierarchy
- **Scale progression**: Clear size differences (e.g., 48px → 32px → 24px → 16px)
- **Weight variation**: Use weight (light/regular/bold) instead of size
- **Color hierarchy**: Primary/secondary text colors
- **Spacing**: Generous line-height and paragraph spacing

### Special Text Effects
- **Typewriter animation**: Text types out character by character
- **Text reveal**: Text appears from behind mask
- **Glitch effect**: Digital distortion animation
- **Fade-in words**: Words appear sequentially
- **Highlight**: Background color behind inline text

---

## COLOR CONCEPTS

### Palette Approaches
- **Monochromatic**: Single hue with different shades
- **Complementary**: Opposite colors on color wheel
- **Analogous**: Adjacent colors on wheel
- **Triadic**: Three evenly spaced colors
- **Brand + neutral**: Brand color with grays
- **Dark + accent**: Dark background with bright accent

### Color Usage
- **Primary action**: Bright color for main CTA
- **Semantic colors**: Red=error, green=success, yellow=warning, blue=info
- **Background gradients**: Subtle gradient instead of solid
- **Overlay colors**: Semi-transparent color layer over image
- **Border accents**: Colored border on one edge
- **Hover color shift**: Color changes on interaction

---

## SPACING CONCEPTS

### White Space Strategies
- **Generous padding**: Lots of breathing room in components
- **Tight grouping**: Related items close together
- **Section separation**: Large gaps between page sections
- **Asymmetric spacing**: More space on one side for visual interest

### Density Options
- **Compact**: Minimal space, information-dense
- **Comfortable**: Balanced spacing, easy to scan
- **Spacious**: Maximum white space, luxury feel

---

## MOTION CONCEPTS

### Animation Speeds
- **Instant**: Immediate, no animation (for critical actions)
- **Fast**: 150-200ms (small interactions)
- **Medium**: 300-400ms (most transitions)
- **Slow**: 500-800ms (dramatic entrances)

### Easing/Timing
- **Linear**: Constant speed (rarely used)
- **Ease-out**: Fast start, slow end (most common)
- **Ease-in**: Slow start, fast end (exits)
- **Ease-in-out**: Slow start, fast middle, slow end (smooth)
- **Bounce**: Elastic bounce effect (playful)
- **Spring**: Natural spring physics (modern, fluid)

### Animation Patterns
- **Stagger**: Items animate in sequence with delay
- **Cascade**: Wave effect across multiple items
- **Zoom on load**: Page elements scale up on entry
- **Slide from edge**: Content enters from screen edge
- **Rotate in**: Elements spin as they appear

---

## IMAGE TREATMENTS

### Image Styles
- **Full bleed**: Image extends to edges, no padding
- **Rounded corners**: Soft corners on images
- **Circular**: Fully round images (profiles)
- **Duotone**: Two-color filter effect
- **Grayscale**: Black and white
- **Overlay**: Dark/colored layer over image for text contrast
- **Blur background**: Sharp subject, blurred bg
- **Aspect ratio lock**: Consistent proportions (16:9, 4:3, 1:1)

### Image Layouts
- **Hero background**: Full-width image behind content
- **Grid gallery**: Uniform grid of images
- **Masonry gallery**: Pinterest-style varied heights
- **Carousel/slider**: Horizontal scrolling images
- **Lightbox**: Click to enlarge in overlay
- **Parallax background**: Image moves slower than scroll
- **Split screen image**: Half image, half content

---

## USAGE TIPS

**Combine patterns:**
"Glassmorphism cards in bento grid with hover lift"
"Dark mode with gradient accents and smooth transitions"
"Minimalist centered layout with oversized typography"

**Reference by name:**
"Stripe-style pricing cards"
"Apple-like hero section"
"Material Design buttons with ripple"
"Airbnb-style image grid"

**Describe the feeling:**
"Clean and spacious like Notion"
"Energetic and colorful like Spotify"
"Professional and structured like LinkedIn"
"Playful and rounded like Duolingo"
