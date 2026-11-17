# Product Requirements Document (PRD): WebCraft-Skill-AI

> **Author:** Ananda Azizul Akbar (`@Azizulakbar89`)  
> **Derived From:** `MobileCraft-Skill-AI`  
> **Target:** Desktop Website, Web Application, Dashboard, & Editorial Frontend Craft  
> **Version:** 1.1.0

---

## 1. Executive Summary & Vision

**WebCraft-Skill-AI** adalah sistem instruksi, aturan desain (*design rules*), dan referensi ekosistem library untuk AI Coding Agents (Cursor, Windsurf, Antigravity, GitHub Copilot, Claude Code) agar menghasilkan **antarmuka website desktop yang tenang, presisi, fungsional, berkelas, sesuai konteks prompt, dan bebas dari "AI visual slop"**.

---

## 2. Masalah yang Diselesaikan (Problem Statement)

1. **AI Visual & Default Slop:** Mengulang tampilan yang sama (`#09090B + #3B82F6 + Inter + Lucide`), gradient ungu-biru neon, `blur-3xl` glow orbs, badge `✨ AI-Powered`, grid ikon pastel warna-warni, dan "boxes inside boxes".
2. **Context Drift (Keluar Konteks dari Prompt):** Menyelipkan hero marketing/pricing ke dalam dashboard internal, atau mengarang backend/DB/auth boilerplate yang tidak diminta.
3. **Dead UI & Incomplete Flows:** Link navigasi, filter, sort, atau tombol yang hanya memunculkan toast `"Coming soon"`.
4. **Salah Pilih Library & Ikon:** Mencampur banyak keluarga ikon atau memakai library berat yang tidak tepat guna.

---

## 3. Prinsip Inti, Context Lock & Anti-Slop Copywriting

### 3.1. Prompt Context Lock (Wajib Dipatuhi Sebelum Coding)
1. **Domain & Archetype Lock:** Kunci jenis produk (Dashboard vs Landing Page vs Storefront vs DevTool) sebelum menulis kode.
2. **Scope Boundary:** Hanya bangun frontend/UI/UX kecuali backend/database diminta secara eksplisit.
3. **Bahasa & Mata Uang:** Ikuti bahasa dan lokalitas prompt (`Rp` / `$`) dengan data realistis.

### 3.2. Anti-AI-Slop Visual & Copywriting Rules
- **No Default AI Look:** Jangan mendaur ulang satu palet/font/ikon yang sama untuk semua proyek.
- **Color Restraint:** Gunakan **1 warna aksen utama** + skala netral; warna semantik (hijau/merah/kuning) hanya untuk status nyata.
- **Banned Visuals:** Dilarang gradient neon ungu-biru, `blur-3xl` orbs, rainbow pastel icon grid, dot-pill spam (`● LIVE`), emoji di UI kontrol, dan fake browser chrome / macOS window dots.
- **Anti-Slop Copywriting:** Dilarang memakai kalimat klise AI seperti *"Revolutionize"*, *"Unleash the power of"*, *"Next-Gen AI-Powered"*, atau *"Elevate your workflow"*. Gunakan copy yang spesifik, ringkas, dan langsung menjelaskan fungsi.

---

## 4. Desktop UI/UX & Ergonomics Requirements

| Aspek | Standar WebCraft |
| :--- | :--- |
| **Viewport & Grid** | Responsif `375px`–`1440px+`. Marketing `max-w-[1280px]`; App/Dashboard `100dvh` dengan collapsible sidebar (`240px–260px`). |
| **Pointer & Keyboard** | `:hover`, `:focus-visible` (`2px` ring), `Tab` order, `Esc` untuk tutup modal/drawer, dan `⌘K` / `Ctrl+K` Command Palette untuk web app. |
| **Typography & Numbers** | `tabular-nums`, `whitespace-nowrap`, `shrink-0` pada angka/harga/tabel; batas lebar bacaan `60–75ch`. |
| **4 Required UI States** | **1) Ready**, **2) Loading Skeleton**, **3) Empty State + CTA**, **4) Error State + Retry**. |
| **Accessibility** | Kontras `>= 4.5:1` (WCAG AA), semantic landmarks, `aria-label` untuk tombol ikon, dan `prefers-reduced-motion`. |

---

## 5. Ekosistem Library Lengkap (5 Kategori Utama)

### 5.1. UI/UX Component Libraries & Styling
- **Tailwind CSS:** Utility-first CSS untuk styling, grid, dan spacing langsung di markup.
- **shadcn/ui (`shadcn-vue`, `shadcn-svelte`):** Copy-paste primitives yang 100% dapat dikustomisasi untuk custom design system.
- **Radix UI / Reka UI / Bits UI:** Headless UI dengan aksesibilitas penuh (keyboard nav, screen reader, focus trap) tanpa styling bawaan.
- **DaisyUI:** Plugin Tailwind untuk rapid prototyping (`btn-primary`, `card`).
- **Mantine / MUI / Ant Design:** Full component library untuk dashboard internal & aplikasi skala enterprise.

### 5.2. Icon Libraries (Wajib 1 Keluarga per Project & Stroke Seragam)
- **Lucide Icons** (`lucide-react`, `lucide-vue-next`): 1.500+ ikon bersih (`2px` stroke), ringan.
- **Phosphor Icons:** 9.000+ ikon dengan 6 ketebalan (`Thin`, `Light`, `Regular`, `Bold`, `Fill`, `Duotone`) — ideal untuk membedakan menu aktif (`Fill`) vs tidak aktif (`Regular`).
- **Heroicons:** Dibuat tim Tailwind CSS, optimal untuk grid `24px`, `20px`, `16px`.
- **Tabler Icons & Remix Icon:** Koleksi open-source ribuan ikon rapi untuk teknis, bisnis, dan gaming.
- **Iconify:** Kerangka universal jika harus memanggil berbagai set (termasuk logo brand Simple Icons) lewat satu komponen.

### 5.3. Palet Warna & Design Tokens
- Gunakan token semantik (`background`, `foreground`, `primary`, `muted`, `destructive`).
- **Radix Colors:** Skala warna 12-langkah yang teruji kontrasnya untuk Light & Dark Mode.
- **Tailwind Default Palette (OKLCH):** Skala `Slate`, `Zinc`, `Neutral`, `Indigo`, `Emerald`, dll. dengan kecerahan seimbang.
- **Chroma.js / Colord:** Manipulasi warna dinamis & cek rasio kontras WCAG di JS.
- **Generator Pendukung:** `Realtime Colors`, `UI Colors`, `Coolors`.
- **10 Palet Kurasi + 5 Typography Pairings** tersedia di `references/05-web-libraries-icons-and-layouts.md`.

### 5.4. Grid Layout, Data Grid (Tabel), & Bento/Draggable Grid
- **Layout Halaman:** Native **CSS Grid / Flexbox** atau Tailwind (`grid`, `grid-cols-12`, `gap-4`) untuk Bento Grid & kolom responsif (tanpa library eksternal).
- **Data Grid (Tabel Kompleks):** `TanStack Table` (`@tanstack/react-table`) untuk sorting, filtering, pagination, row selection; `AG Grid` untuk puluhan ribu baris, pivot, dan export ala Excel.
- **Interactive / Draggable Grid:** `Gridstack.js / React-Grid-Layout` untuk dashboard widget yang bisa digeser & diubah ukurannya; `dnd-kit` untuk Kanban & sortable list.

### 5.5. Library Pelengkap Penting
- **Animasi & Micro-interactions:** `Motion` (`motion` / `Framer Motion`) untuk transisi komponen & layout; `GSAP (GreenSock)` untuk `ScrollTrigger` kompleks.
- **Charts & Visualisasi Data:** `Recharts / Tremor` untuk grafik dashboard bersih; `Chart.js / Apache ECharts` untuk kanvas berkinerja tinggi; `TradingView Lightweight Charts` untuk finansial.
- **Form & Validasi Input:** `React Hook Form` / `Superforms` (Svelte) + `Zod`.
- **State Management & Data Fetching:** `TanStack Query` (React/Vue/Svelte Query) untuk caching & penanganan 4 state wajib (*Loading skeleton, Empty state, Error retry, Success data*); `Zustand` (React) / `Pinia` (Vue) untuk global state ringkas.

---

## 6. Pre-Delivery QA Self-Audit Checklist

Sebelum menyerahkan hasil ke pengguna, agent wajib memastikan:
- [ ] **Context Check:** Tidak ada fitur/section/backend di luar permintaan prompt.
- [ ] **Anti-Slop Check:** 0 neon gradient ungu-biru, 0 `blur-3xl`, 0 pastel icon grid, 0 emoji di kontrol UI, 0 copywriting klise.
- [ ] **Icon & Font Check:** Hanya 1 icon library dipakai dengan stroke konsisten, `tabular-nums` aktif pada semua angka.
- [ ] **Interactivity Check:** Semua tab, filter, search, modal/drawer, dan form bekerja nyata + 4 state UI tersedia.
- [ ] **Responsive & A11y Check:** Tidak ada horizontal overflow, `:focus-visible` jelas, `Esc` menutup overlay.
