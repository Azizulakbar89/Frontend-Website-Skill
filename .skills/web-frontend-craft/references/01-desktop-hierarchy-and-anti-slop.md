# 01: Desktop Hierarchy, Context Lock & Anti-Slop Rules

Great desktop websites feel distinct, intentional, and tailored to their domain. AI slop happens when every website looks like the exact same dark-gray + neon-blue SaaS clone with glowing blobs, generic fonts, and filler copy.

---

## 1. Prompt Context Lock (Stay On-Topic)

1. **Match the Requested Product Type:**
   - Dashboard / Web App → App shell (`100dvh`, sidebar + utility bar + workspace). No marketing hero or pricing table.
   - Marketing / SaaS Landing → Editorial scroll (`max-w-[1280px]`, navbar + hero + value props + pricing + footer).
   - E-Commerce / Top-Up Storefront → Header + search + category/filter + multi-column grid + split-pane checkout or slide-over cart drawer.
2. **Realistic Domain Copy:** Populate tables, charts, and cards with authentic, domain-specific labels and numbers matching the prompt's language and currency.
3. **No Unrequested Backend:** Do not invent API servers, SQL schemas, or auth token boilerplate unless asked.

---

## 2. Anti-Default-Slop: Palette, Font & Icon Diversity

- **Never Recycle the "Default AI Look":** Do not default to `#09090B` + `#3B82F6` + `Plus Jakarta Sans` + `Lucide` for every project. Deliberately pick a matching palette, typography pairing, and icon library from [05-web-libraries-icons-and-layouts.md](file:///Users/azizul/vps/webcraft-skill/.skills/web-frontend-craft/references/05-web-libraries-icons-and-layouts.md):
  - _Gaming / Esports:_ **Tokyo Vermilion** or **Midnight Espresso** + `Space Grotesk` / `Inter` + **Remix Icon** or **Phosphor Icons**.
  - _Fintech / Trading:_ **Nordic Slate & Mint** or **Blueprint Indigo** + `IBM Plex Sans` / `IBM Plex Mono` + **Tabler Icons**.
  - _Editorial / Agency / Luxury:_ **Swiss Editorial** or **Deep Burgundy** + `Instrument Serif` / `DM Sans` + **Iconoir** or **Phosphor Thin**.
  - _Food / Lifestyle / Craft:_ **Warm Terracotta** or **Nordic Sage** + `Outfit` / `Manrope` + **Phosphor Icons**.
- **Color Restraint:** Use **one** primary brand accent + neutral surfaces. Reserve emerald/red/amber strictly for real status indicators.
- **Banned Desktop AI Clichés:**
  - NO purple-to-blue neon gradients (`#8A2BE2` → `#4169E1`) or `blur-3xl` glowing blobs.
  - NO rainbow pastel icon grids (4 cards each with blue/emerald/amber/purple translucent icon squares).
  - NO `✨ AI-Powered` / `● LIVE` dot-pill spam on every card header.
  - NO "boxes inside boxes" (wrapping every list item or metric in nested bordered cards).
  - NO fake browser windows or macOS `🔴🟡🟢` window dots unless requested as a mockup.

---

## 3. Desktop Typography & Numeric Discipline

- **Scale:**
  - Editorial Hero H1: `44–64px`, bold/extrabold (`700–800`), tight tracking (`-0.03em`), `leading-[1.08]`.
  - App Page Title: `22–28px`, bold (`700`), tracking `-0.02em`.
  - Section Header: `16–18px`, semibold (`600`).
  - Body / Table Cell: `14px`, regular/medium (`400–500`), readable line length `max-w-[65ch]`.
- **Tabular Numbers:** Always apply `font-variant-numeric: tabular-nums` to KPIs, financial figures, table columns, percentages, and timestamps. Keep currency symbols (`Rp`, `$`) attached with `whitespace-nowrap shrink-0`.

---

## 4. Iconography

- Enforce **one** icon library per project (`Phosphor`, `Tabler`, `Remix Icon`, `Iconoir`, `Lucide`, `Heroicons`, `Radix Icons`, or `Iconify`) with uniform stroke/weight.
- Never mix raw emojis (`🚀`, `📊`, `⚙️`) into navigation links, buttons, or table headers.
