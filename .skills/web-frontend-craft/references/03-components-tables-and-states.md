# 03: Desktop Components, Data Tables & Essential States

Every desktop interface should handle dense data cleanly, respond to every control, and render gracefully across all 4 lifecycle states.

---

## 1. Interactive Completeness (No Dead UI)

- Every sidebar link, top navbar item, table sort header, filter pill, search bar, pagination button, and modal form must perform a real UI update.
- Never wire visible buttons to dummy `"Coming soon"` toasts.

---

## 2. Core Desktop Patterns

- **KPI & Metric Strip:**
  - 3–4 columns on desktop (`grid-cols-1 sm:grid-cols-2 xl:grid-cols-4 gap-4`).
  - Clean surface, `1px` subtle border, muted label (`13px`), bold `tabular-nums` value (`24–28px`), and quiet delta indicator (`+12.4%` in `#047857` or `-3.1%` in `#DC2626`). No decorative background sparklines unless real data is plotted.
- **Data Tables (`TanStack Table` style):**
  - Sticky header (`12px` semibold muted text), comfortable row height (`48px–52px`), subtle row hover (`bg-black/[0.02]`), `1px` horizontal dividers.
  - Numeric/currency columns right-aligned with `tabular-nums` and `whitespace-nowrap`.
  - Include toolbar above table: Search input + Filter pills/select + Column/Export actions.
  - Include pagination bar below table (`Menampilkan 1–10 dari 48`).
- **Forms & Inputs:**
  - Clear visible `<label>` above every input (never rely solely on placeholder text).
  - Minimum `38px–42px` height on desktop, inline validation messages below fields, and disabled/loading state on submit buttons.

---

## 3. The 4 Essential Visual States

1. **Ready (Normal):** Balanced whitespace, crisp alignment, real domain data.
2. **Loading State:** Shape-matched skeleton shimmer placeholders with explicit heights/widths to prevent Cumulative Layout Shift (CLS).
3. **Empty State:** Clean vector icon (`40px`), concise 1-line explanation, and a primary CTA to resolve (e.g., `"Reset Filter"` or `"Tambah Data Pertama"`).
4. **Error State:** Human-readable message with a clear non-destructive `"Coba Lagi"` button.
