# 05: Web Libraries, Icons, Color Tokens, Grids & Ecosystem

Never default to the same generic look for every website. Pick **one intentional palette/token system, one typography pairing, one icon family, and the right-sized library stack** for the prompt's domain.

---

## 1. UI/UX Component Libraries & Styling

| Library | Type | Key Strength | Best For |
| :--- | :--- | :--- | :--- |
| **Tailwind CSS** | Utility-First CSS | Controls styling, grid, and spacing directly via HTML classes without switching CSS files. | Almost all modern web projects |
| **shadcn/ui** | Copy-Paste Primitives | Not a rigid npm black-box — component code is copied into your project for 100% customization. Also available as `shadcn-vue` and `shadcn-svelte`. | Professional apps & custom design systems |
| **Radix UI / Reka UI / Bits UI** | Headless UI | Provides full UI logic & accessibility (keyboard nav, screen reader, focus trap) with zero forced styling. | Foundation for custom components |
| **DaisyUI** | Tailwind Plugin | Shortens verbose Tailwind chains into clean classes like `btn-primary` or `card`. | Rapid prototyping & fast builds |
| **Mantine / MUI / Ant Design** | Full Component Library | Complete suite with dozens of ready components (date pickers, notifications, tables). | Internal dashboards & enterprise apps |

---

## 2. Icon Libraries (Strict 1-Family Rule per Project)

Pick **one** icon library and keep stroke weight consistent across the entire app. Never mix emojis into UI controls.

| Library | Character & Specs | Package / Source |
| :--- | :--- | :--- |
| **Lucide Icons** | Gold standard for modern UIs (`lucide-react`, `lucide-vue-next`), 1,500+ icons, clean `2px` stroke, lightweight. | `lucide-react`, `lucide.dev` |
| **Phosphor Icons** | 9,000+ icons with 6 weights (`Thin`, `Light`, `Regular`, `Bold`, `Fill`, `Duotone`) — ideal for active (`Fill`) vs inactive (`Regular`) menu states. | `@phosphor-icons/react`, `@phosphor-icons/web` |
| **Heroicons** | Built by the Tailwind CSS team; pixel-tuned specifically for `24px`, `20px`, and `16px` grids. | `@heroicons/react`, `heroicons.com` |
| **Tabler Icons** | Open-source, crisp `1.5px–2px` stroke with thousands of technical & business icons. | `@tabler/icons-react`, `tabler.io/icons` |
| **Remix Icon** | Sharp geometric dual-style (line + fill) for gaming, esports, media, & business. | `remixicon`, `remixicon.com` |
| **Iconify** | Universal framework when you must render multiple icon sets (including brand logos like Simple Icons) through one component. | `@iconify/react`, `iconify.design` |

---

## 3. Color Palettes & Semantic Design Tokens

Instead of guessing random hex codes, use semantic token systems (`background`, `foreground`, `primary`, `muted`, `destructive`):

- **Radix Colors:** 12-step color scale engineered for UI — each step guarantees readable text contrast and supports Light & Dark Mode automatically.
- **Tailwind Default Palette (OKLCH):** Balanced perceptual brightness across `Slate`, `Zinc`, `Neutral`, `Indigo`, `Emerald`, etc.
- **Chroma.js / Colord:** Lightweight JS libraries for dynamic color manipulation (auto-darkening user themes, checking WCAG contrast ratios).
- **Generator Tools:** `Realtime Colors`, `UI Colors`, `Coolors`.

### 10 Curated Domain Palettes (Never Recycle One Default)

| # | Palette Name | Best For | Canvas | Surface | Text | Primary Accent |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | **Swiss Editorial** | Agencies, Magazines, Architecture | `#F7F6F2` | `#FFFFFF` | `#111111` | `#E11D48` (Crimson) |
| 2 | **Warm Terracotta** | Food, Hospitality, Lifestyle, Craft | `#FAF8F5` | `#FFFFFF` | `#1C1917` | `#C2410C` (Terracotta) |
| 3 | **Nordic Sage** | Health, Wellness, Sustainability, SaaS | `#F4F7F5` | `#FFFFFF` | `#14261C` | `#15803D` (Forest) |
| 4 | **Crisp Cobalt** | B2B SaaS, E-Commerce, Travel | `#F8FAFC` | `#FFFFFF` | `#0F172A` | `#2563EB` (Cobalt) |
| 5 | **Midnight Espresso** | Gaming, Luxury, Audio, Coffee | `#12100E` | `#1B1815` | `#F5EFE6` | `#D97706` (Amber Gold) |
| 6 | **Tokyo Vermilion** | Gaming Top-Up, Esports, Streetwear | `#111113` | `#1A1A1E` | `#F4F4F5` | `#F97316` (Vermilion) |
| 7 | **Deep Burgundy** | Fashion, Wine, Editorial Luxury | `#160D10` | `#211419` | `#FAF5F6` | `#E11D48` (Rosewood) |
| 8 | **Nordic Slate & Mint** | Fintech, Crypto, Trading, Analytics | `#0B1116` | `#121B22` | `#F1F5F9` | `#10B981` (Mint) |
| 9 | **Monochrome Ink** | Portfolios, Legal, Docs, DevTools | `#FFFFFF` | `#F4F4F5` | `#09090B` | `#09090B` (Pure Ink) |
| 10 | **Blueprint Indigo** | Engineering, Cloud, Enterprise | `#F5F7FA` | `#FFFFFF` | `#0F172A` | `#4338CA` (Deep Indigo) |

---

## 4. Grid Layout, Data Grid (Tables), & Bento/Draggable Grid

Separate the three meanings of "Grid" cleanly:

1. **Page Layout (CSS Grid & Flexbox):**
   - Use **Native CSS Grid / Flexbox** or Tailwind utilities (`grid`, `grid-cols-12`, `gap-4`) for Bento Grids and responsive column layouts. No external library needed.
2. **Data Grid (Complex Tables):**
   - **TanStack Table (`@tanstack/react-table`):** Headless standard for sorting, filtering, pagination, and row selection with full styling control.
   - **AG Grid:** Industry standard for heavy tables with 10,000+ rows, pivoting, and Excel-like export.
3. **Interactive / Draggable Grid:**
   - **Gridstack.js / React-Grid-Layout:** For user-customizable dashboards where widgets can be dragged and resized.
   - **dnd-kit:** Lightweight modern drag-and-drop for Kanban boards (Trello-style) and sortable lists.

---

## 5. Essential Complementary Libraries

- **Animation & Micro-interactions:** `Motion` (`motion` / `framer-motion`) for component transitions & layout animations; `GSAP (GreenSock)` for complex `ScrollTrigger` landing pages.
- **Charts & Data Visualization:** `Recharts` / `Tremor` for clean customizable dashboard charts; `Chart.js` / `Apache ECharts` for high-performance canvas charts; `TradingView Lightweight Charts` for financial/candlestick data.
- **Forms & Validation:** `React Hook Form` / `Superforms` (Svelte) + `Zod` for strict schema validation.
- **State Management & Data Fetching:** `TanStack Query` (React/Vue/Svelte Query) for caching + effortless handling of the 4 required UI states (*Loading skeleton, Empty state, Error retry, Success data*); `Zustand` (React) / `Pinia` (Vue) for lean global state.
- **Command Palette, Toasts & Maps:** `cmdk` (`⌘K`), `Sonner`, `MapLibre GL` / `Leaflet` (keyless OpenStreetMap / Esri tiles only).

---

## 6. Typography Pairings & Desktop Layout Blueprints

| Pairing | Display / Headings | Body / UI | Mono / Numbers | Best For |
| :--- | :--- | :--- | :--- | :--- |
| **Editorial Classic** | `Instrument Serif` / `Newsreader` | `DM Sans` | `JetBrains Mono` | Magazines, Agencies, Luxury |
| **Modern Geometric** | `Space Grotesk` | `Inter` | `IBM Plex Mono` | Gaming, Tech, DevTools |
| **Swiss Grotesk** | `Bricolage Grotesque` | `Plus Jakarta Sans` | `Fira Code` | Creative SaaS, Portfolios |
| **Technical Precision** | `IBM Plex Sans` | `IBM Plex Sans` | `IBM Plex Mono` | Fintech, Trading, Enterprise |
| **Clean Humanist** | `Outfit` | `Manrope` | `JetBrains Mono` | E-Commerce, Lifestyle, Travel |

### 5 Layout Archetypes
1. **SaaS Dashboard & Analytics:** Collapsible Sidebar (`240px`) + Top Utility Bar (`56px`, `⌘K`) → 4-Col KPI Strip (`tabular-nums`) → `8/4` Chart + Breakdown → `TanStack Table`.
2. **Editorial / Marketing Landing:** Sticky Navbar (`64px`, max 5 links + 1 CTA) → Asymmetric/Editorial Hero → Trust Strip → Bento / Alternating Features → Transparent Pricing → Multi-Col Footer.
3. **E-Commerce / Top-Up Storefront:** Sticky Header → Editorial Banner → Category/Filter Rail + Multi-Col Grid → Split-Pane Checkout (`8/4`) or Slide-Over Cart Drawer.
4. **Developer Tool / Admin Console:** Split-Pane / Master-Detail → Code/Log Viewer (`Shiki`/`Monaco`) → `1px`-divided status table → Slide-Over Inspector Drawer.
5. **Fintech / Trading Terminal:** *Nordic Slate & Mint* or *Editorial Light* → `TradingView Lightweight Charts` → Order Book & Positions (`tabular-nums`) → Order Entry Panel.
