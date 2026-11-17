# 04: Motion, Keyboard Ergonomics & Accessibility

Motion on desktop clarifies state transitions and acknowledges pointer/keyboard input — never to distract or slow down power users.

---

## 1. Pointer & Hover Micro-Interactions

- **Subtle Feedback:** Buttons, table rows, and cards should have crisp hover state transitions (`150ms ease`) and subtle active press feedback (`scale(0.98)`).
- **No Competing Loops:** Avoid simultaneous pulsing, floating, or bouncing animations across the page.
- **Respect Reduced Motion:** Always honor `@media (prefers-reduced-motion: reduce)` by disabling non-essential transforms and animations.

---

## 2. Keyboard Navigation & Shortcuts

- **Focus Rings:** Every interactive element (`button`, `a`, `input`, `select`, custom `[role="button"]`) must show a clear `:focus-visible` ring (`2px` solid accent with `2px` offset).
- **Standard Shortcuts for Web Apps:**
  - `Esc` closes any open modal, slide-over drawer, dropdown, or command palette.
  - `⌘K` / `Ctrl+K` opens the Command Palette (`cmdk`) for quick navigation and search in dashboards/tools.
  - Arrow keys navigate dropdown menus and tabs where appropriate.

---

## 3. Accessibility (WCAG AA)

- **Contrast:** Minimum `4.5:1` for body text and `3:1` for large headings and UI borders/icons.
- **Semantic Landmarks:** Use `<header>`, `<nav>`, `<main>`, `<aside>`, `<section>`, and `<footer>` properly.
- **Icon-Only Buttons:** Always provide `aria-label` (e.g. `aria-label="Tutup panel"`).
