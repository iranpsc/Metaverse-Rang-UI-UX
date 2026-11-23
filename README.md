<div align="center">

# 🎨 MetaRang UI/UX & Design System
### Automated Open-Source UI/UX Architecture, DesignOps & Design System of the MetaRang Parallel World

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![Open Source](https://img.shields.io/badge/Open%20Source-DesignOps-00d2ff.svg)](https://github.com/iranpsc/Metaverse-Rang-UI-UX)
[![Base Standard](https://img.shields.io/badge/Base%20Standard-Dark%20%7C%20RTL%20(Default)-1a1a2e.svg)](#)
[![Platforms](https://img.shields.io/badge/Platforms-Web%20%7C%20WebGL%20%7C%20Mobile%20%7C%20VR-purple.svg)](https://metarang.com)
[![Governance](https://img.shields.io/badge/Governance-Automated%20CI%20%26%20CODEOWNERS-14b8a6.svg)](./.github/workflows/pr-guard.yml)

**English** | **[فارسی](#-معماری-رابط-کاربری-تجربه-کاربری-و-سیستم-دیزاین-متارنگ)**

[Official Website (External Index)](https://metarang.com) • [MetaRang World (Internal Index)](https://world.metarang.com) • [Tasks & Issues](https://github.com/iranpsc/Metaverse-Rang-UI-UX/issues) • [Issue Standard](./.github/ISSUE_TEMPLATE/ISSUE-STANDARD.md) • [Contribution Guide](./CONTRIBUTING.md)

</div>

---

## 🌌 About This Repository

**MetaRang (متارنگ)** is an international 3D parallel world metaverse platform with Iranian roots and a decentralized architecture, initiated in April 2021 (Spring 1400 SH) to pioneer futuristic digital interactions, virtual economy, and 3D urban architecture.

This repository serves as the official open-source **Design System**, **Visual Standards**, and **Automated DesignOps UI/UX Architecture** hub across all layers of the MetaRang ecosystem. Every design task is standardized through structured YAML Issue Forms, automatically scaffolded into strict versioned directories with bilingual documentation, and protected by an automated Pull Request Quality Gatekeeper and `@iranpsc/ui-ux-manager` code ownership.

---

## 🔗 Official Master Figma Files

Approved and finalized designs are reviewed by `@iranpsc/ui-ux-manager` and consolidated into the official master Figma workspaces:

| Product / Layer | Domain / Environment | Official Master Figma Link |
| :--- | :--- | :--- |
| **External Index** | `metarang.com` | [Open External Index Master Figma](https://www.figma.com/design/qyvJ4Sjw4h5gRIrE9KotBY/ui-next?node-id=1863-759&p=f&t=ZhzzROkrsum2bANV-0) |
| **Internal Index** | `world.metarang.com` | [Open Internal Index Master Figma](https://www.figma.com/design/lHgvuzgJhUFACNpMBJK0jI/ui?node-id=34-1989&p=f&t=eTHiDSZ99JfQoJ9T-0) |
| **3D Environments (WebGL & VR)** | `3D Spatial & Headset UI` | [Open 3D Environments Master Figma](https://www.figma.com/design/Rs8cdjPco3ovjPHFyxZPuC/3d-scien?node-id=2309-2&p=f&t=HWmizeDXyRz7sBW7-0) |

---

## 🏗️ Complete Directory Architecture

Every UI/UX deliverable follows a deterministic, machine-verified directory hierarchy:

```text
<category>/<platform>/<theme>/<direction>/<slug>/<lang>/README.md
```

<pre>
Metaverse-Rang-UI-UX/
├── .gitattributes                       # Git LFS enforcement for *.glb & *.fbx
├── .github/
│   ├── CODEOWNERS                       # Mandatory merge approval by @iranpsc/ui-ux-manager
│   ├── PULL_REQUEST_TEMPLATE.md         # Bilingual PR template (Issue + Figma URL required)
│   ├── ISSUE_TEMPLATE/
│   │   ├── config.yml                   # Disables blank issues; links to ISSUE-STANDARD.md
│   │   ├── ISSUE-STANDARD.md            # Bilingual governance & directory rules
│   │   ├── ui-task.yml                  # Automated UI Task & Directory Generator form
│   │   ├── design-system-update.yml     # Design tokens & component update form
│   │   ├── design-bug.yml               # Visual / layout bug report form
│   │   └── ux-improvement.yml           # UX improvement proposal form
│   └── workflows/
│       ├── issue-scaffold.yml           # Auto-generates directories, v2/v3 versions & bilingual READMEs
│       └── pr-guard.yml                 # Strict PR Gatekeeper with bilingual (EN/FA) error reporting
├── 00-design-system/                    # Shared tokens (colors-dark/light, typography), icons & components
├── 01-external-index/                   # External Index UI (metarang.com)
│   ├── web-desktop/{dark,light}/{rtl,ltr}/<slug>/<lang>/
│   └── web-mobile/{dark,light}/{rtl,ltr}/<slug>/<lang>/
├── 02-internal-index/                   # Internal Index UI (world.metarang.com)
│   ├── web-desktop/{dark,light}/{rtl,ltr}/<slug>/<lang>/
│   └── web-mobile/{dark,light}/{rtl,ltr}/<slug>/<lang>/
├── 03-3d-environments/                  # 3D Worlds, Spatial HUD & VR UI
│   ├── web-desktop/{dark,light}/{rtl,ltr}/<slug>/<lang>/
│   ├── web-mobile/{dark,light}/{rtl,ltr}/<slug>/<lang>/
│   └── vr-headset/{dark,light}/{rtl,ltr}/<slug>/<lang>/
├── 04-community-concepts/               # Experimental & community design concepts
├── 05-contributors/                     # Verified MetaRang Citizen contributor profiles (HM-xxxx.json)
├── CONTRIBUTING.md                      # Bilingual contribution guide
├── LICENSE                              # GNU Affero General Public License v3.0
└── README.md                            # This document
</pre>

---

## ⚙️ Automated DesignOps & Merge Protection

To guarantee zero structural drift and international-grade portfolio quality, two GitHub Actions workflows govern all changes to `main`:

### 1. Issue Auto-Directory & README Scaffolder (`issue-scaffold.yml`)
- **Automated Path Generation:** Triggered when a `ui-task` issue is opened or edited, automatically generating `<category>/<platform>/<theme>/<direction>/<slug>/<lang>/README.md` via a Pull Request to `main`.
- **Mandatory RTL Baseline:** `rtl` is always generated by default; checking `dir:ltr` adds `ltr` alongside it.
- **Language Subdirectories:** Creates dedicated subdirectories (`fa/`, `en/`) for each selected language.
- **Immutable Slug Lock:** Locks the original `Directory Slug` on creation; editing the slug later is blocked with a bilingual error comment.
- **Non-Destructive Auto-Versioning (`v2`, `v3`, `v4`...):** Selecting `enhance-existing` verifies the base folder exists and automatically scaffolds `<slug>-v2`, `<slug>-v3`, etc., preserving all previously merged design files.

### 2. PR Quality & Structure Gatekeeper (`pr-guard.yml`)
Every Pull Request targeting `main` is automatically checked and **blocked from merging** if any rule is violated (with instant **English + Persian** diagnostic comments):
- **No New Directories in PRs:** Design files must reside strictly inside pre-existing directories containing an approved `README.md` on `main`.
- **No Deletion of Existing Designs:** Previously merged design assets cannot be deleted (use versioned enhancement issues instead).
- **Strict Filename Convention:** Lowercase `kebab-case` only (`a-z`, `0-9`, `-`, `_`, `.`) — no spaces, uppercase letters, or Persian characters.
- **Allowed Formats & Size / Git LFS Policy:**
  - Allowed design formats: `.png`, `.jpg`, `.jpeg`, `.gif`, `.svg`, `.pdf`, `.json`, `.glb`, `.fbx`, `.md`.
  - **Max `5 MB`** for 2D/document files without Git LFS.
  - **Mandatory Git LFS** for 3D assets (`.glb`, `.fbx`) and any file exceeding **`10 MB`**.
- **Mandatory Metadata:** Valid JSON syntax for `.json` files, linked Issue reference (`Closes #12` or `Refs #12`), and a public **Figma URL** (`https://www.figma.com/design/...` or `/file/...`).
- **Mandatory Human Review:** Final visual verification and approval by `@iranpsc/ui-ux-manager` (`CODEOWNERS`).

---

## ⚖️ License

This repository is licensed under the **GNU Affero General Public License v3.0 (GNU AGPL-3.0)** — see the [LICENSE](./LICENSE) file for full details.

---
---

<div dir="rtl">

# 🎨 معماری رابط کاربری، تجربه کاربری و سیستم دیزاین متارنگ
### مخزن رسمی، متن‌باز و هوشمند طراحی رابط کاربری و سیستم دیزاین جهان موازی متارنگ

[وب‌سایت اصلی (ایندکس خارجی)](https://metarang.com) • [پورتال و دنیای متارنگ (ایندکس داخلی)](https://world.metarang.com) • [لیست تسک‌ها (Issues)](https://github.com/iranpsc/Metaverse-Rang-UI-UX/issues) • [استاندارد ثبت ایشو](./.github/ISSUE_TEMPLATE/ISSUE-STANDARD.md) • [راهنمای مشارکت](./CONTRIBUTING.md)

---

## 🌌 درباره این ریپازیتوری

**متارنگ (MetaRang)** یک پلتفرم بین‌المللی جهان موازی سه‌بعدی با ریشه ایرانی و معماری غیرمتمرکز است که از بهار ۱۴۰۰ برای پیشتازی در تعاملات دیجیتال آینده‌نگر، اقتصاد مجازی و معماری شهری سه‌بعدی بنیان‌گذاری شده است.

این مخزن، مرجع رسمی و متن‌باز **سیستم دیزاین (Design System)**، **استانداردهای بصری** و **معماری رابط و تجربه کاربری (UI/UX)** در تمامی لایه‌های اکوسیستم متارنگ است. در نسخه جدید این مخزن، تمامی فرآیندهای ایجاد دایرکتوری، مستندسازی دوزبانه، نسخه‌بندی (`v2`, `v3`...) و کنترل کیفیت پیش از مرج به‌صورت کاملاً خودکار توسط **GitHub Actions** و تیم `@iranpsc/ui-ux-manager` مدیریت می‌شوند.

---

## 🔗 مراجع رسمی Figma متارنگ (Official Master Files)

طرح‌های نهایی پس از بررسی و تایید تیم `@iranpsc/ui-ux-manager` در فایل‌های مرکزی Figma متارنگ تجمیع می‌شوند:

| لایه محصول | دامنه / محیط | لینک مرجع رسمی Figma |
| :--- | :--- | :--- |
| **ایندکس خارجی (External Index)** | `metarang.com` | [مشاهده فایل Figma ایندکس خارجی](https://www.figma.com/design/qyvJ4Sjw4h5gRIrE9KotBY/ui-next?node-id=1863-759&p=f&t=ZhzzROkrsum2bANV-0) |
| **ایندکس داخلی (Internal Index)** | `world.metarang.com` | [مشاهده فایل Figma ایندکس داخلی](https://www.figma.com/design/lHgvuzgJhUFACNpMBJK0jI/ui?node-id=34-1989&p=f&t=eTHiDSZ99JfQoJ9T-0) |
| **محیط‌های سه‌بعدی (3D & VR UI)** | `WebGL & VR Headset` | [مشاهده فایل Figma محیط‌های سه‌بعدی](https://www.figma.com/design/Rs8cdjPco3ovjPHFyxZPuC/3d-scien?node-id=2309-2&p=f&t=HWmizeDXyRz7sBW7-0) |

---

## ⚙️ سیستم اتوماسیون DesignOps و جلوگیری از مرج اشتباه

برای حفظ پایداری مخزن، جلوگیری از بی‌نظمی دایرکتوری‌ها و حفظ اعتبار بین‌المللی رزومه مشارکت‌کنندگان، دو اکشن تخصصی تمامی تغییرات روی شاخه `main` را کنترل می‌کنند:

### ۱. ساخت خودکار دایرکتوری و `README.md` دوزبانه (`issue-scaffold.yml`)
- **ساخت خودکار ساختار مسیر:** با ثبت فرم `UI-TASK`، مسیر دقیق `<category>/<platform>/<theme>/<direction>/<slug>/<lang>/README.md` همراه با فایل `README.md` دوزبانه (ابتدا انگلیسی، سپس فارسی) در یک Pull Request به شاخه `main` ایجاد می‌شود.
- **پیش‌فرض اجباری RTL:** جهت `rtl` همیشه به‌صورت پیش‌فرض ساخته می‌شود و در صورت انتخاب `dir:ltr`، نسخه `ltr` نیز ایجاد خواهد شد.
- **زیرپوشه اختصاصی زبان‌ها:** برای هر زبان انتخاب‌شده (`fa` و `en`)، زیرپوشه مجزا ساخته می‌شود.
- **قفل شدن اسلاگ (Slug Lock):** پس از ثبت ایشو، تغییر نام دایرکتوری از طریق ویرایش ایشو مسدود است.
- **نسخه‌بندی خودکار بدون حذف فایل‌های قبلی (`v2`, `v3`, `v4`...):** با انتخاب گزینه `enhance-existing`، نسخه بعدی در کنار دایرکتوری اصلی ایجاد می‌شود و هیچ فایلی از نسخه‌های قبلی حذف نمی‌گردد.

### ۲. گیت‌کیپر کنترل کیفیت Pull Request (`pr-guard.yml`)
در صورت بروز هرگونه مغایرت، مرج PR به‌صورت خودکار **مسدود** شده و گزارش دقیق خطاها به **دو زبان انگلیسی و فارسی** روی PR ثبت می‌شود:
- **ممنوعیت ساخت دایرکتوری جدید در PR:** تمامی فایل‌های طراحی باید صرفاً درون دایرکتوری‌های از پیش ایجادشده و دارای `README.md` روی شاخه `main` قرار بگیرند.
- **ممنوعیت حذف فایل‌های طراحی‌شده قبلی:** حذف طرح‌های مرج‌شده مجاز نیست.
- **نام‌گذاری استاندارد (`kebab-case`):** فقط حروف کوچک انگلیسی، اعداد و خط تیره (بدون فاصله، حروف بزرگ یا کاراکتر فارسی).
- **فرمت‌های مجاز و سقف حجم / Git LFS:**
  - فرمت‌های مجاز: `.png`, `.jpg`, `.jpeg`, `.gif`, `.svg`, `.pdf`, `.json`, `.glb`, `.fbx`, `.md`.
  - سقف حجم **۵ مگابایت** برای فایل‌های دوبعدی و مستندات بدون Git LFS.
  - استفاده از **Git LFS** برای فایل‌های سه‌بعدی (`.glb`, `.fbx`) و تمامی فایل‌های بالای **۱۰ مگابایت** اجباری است.
- **الزامات متادیتا:** صحت سینتکس فایل‌های `.json`، درج شماره ایشو (`Closes #12` یا `Refs #12`) و درج لینک عمومی معتبر **Figma** در متن PR.
- **تایید نهایی انسانی (`CODEOWNERS`):** هر PR پس از پاس شدن چک‌های خودکار، برای مرج نهایی در `main` نیازمند تایید تیم `@iranpsc/ui-ux-manager` است.

---

## ⚖️ مجوز و مالکیت معنوی (License)

این مخزن تحت مجوز متن‌باز **GNU Affero General Public License v3.0 (GNU AGPL-3.0)** منتشر شده است. برای جزئیات بیشتر فایل [LICENSE](./LICENSE) را مطالعه کنید.

</div>
