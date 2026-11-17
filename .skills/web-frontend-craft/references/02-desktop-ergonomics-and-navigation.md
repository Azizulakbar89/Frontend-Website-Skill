# 02: Desktop Ergonomics, Grids & Navigation Architecture

Desktop interfaces are operated with a mouse/trackpad and keyboard on wide horizontal viewports (`1280px–1440px+`), while still needing clean responsiveness down to `375px`.

---

## 1. Layout Grids & Containers

- **Marketing / Editorial Sites:**
  - Centered container `max-w-[1280px]` (or `max-w-[1200px]`) with `px-6 lg:px-8` horizontal gutter.
  - Use a `12-column` CSS Grid (`grid-cols-12 gap-6`) for asymmetric editorial splits (`col-span-7` + `col-span-5`) and bento grids.
- **Web Apps, Dashboards & Terminals:**
  - Full-height `100dvh` app shell (`flex h-dvh overflow-hidden`) with independent scrollable workspace so the navigation stays anchored.
  - Collapsible Left Sidebar (`240px–260px` expanded, `68px` icon-only collapsed, drawer on `< 1024px`).
  - Sticky Top Utility Bar (`56px` height): Breadcrumb/Page Title on left, `⌘K` Quick Search in center/right, Notification & Profile menu on right.

---

## 2. Navigation Discipline

- **Top Navbar (Marketing):** `64px` height, max 5–6 top-level links, 1 clear primary CTA button. Never crowd 10+ links or multi-row mega-banners at the top.
- **Sidebar (Web Apps):** Group links into max 2–3 logical sections with plain muted section labels (`11px` uppercase). Active item uses subtle surface tint + bold text, never neon gradient pills.
- **Contextual Drawers & Modals:**
  - Use **slide-over drawers** (`400px–520px` width) for inspecting/editing records without losing table context.
  - Use centered **dialog modals** (`max-w-md` or `max-w-lg`) only for focused confirmations or short forms. Always support `Esc` and backdrop click to dismiss.
  - Never use browser-native `alert()`, `confirm()`, or `prompt()`.

---

## 3. Responsive Breakpoints

- `>= 1280px` (`xl`): Full desktop multi-column & expanded sidebar.
- `1024px–1279px` (`lg`): Compact sidebar or 2-column grids.
- `< 768px` (`sm`): Sidebar collapses into slide-over drawer; multi-column grids stack cleanly to 1–2 columns; tables scroll horizontally inside an explicit `overflow-x-auto` wrapper.

---

## 4. Dual-Session Architecture (Admin & Non-Admin)

When building interactive frontend apps (Storefronts, Portals, SaaS, Booking, Clinics), automatically support both roles cleanly:

1. **Subtle Session Switcher:** Place a compact, high-contrast role toggle (`Sesi: Pengguna` / `Sesi: Admin`) in the top utility bar or account dropdown — never clutter the customer hero with admin banners.
2. **Shared Live State:** Actions taken in **Non-Admin** (e.g., placing an order, submitting a booking, writing a review) must appear immediately in **Admin**, and Admin actions (e.g., approving an order, toggling item availability, updating status) must reflect immediately in **Non-Admin**.
3. **Distinct Session Ergonomics:**
   - **Non-Admin Session:** Customer/user-focused layout (Navbar + Catalog/Portal + Checkout/Form + User History).
   - **Admin Session:** Operator console (`100dvh` Sidebar `240px` + Top Utility Bar `56px` + KPI Strip + Filterable/Sortable Management Table + Slide-Over CRUD/Approval Drawer).
