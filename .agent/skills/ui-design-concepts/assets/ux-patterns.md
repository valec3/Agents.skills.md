# UX Patterns & User Flows

User experience concepts and interaction flows described conceptually, not technically.

---

## ONBOARDING PATTERNS

### Welcome Tour
**Flow**: User signs up → Welcome screen with key benefits → Step-by-step guided tour (3-5 steps) highlighting main features → Optional tutorial → Dashboard
**UX Goal**: Orient new users without overwhelming
**Key Moments**: Skip option, progress indicators, clear "Next" actions
**Best For**: Complex apps, SaaS, tools with learning curve

### Progressive Disclosure
**Flow**: Show basic features first → User completes initial action → Reveal more advanced features gradually → Full power user mode after several sessions
**UX Goal**: Prevent overwhelm, guide learning
**Key Moments**: Feature unlocks feel like rewards, clear advancement
**Best For**: Complex tools, educational apps, power user tools

### Empty States with Actions
**Flow**: New user sees empty dashboard → Helpful message: "Get started by..." → Clear CTA to create first item → Celebrate first creation
**UX Goal**: Convert empty state to first action quickly
**Key Moments**: Encouraging message, single clear action, immediate feedback
**Best For**: Content creation tools, task managers, any app that starts "empty"

### Quick Win First
**Flow**: Skip all setup → User completes one valuable action immediately → Then ask for account/setup → Continue with full features
**UX Goal**: Prove value before asking commitment
**Key Moments**: Instant utility, delayed signup, smooth transition
**Best For**: Tools, utilities, B2C apps

### Personalization Quiz
**Flow**: Welcome → "Tell us about yourself" quiz (3-7 questions) → Customize experience based on answers → Show personalized results
**UX Goal**: Tailor experience, increase engagement
**Key Moments**: Fun questions, see results immediately, optional
**Best For**: Content apps, e-commerce, recommendation engines

---

## NAVIGATION PATTERNS

### Persistent Top Nav
**UX**: Navigation always visible at top, scrolls away or becomes sticky
**User Expectation**: Always know where I am, quick access to main areas
**Interaction**: Click to navigate, dropdown menus for sub-pages
**Best For**: Content sites, marketing sites, shallow hierarchies

### Sidebar Navigation
**UX**: Fixed left sidebar with hierarchical menu, main content on right
**User Expectation**: App-like experience, nested navigation
**Interaction**: Collapsible sections, active state shows current page, can minimize entire sidebar
**Best For**: Apps, dashboards, deep hierarchies, SaaS

### Tab Navigation
**UX**: Horizontal tabs, only one active at a time, content area updates
**User Expectation**: Related content, quick switching, no page reload
**Interaction**: Click tab to switch view, visual active state
**Best For**: Detail pages, settings, dashboards with view modes

### Breadcrumbs
**UX**: Shows path from home to current page, clickable trail
**User Expectation**: Know location, navigate back up hierarchy
**Interaction**: Click any level to jump back
**Best For**: Deep sites, e-commerce categories, documentation

### Bottom Tab Bar (Mobile)
**UX**: Fixed bottom bar with 3-5 main sections, icons + labels
**User Expectation**: Native app feel, thumb-friendly navigation
**Interaction**: Tap to switch sections, current section highlighted
**Best For**: Mobile-first apps, main feature areas

### Mega Menu
**UX**: Hover/click navigation item, large dropdown shows organized links with optional images/descriptions
**User Expectation**: See all options, visual organization
**Interaction**: Hover or click to open, click links to navigate
**Best For**: Large sites, e-commerce, many categories

---

## SEARCH & DISCOVERY PATTERNS

### Instant Search (Type-ahead)
**Flow**: User types → Results appear immediately → User continues typing to refine → Click result
**UX Goal**: Fast discovery, no waiting
**Key Moments**: Results update in real-time, highlight matched text
**Best For**: Large content catalogs, e-commerce, knowledge bases

### Filter + Sort
**Flow**: User browses grid → Applies filters (sidebar or top bar) → Results update → Adjusts filters → Applies sorting
**UX Goal**: Refine large sets to find relevant items
**Key Moments**: Clear active filters, easy to clear, result count updates
**Best For**: E-commerce, job boards, directories, large catalogs

### Faceted Search
**Flow**: User searches → Results with multiple facets (category, price, date, etc.) → User clicks facet to drill down → Results narrow → User continues filtering
**UX Goal**: Progressive refinement through attributes
**Key Moments**: See available facets, counts per facet, multiple selection
**Best For**: E-commerce, research databases, complex filtering needs

### Saved Searches/Alerts
**Flow**: User performs search → "Save this search" option → User names it → Future results notify user
**UX Goal**: Return to important searches, passive discovery
**Key Moments**: Easy to save, manage saved searches, notification preferences
**Best For**: Job boards, real estate, marketplaces

### Recommendation Engine
**Flow**: User views item → "You might also like" section shows related items → User explores recommendations → Algorithm learns
**UX Goal**: Discovery beyond search, personalization
**Key Moments**: Relevant suggestions, explain why ("Because you viewed..."), refresh options
**Best For**: E-commerce, content platforms, streaming

---

## CONTENT INTERACTION PATTERNS

### Infinite Scroll
**Flow**: User scrolls down → New content loads automatically → User continues scrolling → Endless content
**UX Goal**: Frictionless browsing, no pagination clicks
**Key Moments**: Loading indicator, "You've reached the end" message
**Best For**: Social feeds, image galleries, news feeds
**Note**: Can harm SEO and make footer hard to reach

### Load More Button
**Flow**: User sees initial set → "Load More" button at bottom → Click loads next batch → Repeat
**UX Goal**: User-controlled loading, preserves footer access
**Key Moments**: Clear button, loading state, eventually reach end
**Best For**: Blogs, product listings, controlled browsing

### Pagination
**Flow**: User sees page 1 → Numbers at bottom → Click next page → New content loads
**UX Goal**: Traditional, SEO-friendly, clear position
**Key Moments**: Current page highlighted, "Previous/Next" always available, jump to page
**Best For**: Search results, product catalogs, traditional sites

### Tabs for Content Sections
**Flow**: User lands on page → Sees tabbed sections → Clicks tab to view different content → Content area updates
**UX Goal**: Organize related content without scrolling or new pages
**Key Moments**: Clear tab labels, active state, content updates smoothly
**Best For**: Product details, profiles, settings pages

### Accordion (Expandable Sections)
**Flow**: User sees list of titles → Clicks one to expand → Content reveals → Click another or same to collapse
**UX Goal**: Compact presentation, user explores at their pace
**Key Moments**: One or multiple open at once?, smooth animation, clear expand/collapse icon
**Best For**: FAQs, long content sections, mobile-friendly content

---

## FORM INTERACTION PATTERNS

### Multi-Step Forms (Wizard)
**Flow**: User starts form → Completes step 1 → "Next" to step 2 → Progress indicator shows position → Final step submits
**UX Goal**: Break complex forms into manageable chunks
**Key Moments**: Progress indicator, ability to go back, save progress
**Best For**: Signups, checkout, complex data entry

### Inline Validation
**Flow**: User fills field → On blur (or while typing), validation occurs → Immediate feedback (error or success) → User corrects
**UX Goal**: Catch errors early, guide correct entry
**Key Moments**: Real-time feedback, clear error messages, success indicators
**Best For**: All forms, especially long/complex ones

### Autosave
**Flow**: User types → After pause, form auto-saves → "Saved" indicator appears briefly → User continues
**UX Goal**: Never lose work, remove save anxiety
**Key Moments**: Subtle "Saving..." then "Saved" indicator, no interruption
**Best For**: Content editors, long forms, drafts

### Smart Defaults
**Flow**: Form opens pre-filled with smart guesses (location, previous choices, common values) → User adjusts only what's wrong → Submit
**UX Goal**: Minimize effort, speed completion
**Key Moments**: Obvious what's pre-filled, easy to change, helpful not creepy
**Best For**: Settings, preferences, repeat forms

### Conditional Fields
**Flow**: User selects option → Related fields appear/disappear based on selection → Form adapts to user's path
**UX Goal**: Show only relevant fields, reduce clutter
**Key Moments**: Smooth appearance/disappearance, logical conditions, clear why fields appear
**Best For**: Complex forms, personalized flows, conditional logic

---

## E-COMMERCE UX PATTERNS

### Quick View
**Flow**: User browsing grid → Hovers/clicks "Quick View" → Modal opens with product basics and add to cart → User adds or closes to continue browsing
**UX Goal**: Explore products without leaving browse page
**Key Moments**: Fast loading, essential info only, easy to close
**Best For**: Fashion, accessories, items with simple options

### Sticky Add to Cart
**Flow**: User scrolls product page → Add to cart button becomes sticky (follows scroll) → Always accessible to purchase
**UX Goal**: Remove friction from purchase decision
**Key Moments**: Appears after scrolling past main button, unobtrusive, clear price
**Best For**: Long product pages, detailed descriptions

### Cart Preview Drawer
**Flow**: User adds item → Drawer slides in from side showing cart contents → User can continue shopping or checkout → Drawer dismisses
**UX Goal**: Confirm add, provide quick cart access, keep shopping flow
**Key Moments**: Shows what was added, cart total, quick checkout option
**Best For**: E-commerce, services, any add-to-cart experience

### Wishlist/Save for Later
**Flow**: User finds item → Clicks heart/save icon → Item saved to list → User continues browsing → Later reviews saved items
**UX Goal**: Let users collect without committing, return later
**Key Moments**: Visual heart fill, access saved list, move from saved to cart
**Best For**: E-commerce, content bookmarking, inspiration

### Size/Variant Selector
**Flow**: User selects product → Chooses size/color/variant → Visual updates (if applicable) → Availability shows → Add to cart
**UX Goal**: Clear selection, show availability, prevent errors
**Key Moments**: Visual feedback, disabled unavailable options, clear selection
**Best For**: Clothing, products with variants

---

## FEEDBACK & CONFIRMATION PATTERNS

### Toast Notifications
**Flow**: User completes action → Small message appears in corner → Displays for 3-5 seconds → Auto-dismisses
**UX Goal**: Non-intrusive confirmation
**Key Moments**: Briefly visible, doesn't block content, shows success/error
**Best For**: Background actions, confirmations, non-critical messages

### Modal Confirmations
**Flow**: User clicks destructive action → Modal appears: "Are you sure?" → User confirms or cancels → Action completes or aborts
**UX Goal**: Prevent accidental destructive actions
**Key Moments**: Clear question, obvious confirm/cancel, explain consequences
**Best For**: Delete, destructive actions, critical decisions

### Inline Success Messages
**Flow**: User completes form/action → Success message appears in place → Provides next step or confirmation → Remains visible
**UX Goal**: Contextual confirmation, guide next action
**Key Moments**: Green checkmark, clear success message, suggest next action
**Best For**: Forms, settings changes, profile updates

### Loading States
**Flow**: User initiates action → Loading indicator appears → Action processes → Result shown
**UX Goal**: Show system is working, set expectations
**Key Moments**: Immediate feedback, progress indicator if long, informative (don't just show spinner)
**Best For**: All async actions, especially slow operations

### Empty States
**Flow**: User lands on empty section → Helpful message explains why it's empty → Clear CTA to add first item → Illustration or icon adds personality
**UX Goal**: Guide user to first action, prevent confusion
**Key Moments**: Encouraging message, clear action, optional preview of what full state looks like
**Best For**: New accounts, cleared lists, no search results

---

## SOCIAL INTERACTION PATTERNS

### Like/Favorite
**Flow**: User sees content → Clicks heart/star → Animates (fills with color, bounces) → Count increases → Click again to unlike
**UX Goal**: Express appreciation, save content
**Key Moments**: Satisfying animation, visible count, toggle on/off
**Best For**: Social media, content platforms, user-generated content

### Comment Threading
**Flow**: User reads post → Adds comment → Others reply to comment → Threads nest → User can expand/collapse threads
**UX Goal**: Organized discussions, follow conversations
**Key Moments**: Clear thread hierarchy, reply targets visible, collapse long threads
**Best For**: Forums, social platforms, collaborative tools

### Share Functionality
**Flow**: User finds content worth sharing → Clicks share → Modal/dropdown with options (social platforms, copy link, email) → User selects → Confirmation
**UX Goal**: Viral distribution, content reach
**Key Moments**: Multiple share options, copy link easy, native sharing on mobile
**Best For**: Content platforms, articles, products

### Follow/Subscribe
**Flow**: User discovers creator/topic → Clicks follow → Confirmation (button changes to "Following") → User sees content in feed → Can unfollow anytime
**UX Goal**: Content curation, personalization
**Key Moments**: Clear followed state, easy to unfollow, feed updates
**Best For**: Social platforms, content platforms, newsletters

### Reactions (Beyond Like)
**Flow**: User sees content → Clicks reaction picker → Selects from options (love, laugh, wow, sad, angry, etc.) → Reaction shows → Others see reaction counts
**UX Goal**: More expressive than binary like, emotional engagement
**Key Moments**: Quick picker, multiple options, see breakdown of reactions
**Best For**: Social platforms, community tools, expressive feedback

---

## DASHBOARD & DATA PATTERNS

### KPI Cards at Top
**Flow**: User opens dashboard → Immediately sees key metrics (users, revenue, growth, etc.) in card format → Can click for details
**UX Goal**: At-a-glance insights, quick status check
**Key Moments**: Big numbers, trend indicators (up/down), comparison to previous period
**Best For**: Analytics, business dashboards, admin panels

### Drill-Down Navigation
**Flow**: User sees high-level data → Clicks to drill into details → Sees sub-category → Can drill further or return
**UX Goal**: Explore data at different levels of detail
**Key Moments**: Breadcrumbs show path, easy back navigation, maintain context
**Best For**: Analytics, reporting, hierarchical data

### Time Range Selector
**Flow**: User views time-based data → Selects range (Today, Week, Month, Year, Custom) → Data updates to match
**UX Goal**: Compare periods, find relevant timeframe
**Key Moments**: Common presets, custom range picker, comparison mode optional
**Best For**: Analytics, reporting, time-series data

### Data Table with Actions
**Flow**: User views table → Can sort columns → Filter rows → Select items → Perform bulk actions → See updated results
**UX Goal**: Manage and manipulate data efficiently
**Key Moments**: Sortable columns, inline actions, bulk select, clear feedback
**Best For**: Admin panels, data management, records

### Real-Time Updates
**Flow**: User views dashboard → New data arrives → UI updates live → Optional notification of change → Smooth transition
**UX Goal**: Always current data, no manual refresh
**Key Moments**: Smooth updates, highlight what changed, not jarring
**Best For**: Monitoring, live data, collaborative tools

---

## MOBILE-SPECIFIC PATTERNS

### Pull to Refresh
**Flow**: User at top of list → Pulls down → Release → Refresh animation → New content loads
**UX Goal**: Mobile-native refresh mechanism
**Key Moments**: Visual indicator while pulling, satisfying animation, new content appears
**Best For**: Feeds, lists, mobile-first apps

### Swipe Actions
**Flow**: User swipes item left/right → Action buttons reveal (delete, archive, etc.) → User taps action or swipes back → Action completes
**UX Goal**: Quick actions without opening item
**Key Moments**: Smooth swipe, clear action icons/colors, undo option for destructive
**Best For**: Email, tasks, lists, mobile apps

### Bottom Sheet
**Flow**: User taps element → Panel slides up from bottom with details/actions → User interacts or dismisses → Sheet slides down
**UX Goal**: Thumb-friendly modal alternative
**Key Moments**: Smooth animation, can drag to dismiss, overlay content
**Best For**: Mobile filters, actions, detail views

### Thumb-Friendly Zones
**UX**: Interactive elements placed in easy-to-reach areas on phone (bottom third), important actions not at top edges
**User Expectation**: Can use with one hand, thumb reaches everything important
**Interaction**: Bottom navigation, floating action buttons, reachable targets
**Best For**: All mobile apps, mobile-first design

---

## USAGE EXAMPLES

**Describe complete flows:**
```
"Multi-step signup: email → password → personalization quiz → empty state with first action prompt"

"E-commerce browse: grid with filters → quick view modal → add to cart drawer → sticky checkout button"

"Dashboard experience: KPI cards at top → main chart with time selector → activity feed → data table with actions"
```

**Reference by feeling:**
```
"Onboarding feels like Duolingo - quick win first, playful, progressive"

"Search like Google - instant results, faceted filters, saved searches"

"Social interactions like Twitter - like, retweet, reply threading, real-time updates"
```

**Focus on key moments:**
```
"When user adds to cart, show confirmation toast + drawer preview, keep them shopping"

"Empty state should be encouraging, show example of what full state looks like, single clear CTA"

"Form validation happens on blur, inline errors, celebrates completion"
```
