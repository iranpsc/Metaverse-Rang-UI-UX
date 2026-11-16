<div align="center">

# 🎨 MetaRang UI/UX & Design System
### User Interface Architecture, User Experience & Design System of the MetaRang Parallel World

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![Open Source](https://img.shields.io/badge/Open%20Source-DesignOps-00d2ff.svg)](https://github.com/iranpsc/Metaverse-Rang-UI-UX)
[![Base Standard](https://img.shields.io/badge/Base%20Standard-Dark%20%7C%20RTL%20(Persian)-1a1a2e.svg)](#)
[![Platforms](https://img.shields.io/badge/Platforms-Web%20%7C%20WebGL%20%7C%20Mobile%20%7C%20VR-purple.svg)](https://metarang.com)
[![Languages](https://img.shields.io/badge/i18n-RTL%20%26%20LTR%20(6%20Languages)-gold.svg)](https://world.metarang.com)

**English** | **[فارسی](#-معماری-رابط-کاربری-تجربه-کاربری-و-سیستم-دیزاین-متارنگ)**

[Official Website (External Index)](https://metarang.com) • [MetaRang World (Internal Index)](https://world.metarang.com) • [Tasks & Issues](https://github.com/iranpsc/Metaverse-Rang-UI-UX/issues) • [Contribution Guide](./CONTRIBUTING.md)

</div>

---

## 🌌 About This Repository

**MetaRang (متارنگ)** is an international 3D parallel world metaverse platform with Iranian roots and a decentralized architecture, initiated in April 2021 (Spring 1400 SH) to pioneer futuristic digital interactions, virtual economy, and 3D urban architecture.

This repository serves as the official open-source **Design System**, **Visual Standards**, and **UI/UX Architecture** hub across all layers of the MetaRang ecosystem. Designed with an open-source, decentralized philosophy, all UI/UX tasks are published as **Issues**, empowering designers worldwide to contribute, iterate on colors and components, submit concepts, and earn official MetaRang citizen rewards and recognition.

---

## 🔗 Official Master Figma Files

Approved and finalized designs are reviewed by the Design System Management team and consolidated into the official master Figma workspaces:

| Product / Layer | Domain / Environment | Official Master Figma Link |
| :--- | :--- | :--- |
| **External Index** | `metarang.com` | [Open External Index Master Figma](https://www.figma.com/design/qyvJ4Sjw4h5gRIrE9KotBY/ui-next?node-id=1863-759&p=f&t=ZhzzROkrsum2bANV-0) |
| **Internal Index** | `world.metarang.com` | [Open Internal Index Master Figma](https://www.figma.com/design/lHgvuzgJhUFACNpMBJK0jI/ui?node-id=34-1989&p=f&t=eTHiDSZ99JfQoJ9T-0) |
| **3D Environments (WebGL & VR)** | `3D Spatial & Headset UI` | [Open 3D Environments Master Figma](https://www.figma.com/design/Rs8cdjPco3ovjPHFyxZPuC/3d-scien?node-id=2309-2&p=f&t=HWmizeDXyRz7sBW7-0) |

---

## 🏗️ Complete Directory Architecture

The repository is strictly structured across core design tokens, platforms, themes (`dark`/`light`), and text directions (`rtl`/`ltr` supporting 6 languages: Persian, English, Arabic, Russian, Chinese, and Turkish):

<pre>
Metaverse-Rang-UI-UX/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── ui-feature-request.md        # Template for new UI feature tasks
│   │   ├── ux-improvement.md            # Template for UX enhancement proposals
│   │   └── design-bug.md                # Template for visual/layout bug reports
│   └── PULL_REQUEST_TEMPLATE.md         # Mandatory PR checklist (Base Dark+RTL, Citizen ID, Tokens)
│
├── 00-design-system/                    # Core Design System (Single Source of Truth)
│   ├── tokens/                          # W3C Design Tokens (JSON)
│   │   ├── colors-dark.json
│   │   ├── colors-light.json
│   │   └── typography.json
│   ├── foundations/                     # Grids, color palettes, 6-language typography scales
│   ├── components/                      # Core UI components (Glassmorphism cards, buttons, modals)
│   ├── icons-and-assets/                # Optimized SVG icon packs & brand mascots (e.g., Jelly)
│   └── CHANGELOG.md                     # Versioned changelog of the Design System
│
├── 01-external-index/                   # External Index UI (metarang.com)
│   ├── web-desktop/                     # Windows & Desktop Web version
│   │   ├── dark/
│   │   │   ├── rtl/                     # [BASE REFERENCE] Persian, Arabic
│   │   │   └── ltr/                     # English, Russian, Chinese, Turkish
│   │   └── light/
│   │       ├── rtl/
│   │       └── ltr/
│   └── web-mobile/                      # Mobile Web & PWA version
│       ├── dark/
│       │   ├── rtl/                     # [BASE REFERENCE]
│       │   └── ltr/
│       └── light/
│           ├── rtl/
│           └── ltr/
│
├── 02-internal-index/                   # Internal Index UI (world.metarang.com)
│   ├── web-desktop/                     # Citizen Dashboard, Land Management & Desktop Portal
│   │   ├── dark/
│   │   │   ├── rtl/                     # [BASE REFERENCE]
│   │   │   └── ltr/
│   │   └── light/
│   │       ├── rtl/
│   │       └── ltr/
│   └── web-mobile/                      # Mobile Internal Index & Android TWA version
│       ├── dark/
│       │   ├── rtl/                     # [BASE REFERENCE]
│       │   └── ltr/
│       └── light/
│           ├── rtl/
│           └── ltr/
│
├── 03-3d-environments/                  # 3D Spatial & In-World UI (Unity WebGL & VR)
│   ├── webgl-desktop/                   # Desktop WebGL 3D environment HUD & menus
│   │   ├── dark/
│   │   │   ├── rtl/                     # [BASE REFERENCE]
│   │   │   └── ltr/
│   │   └── light/
│   │       ├── rtl/
│   │       └── ltr/
│   ├── webgl-mobile/                    # Mobile WebGL (Touch controllers & responsive HUD)
│   │   ├── dark/
│   │   │   ├── rtl/                     # [BASE REFERENCE]
│   │   │   └── ltr/
│   │   └── light/
│   │       ├── rtl/
│   │       └── ltr/
│   └── vr-headset/                      # VR Headset Spatial UI & 3D interactions
│       ├── dark/
│       │   ├── rtl/                     # [BASE REFERENCE]
│       │   └── ltr/
│       └── light/
│           ├── rtl/
│           └── ltr/
│
├── 04-community-concepts/               # Futuristic concepts & community redesign proposals
│   └── [HM-xxxx-username]/              # Dedicated folder per contributor by Citizen ID
│
├── 05-contributors/                     # Contributor Registry (For attribution & reward allocation)
│   ├── TEMPLATE-contributor.json        # Standard JSON profile template
│   └── HM-2000007.json                  # Sample registered designer profile
│
├── CONTRIBUTING.md                      # Comprehensive contribution & handoff guidelines
├── LICENSE                              # GNU AGPL-3.0 Open Source License
└── README.md                            # Bilingual repository documentation
</pre>

### 📌 Core Design Governance Rules
1. **Base Reference Standard (`Dark + RTL`):** All new interfaces must first be designed and delivered in **Dark Mode** and **RTL (Persian)** as the primary source of truth. **Light Mode** and **LTR** variants are subsequently localized into their corresponding directories.
2. **Synchronized Versioning:** UI/UX release versions strictly follow MetaRang's core technical versioning standard (e.g., `v1.1.26`, `v2.0.0`).
3. **Mandatory Design System Sync:** Whenever a designer introduces or modifies colors, typography, design tokens (`.json`), or vector icons (`.svg`), they must update `00-design-system/` within the same Pull Request so the Design System Lead can integrate them into the Master Figma files.

---

## 🔄 Designer Contribution Workflow

1. **Pick an Issue:** Browse the [Issues](https://github.com/iranpsc/Metaverse-Rang-UI-UX/issues) tab and claim an open task (or open a new issue for your futuristic concept).
2. **Fork & Branch:** Fork this repository and create a descriptive branch (e.g., `feat/internal-index-wallet-dark-rtl`).
3. **Design in Personal Figma:** Create your designs in your personal Figma workspace using `00-design-system/` tokens, and set sharing permissions to **Public ("Anyone with the link can view")**.
4. **Prepare Export Deliverables:**
   - Export high-resolution screens as `.png` and comprehensive user flows/specs as `.pdf` into the exact target directory (e.g., `02-internal-index/web-desktop/dark/rtl/`).
   - Update modified `.svg` icons and `.json` tokens inside `00-design-system/`.
   - Document your **Personal Figma Link**, issue number, and designer notes in the target folder's `README.md`.
5. **Register Citizen Identity (Required):** Create or update your profile file in `05-contributors/` named after your official MetaRang Citizen ID (e.g., `HM-2000007.json`), including your portfolio and social links.
6. **Submit a Pull Request:** Open a PR and complete the checklist. Once reviewed and approved, your work will be merged into the repository and integrated into MetaRang's Master Figma files under your name.

---

## 📐 File Naming & Format Standards

* **Naming Pattern (`kebab-case`):**
  `[metarang-version]_[screen-or-feature]_[theme]_[direction].[ext]`
  * *Example:* `v1.1.26_citizen-dashboard_dark_rtl.png`
* **Allowed File Formats:**
  * `.svg` — Optimized vector icons and brand graphics
  * `.png` / `.webp` — Screen exports (`2x` for web/desktop, `1x` for previews)
  * `.pdf` — Complete design specifications and user flow documentation
  * `.json` — Design tokens (`00-design-system/`) and contributor profiles (`05-contributors/`)
  * `.md` — Documentation and Figma reference links

---

## ⚖️ License

This repository is licensed under the **GNU AGPL-3.0 License**. All merged designs become part of MetaRang's open-source infrastructure, with permanent attribution preserved for every contributing designer.

---
---

<div dir="rtl">

# 🎨 معماری رابط کاربری، تجربه کاربری و سیستم دیزاین متارنگ
### مخزن رسمی و متن‌باز طراحی رابط کاربری و سیستم دیزاین جهان موازی متارنگ

**متارنگ (MetaRang)** یک پلتفرم متاورس بین‌المللی و جهان موازی سه‌بعدی با ریشه ایرانی و معماری غیرمتمرکز است که از بهار ۱۴۰۰ آغاز شده و با هدف خلق تجربه‌ای آینده‌نگرانه در تعاملات دیجیتال، اقتصاد مجازی و شهرسازی سه‌بعدی توسعه می‌یابد.

[وب‌سایت اصلی (ایندکس خارجی)](https://metarang.com) • [پورتال و دنیای متارنگ (ایندکس داخلی)](https://world.metarang.com) • [لیست تسک‌ها (Issues)](https://github.com/iranpsc/Metaverse-Rang-UI-UX/issues) • [راهنمای مشارکت](./CONTRIBUTING.md)

---

## 🌌 درباره این ریپازیتوری

این مخزن مرجع رسمی و متن‌باز **سیستم دیزاین (Design System)**، **استانداردهای بصری** و **معماری رابط کاربری (UI/UX)** در تمامی لایه‌های اکوسیستم متارنگ است. با توجه به ماهیت آینده‌نگرانه و غیرمتمرکز متارنگ، تمامی نیازهای طراحی در قالب **Issue** در این ریپازیتوری تعریف می‌شوند و طراحان از سراسر جهان می‌توانند با مشارکت در این مخزن، ضمن توسعه رابط کاربری متارنگ، امتیاز و پاداش‌های شهروندی متارنگ را دریافت کنند.

---

## 🔗 مراجع رسمی Figma متارنگ (Official Master Files)

در اکوسیستم متارنگ، فایل‌های تاییدشده و نهایی پس از بررسی Pull Requestها توسط تیم مدیریت سیستم دیزاین در فایل‌های مرکزی زیر تجمیع و منتشر می‌شوند:

| بخش / محصول | دامنه / محیط | لینک دسترسی مستقیم Figma (Master) |
| :--- | :--- | :--- |
| **ایندکس خارجی (External Index)** | `metarang.com` | [مشاهده فایل Figma ایندکس خارجی](https://www.figma.com/design/qyvJ4Sjw4h5gRIrE9KotBY/ui-next?node-id=1863-759&p=f&t=ZhzzROkrsum2bANV-0) |
| **ایندکس داخلی (Internal Index)** | `world.metarang.com` | [مشاهده فایل Figma ایندکس داخلی](https://www.figma.com/design/lHgvuzgJhUFACNpMBJK0jI/ui?node-id=34-1989&p=f&t=eTHiDSZ99JfQoJ9T-0) |
| **محیط‌های سه‌بعدی (3D & VR UI)** | `WebGL & VR Headset` | [مشاهده فایل Figma محیط‌های سه‌بعدی](https://www.figma.com/design/Rs8cdjPco3ovjPHFyxZPuC/3d-scien?node-id=2309-2&p=f&t=HWmizeDXyRz7sBW7-0) |

---

## 🏗️ معماری و ساختار دایرکتوری‌ها

فایل‌های طراحی بر اساس نوع محصول، پلتفرم هدف، تم رنگی (`dark`/`light`) و جهت‌گیری زبان (`rtl`/`ltr` با پشتیبانی از ۶ زبان: فارسی، انگلیسی، عربی، روسی، چینی و ترکی) دسته‌بندی شده‌اند:

<div dir="ltr">
<pre>
Metaverse-Rang-UI-UX/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── ui-feature-request.md        # قالب ایشو برای طراحی بخش جدید
│   │   ├── ux-improvement.md            # قالب ایشو برای بهبود تجربه کاربری
│   │   └── design-bug.md                # قالب ایشو برای باگ‌های بصری
│   └── PULL_REQUEST_TEMPLATE.md         # چک‌لیست اجباری بررسی PR (نسخه پایه Dark+RTL، شناسه شهروندی، توکن‌ها)
│
├── 00-design-system/                    # هسته مرکزی سیستم دیزاین متارنگ (مرجع تمام نسخه‌ها)
│   ├── tokens/                          # توکن‌های رنگ، تایپوگرافی، گردی گوشه‌ها (JSON)
│   │   ├── colors-dark.json
│   │   ├── colors-light.json
│   │   └── typography.json
│   ├── foundations/                     # اصول پایه (شبکه‌بندی، رنگ‌های برند، تایپوگرافی ۶ زبان)
│   ├── components/                      # کامپوننت‌های پایه (کارت‌های شیشه‌ای/Glassmorphism، دکمه‌ها، مودال‌ها)
│   ├── icons-and-assets/                # پک آیکون‌های اختصاصی SVG و کاراکترهای برند (مثل Jelly)
│   └── CHANGELOG.md                     # تاریخچه تمام تغییرات سیستم دیزاین
│
├── 01-external-index/                   # رابط کاربری ایندکس خارجی (دامنه metarang.com)
│   ├── web-desktop/                     # نسخه تحت وب دسکتاپ و ویندوز
│   │   ├── dark/
│   │   │   ├── rtl/                     # [نسخه پایه و مرجع] فارسی، عربی
│   │   │   └── ltr/                     # انگلیسی، روسی، چینی، ترکی
│   │   └── light/
│   │       ├── rtl/
│   │       └── ltr/
│   └── web-mobile/                      # نسخه تحت وب موبایل و PWA
│       ├── dark/
│       │   ├── rtl/                     # [نسخه پایه و مرجع]
│       │   └── ltr/
│       └── light/
│           ├── rtl/
│           └── ltr/
│
├── 02-internal-index/                   # رابط کاربری ایندکس داخلی (دامنه world.metarang.com)
│   ├── web-desktop/                     # داشبورد شهروندی، مدیریت املاک و پورتال دسکتاپ
│   │   ├── dark/
│   │   │   ├── rtl/                     # [نسخه پایه و مرجع]
│   │   │   └── ltr/
│   │   └── light/
│   │       ├── rtl/
│   │       └── ltr/
│   └── web-mobile/                      # نسخه موبایل ایندکس داخلی و Android TWA
│       ├── dark/
│       │   ├── rtl/                     # [نسخه پایه و مرجع]
│       │   └── ltr/
│       └── light/
│           ├── rtl/
│           └── ltr/
│
├── 03-3d-environments/                  # رابط کاربری محیط‌های سه‌بعدی (Unity WebGL & VR)
│   ├── webgl-desktop/                   # نسخه دسکتاپ WebGL محیط سه‌بعدی (HUD و منوها)
│   │   ├── dark/
│   │   │   ├── rtl/                     # [نسخه پایه و مرجع]
│   │   │   └── ltr/
│   │   └── light/
│   │       ├── rtl/
│   │       └── ltr/
│   ├── webgl-mobile/                    # نسخه موبایل WebGL (کنترلرهای لمسی و HUD بهینه)
│   │   ├── dark/
│   │   │   ├── rtl/                     # [نسخه پایه و مرجع]
│   │   │   └── ltr/
│   │   └── light/
│   │       ├── rtl/
│   │       └── ltr/
│   └── vr-headset/                      # نسخه هدست واقعیت مجازی (Spatial UI و تعاملات سه‌بعدی)
│       ├── dark/
│       │   ├── rtl/                     # [نسخه پایه و مرجع]
│       │   └── ltr/
│       └── light/
│           ├── rtl/
│           └── ltr/
│
├── 04-community-concepts/               # ایده‌ها، کانسپت‌های آینده‌نگرانه و بازطراحی‌های پیشنهادی طراحان
│   └── [HM-xxxx-username]/              # پوشه اختصاصی طراح با شناسه شهروندی
│
├── 05-contributors/                     # بانک اطلاعاتی طراحان مشارکت‌کننده (جهت ثبت رزومه و تخصیص پاداش)
│   ├── TEMPLATE-contributor.json        # فایل الگو برای ثبت مشخصات طراح
│   └── HM-2000007.json                  # نمونه فایل ثبت‌شده با شناسه شهروندی متارنگ
│
├── CONTRIBUTING.md                      # راهنمای جامع مشارکت، قوانین PR و استانداردهای طراحی
├── LICENSE                              # مجوز متن‌باز (GNU AGPL-3.0)
└── README.md                            # فایل مستندات دوزبانه مخزن
</pre>
</div>

### 📌 قوانین پایه معماری طراحی
1. **نسخه پایه و مرجع (Base Standard):** تمام طرح‌های جدید ابتدا باید در وضعیت **Dark Mode** و جهت **RTL (زبان فارسی)** طراحی و تحویل شوند. نسخه‌های **Light Mode** و **LTR** (برای زبان‌های انگلیسی، روسی، چینی، ترکی و عربی) بر پایه نسخه مرجع و در پوشه‌های متناظر خود تکمیل می‌گردند.
2. **هماهنگی نسخه‌بندی (Versioning):** شماره‌گذاری نسخه‌های UI/UX دقیقاً از استاندارد نسخه‌بندی فنی متارنگ (مانند `v1.1.26` یا `v2.0.0`) پیروی می‌کند.
3. **به‌روزرسانی هم‌زمان سیستم دیزاین:** هرگونه تغییر در پالت رنگی، تایپوگرافی، توکن‌های JSON یا افزودن آیکون‌های SVG جدید باید هم‌زمان توسط طراح در پوشه `00-design-system/` نیز اعمال شود تا مدیر سیستم دیزاین فرآیند یکپارچه‌سازی در فیگمای مرکزی را انجام دهد.

---

## 🔄 گردش کار مشارکت طراحان (Contribution Workflow)

1. **انتخاب تسک (Issue):** وارد بخش [Issues](https://github.com/iranpsc/Metaverse-Rang-UI-UX/issues) شوید و تسک مورد نظر خود را انتخاب کنید (یا برای ایده جدید خود یک ایشو ثبت نمایید).
2. **ساخت Fork و Branch:** مخزن را Fork کرده و یک برنچ با نام استاندارد بسازید (مثال: `feat/internal-index-wallet-dark-rtl`).
3. **طراحی در Figma شخصی:** طرح خود را در فضای فیگمای شخصی خود بر اساس توکن‌های `00-design-system/` طراحی کنید و دسترسی آن را روی حالت عمومی (**Anyone with the link can view**) قرار دهید.
4. **آماده‌سازی فایل‌های خروجی و Handoff:**
   - فایل‌های تصویری صفحات را با پسوند `.png` و مستندات کامل/فلوچارت را با پسوند `.pdf` در دایرکتوری دقیق مربوطه (مثلاً `02-internal-index/web-desktop/dark/rtl/`) قرار دهید.
   - فایل‌های آیکون `.svg` و توکن‌های `.json` تغییریافته را در مسیر `00-design-system/` آپدیت کنید.
   - لینک مشاهده فایل **Figma شخصی** خود، شماره ایشو و توضیحات تغییر را در فایل `README.md` همان پوشه ثبت نمایید.
5. **ثبت هویت شهروندی (الزامی برای امتیازدهی):** در پوشه `05-contributors/` یک فایل با نام شناسه شهروندی متارنگ خود (مثال: `HM-2000007.json`) ایجاد یا به‌روزرسانی کنید و مشخصات، لینک پورتفولیو و شبکه‌های اجتماعی خود را ثبت نمایید.
6. **ارسال Pull Request:** درخواست PR را ثبت کنید. پس از بررسی توسط تیم معماری و سیستم دیزاین متارنگ، طرح شما در مخزن اصلی Merge شده و به فایل‌های مرکزی Figma منتقل خواهد شد.

---

## 📐 استاندارد نام‌گذاری و فرمت فایل‌ها

* **الگوی نام‌گذاری فایل‌ها (`kebab-case`):**
  `[metarang-version]_[screen-or-feature]_[theme]_[direction].[ext]`
  * *مثال:* `v1.1.26_citizen-dashboard_dark_rtl.png`
* **فرمت‌های مجاز:**
  * `.svg` — آیکون‌ها و المان‌های برداری بهینه‌شده
  * `.png` / `.webp` — خروجی صفحات با رزولوشن `2x` برای وب و `1x` برای پیش‌نمایش
  * `.pdf` — مستندات کامل طراحی و User Flow
  * `.json` — توکن‌های طراحی در `00-design-system/` و پروفایل مشارکت‌کننده در `05-contributors/`
  * `.md` — مستندات متنی و ثبت لینک‌های Figma

---

## ⚖️ مجوز و مالکیت معنوی (License)

این پروژه تحت مجوز **GNU AGPL-3.0** منتشر شده است. تمامی طرح‌های پذیرفته‌شده بخشی از زیرساخت متن‌باز متارنگ محسوب می‌شوند و نام، پورتفولیو و شناسه شهروندی طراحان مشارکت‌کننده به صورت دائمی در تاریخچه مخزن و مستندات رسمی متارنگ ثبت خواهد شد.

</div>
