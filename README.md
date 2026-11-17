<div align="center">
  <h1>🖥️ WebCraft</h1>
  <p>
    <strong>Desktop Website & Web App UI/UX Skill, Dual-Session & Anti-Slop Ruleset for AI Coding Agents</strong><br>
    <em>Ubah AI agent Anda dari penghasil template generik menjadi Senior Desktop UI/UX Designer & Frontend Engineer.</em>
  </p>
  <p>
    <a href="https://github.com/Azizulakbar89/Frontend-Website-Skill/stargazers"><img src="https://img.shields.io/github/stars/Azizulakbar89/Frontend-Website-Skill?style=for-the-badge&logo=github&color=111827" alt="Stars"></a>
    <img src="https://img.shields.io/badge/Focus-Desktop%20Web%20UI%2FUX-C2410C?style=for-the-badge" alt="Focus Desktop Web UI/UX">
    <img src="https://img.shields.io/badge/Sessions-Admin%20%26%20Non--Admin-15803D?style=for-the-badge" alt="Dual Session Admin & Non-Admin">
    <img src="https://img.shields.io/badge/Stack-React%20%7C%20Vue%20%7C%20Svelte%20%7C%20HTML-4338CA?style=for-the-badge" alt="Stack">
  </p>
</div>

> **Author:** Ananda Azizul Akbar ([@Azizulakbar89](https://github.com/Azizulakbar89))  
> **Derived From:** [MobileCraft-Skill-AI](https://github.com/Azizulakbar89/MobileCraft-Skill-AI)  
> **Repository:** [Azizulakbar89/Frontend-Website-Skill](https://github.com/Azizulakbar89/Frontend-Website-Skill)

---

## 🎯 Kenapa Pakai WebCraft?

Sebagian besar AI coding agent saat diminta membuat website desktop selalu mengulang **"AI Slop"** yang sama:
- Selalu memakai tampilan **dark-blue default** (`#09090B + #3B82F6 + Inter + Lucide`) untuk semua jenis website.
- Gradasi ungu-biru neon, lingkaran `blur-3xl` di belakang hero, badge `✨ AI-Powered`, dan kotak ikon pastel warna-warni.
- **Keluar konteks dari prompt (*Context Drift*):** Diminta membuat *dashboard internal*, malah menyelipkan hero marketing & tabel pricing; diminta *frontend*, malah mengarang backend & SQL schema.
- **Hanya membuat 1 sisi tampilan:** Membuat web toko/kontraktor/klinik hanya untuk pelanggan, tanpa menyediakan konsol **Admin/Operator** yang terhubung.

**WebCraft** membuang seluruh kebiasaan buruk tersebut. Skill ini mengarahkan AI (**Antigravity, Cursor, Windsurf, GitHub Copilot, Claude Code**) untuk menghasilkan website desktop yang tenang, presisi, kaya interaksi nyata, sesuai konteks prompt, dan otomatis peka membangun **Sesi Admin & Non-Admin**.

---

## ⚡ Before vs After: AI Slop vs WebCraft

| Aspek Desain | ❌ Output AI Bawaan (Slop) | ✅ Standar WebCraft |
| :--- | :--- | :--- |
| **Palet & Token Warna** | Selalu `#09090B + #3B82F6` atau gradasi neon ungu-biru + `blur-3xl` | **10 Palet Domain Terkalibrasi** + Semantic Tokens (`Radix Colors`, `OKLCH`, `Chroma.js`) |
| **Tipografi & Angka** | 1 font generik untuk semua web; angka tabel bergeser | **5 Typography Pairings** + wajib `tabular-nums`, `whitespace-nowrap`, & `max-w-[65ch]` |
| **Ikonografi** | Campur aduk Lucide + FontAwesome + emoji (`🚀`, `✨`) | **1 Keluarga Ikon Konsisten** (`Phosphor`, `Tabler`, `Remix`, `Heroicons`, `Lucide`, `Iconify`) |
| **Sesi Pengguna** | Hanya tampilan statis satu arah atau tombol mati (`Coming soon`) | **Dual-Session Otomatis:** Sesi **Non-Admin (Klien/User)** & **Admin** dengan *shared live state* |
| **Grid & Tabel** | Kartu bertumpuk (*boxes inside boxes*) tanpa sorting/filter | Pemisahan tegas: **CSS Grid/Flexbox** (layout), **TanStack Table / AG Grid** (tabel), **dnd-kit** |
| **Keyboard & A11y** | Tidak ada `:focus-visible`, modal tidak bisa ditutup `Esc` | Wajib `:focus-visible`, `Esc` dismiss, `⌘K` Command Palette, & `>= 4.5:1` kontras |
| **4 State Wajib** | Hanya *happy path* | Wajib mendukung **Ready**, **Loading Skeleton**, **Empty State + CTA**, & **Error Retry** |

---

## 🧠 Fitur Utama Skill WebCraft

### 1. Prompt Context Lock & Dual-Session Sensitivity (Admin & Non-Admin)
- **Context Lock:** AI mengunci domain, archetype (Dashboard vs Landing Page vs Storefront vs DevTool), bahasa, dan mata uang (`Rp` / `$`) sebelum menulis kode—tanpa mengarang backend yang tidak diminta.
- **Otomatis Sesi Admin & Non-Admin:** Untuk aplikasi interaktif (E-Commerce, Top-Up, Kontraktor, Klinik/Mental Health, Booking, SaaS, LMS), AI otomatis menyediakan:
  - **Sesi Non-Admin (Pengguna/Klien):** Antarmuka pelanggan/klien yang bersih (katalog, checkout, portal progres, form pengajuan).
  - **Sesi Admin (Operator/Back-Office):** Konsol `100dvh` dengan sidebar `240px`, KPI strip, tabel manajemen, chart, dan drawer CRUD/approval.
  - **Shared Live State + Role Switcher:** Perubahan di Sesi Klien (misal: buat pesanan/pengajuan) langsung muncul di Sesi Admin untuk disetujui/diproses, dengan *Role Switcher* (`Klien` ↔ `Admin`) yang rapi di top bar.

### 2. 10 Palet Warna Terkurasi (Zero Default AI Look)
| Palet | Cocok Untuk | Canvas | Surface | Accent |
| :--- | :--- | :--- | :--- | :--- |
| **Swiss Editorial** | Agency, Majalah, Arsitektur | `#F7F6F2` | `#FFFFFF` | `#E11D48` (Crimson) |
| **Warm Terracotta** | Kontraktor, Kuliner, Hospitality | `#FAF8F5` | `#FFFFFF` | `#C2410C` (Terracotta) |
| **Nordic Sage** | Mental Health, Kesehatan, SaaS | `#F4F7F5` | `#FFFFFF` | `#15803D` (Forest) |
| **Crisp Cobalt** | B2B SaaS, E-Commerce, Travel | `#F8FAFC` | `#FFFFFF` | `#2563EB` (Cobalt) |
| **Midnight Espresso** | Gaming, Luxury, Audio, Kopi | `#12100E` | `#1B1815` | `#D97706` (Amber Gold) |
| **Tokyo Vermilion** | Top-Up Game, Esports, Streetwear | `#111113` | `#1A1A1E` | `#F97316` (Vermilion) |
| **Deep Burgundy** | Fashion, Wine, Editorial Luxury | `#160D10` | `#211419` | `#E11D48` (Rosewood) |
| **Nordic Slate & Mint** | Fintech, Crypto, Trading | `#0B1116` | `#121B22` | `#10B981` (Mint) |
| **Monochrome Ink** | Portfolio, Legal, Docs, DevTools | `#FFFFFF` | `#F4F4F5` | `#09090B` (Pure Ink) |
| **Blueprint Indigo** | Engineering, Cloud, Top-Up Light | `#F5F7FA` | `#FFFFFF` | `#4338CA` (Deep Indigo) |

### 3. Ekosistem Library Lengkap (5 Kategori)
- **UI & Styling:** `Tailwind CSS`, `shadcn/ui` (`shadcn-vue`, `shadcn-svelte`), `Radix UI / Reka UI / Bits UI`, `DaisyUI`, `Mantine / MUI / Ant Design`.
- **Icon Libraries (Pilih 1 per Project):** `Lucide Icons`, `Phosphor Icons` (6 ketebalan: Thin s/d Fill & Duotone), `Heroicons`, `Tabler Icons`, `Remix Icon`, `Iconify`.
- **Color Tokens & Tools:** `Radix Colors` (12-step scale), `Tailwind OKLCH`, `Chroma.js / Colord`, `Realtime Colors`, `UI Colors`, `Coolors`.
- **Grid Systems:** Native CSS Grid / Flexbox (Bento & Layout), `TanStack Table` & `AG Grid` (Data Tables), `Gridstack.js / React-Grid-Layout` & `dnd-kit` (Draggable Dashboard / Kanban).
- **Motion, Charts, Forms & State:** `Motion` (`Framer Motion`), `GSAP` (`ScrollTrigger`), `Recharts / Tremor`, `Chart.js / Apache ECharts`, `TradingView Lightweight Charts`, `React Hook Form / Superforms + Zod`, `TanStack Query`, `Zustand / Pinia`, `cmdk` (`⌘K`), `Sonner`, `MapLibre / Leaflet` (tile bebas API key).

### 4. 5 Blueprint Layout Desktop
1. **SaaS Dashboard & Analytics:** Collapsible Sidebar (`240px`) + Top Utility Bar (`56px`, `⌘K`) → 4-Col KPI Strip → `8/4` Chart & Breakdown → `TanStack Table`.
2. **Editorial / Marketing Landing Page:** Sticky Navbar (`64px`) → Focused Hero → Trust Strip → Bento / Alternating Features → Transparent Pricing → Footer.
3. **E-Commerce & Top-Up Storefront:** Sticky Header → Editorial Banner → Category/Filter Rail + Product Grid → Split-Pane Checkout (`8/4`) / Cart Drawer.
4. **Developer Tool / Admin Console:** Split-Pane / Master-Detail → Code/Log Viewer (`Shiki`/`Monaco`) → Dense Status Table → Slide-Over Inspector Drawer.
5. **Fintech / Trading Terminal:** *Nordic Slate & Mint* / *Editorial Light* → `TradingView Lightweight Charts` → Order Book (`tabular-nums`) → Order Entry Panel.

---

## 🚀 Cara Pemasangan (1 Menit)

### Quick Install via Terminal
Jalankan di root folder proyek website Anda:

```bash
git clone https://github.com/Azizulakbar89/Frontend-Website-Skill.git .temp-webcraft
cp -r .temp-webcraft/.cursor .temp-webcraft/.skills .temp-webcraft/.windsurfrules .temp-webcraft/.github .
rm -rf .temp-webcraft
```

### Panduan per AI Agent
| AI Tool | Lokasi File | Cara Kerja |
| :--- | :--- | :--- |
| **Google Antigravity** | `.skills/web-frontend-craft/` *(atau `~/.gemini/antigravity/skills/`)* | Otomatis terbaca saat Anda meminta pembuatan website / web app desktop |
| **Cursor IDE** | `.cursor/rules/` (`web-ui-core.mdc`, `web-motion-ergonomics.mdc`) | Aktif otomatis (`alwaysApply: true`) di semua file UI web |
| **Windsurf** | `.windsurfrules` | Otomatis diterapkan oleh Cascade di setiap generasi UI |
| **GitHub Copilot** | `.github/copilot-instructions.md` | Mengarahkan Copilot Chat & inline suggestions |
| **Claude Code** | `.skills/web-frontend-craft/SKILL.md` | Referensikan di `CLAUDE.md` proyek Anda |

---

## 📂 Struktur Repositori

```text
Frontend-Website-Skill/
├── README.md                               # Dokumentasi lengkap repositori ini
├── .cursor/rules/
│   ├── web-ui-core.mdc                     # Context Lock, Dual-Session, Anti-Slop & Library rules
│   └── web-motion-ergonomics.mdc           # Keyboard (⌘K, Esc), Grid & Accessibility rules
├── .github/
│   └── copilot-instructions.md             # Instruksi untuk GitHub Copilot
├── .skills/web-frontend-craft/
│   ├── SKILL.md                            # Instruksi utama skill web-ui-craft
│   └── references/
│       ├── 01-desktop-hierarchy-and-anti-slop.md
│       ├── 02-desktop-ergonomics-and-navigation.md
│       ├── 03-components-tables-and-states.md
│       ├── 04-motion-keyboard-and-a11y.md
│       └── 05-web-libraries-icons-and-layouts.md
└── .windsurfrules                          # Aturan untuk Windsurf IDE
```

---

<p align="center">
  Dibuat oleh <strong>Ananda Azizul Akbar</strong> (<a href="https://github.com/Azizulakbar89">@Azizulakbar89</a>) • MIT License
</p>
