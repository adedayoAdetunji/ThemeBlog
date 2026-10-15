# ThemeBlog 📰✨

[![LifeTech OCMS](https://img.shields.io/badge/LifeTech%20OCMS-v2.7.4%2B-blue.svg)](https://github.com/adedayoAdetunji/ThemeBlog)
[![Dependency](https://img.shields.io/badge/Depends%20On-MdBlog%20v1.0.0-green.svg)](https://github.com/adedayoAdetunji/ThemeBlog)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Version](https://img.shields.io/badge/Version-1.0.0-indigo.svg)](package.json)
[![Tech Stack](https://img.shields.io/badge/Stack-HTML5%20%7C%20TailwindCSS%20%7C%20JS%20%7C%20PHP-orange.svg)](#technology-stack)

**ThemeBlog** is a modern, responsive, and editorial-grade publication theme developed for **LifeTech OCMS (v2.7.4+)**. Built to deliver an immersive reading experience, ThemeBlog pairs warm paper aesthetics and rich typography with an interactive front-end and a full-featured admin management dashboard designed to seamlessly complement the **MdBlog** module.

---

## 📑 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
  - [Reader & Public Experience](#reader--public-experience)
  - [Editorial & Admin Management](#editorial--admin-management)
- [Design System & Styling](#-design-system--styling)
- [Directory Structure](#-directory-structure)
- [Dependencies & Prerequisites](#-dependencies--prerequisites)
- [Installation & Setup](#-installation--setup)
- [Pages & Routing](#-pages--routing)
- [Package Metadata & DDM Export](#-package-metadata--ddm-export)
- [Git & GitHub Setup](#-git--github-setup)
- [Contributing & License](#-contributing--license)

---

## 🌟 Overview

ThemeBlog transforms your LifeTech OCMS installation into a high-performance publishing platform. Whether creating an independent newsroom, tech publication, personal blog, or corporate editorial portal, ThemeBlog delivers:

- **Warm Editorial Aesthetic**: Crafted with warm hues, distinct category accents, and high-legibility serif and sans-serif typefaces.
- **Dynamic Client Interactivity**: Instant search, category filtering, sort selectors, live view counter, post reactions, interactive comments, and share actions.
- **Integrated Administration**: Dedicated admin layout and views for complete control over articles, categories, tags, user comments, moderation reports, and theme settings.
- **Full LifeTech OCMS Standard Compliance**: Includes complete Data Definition Models (`ddm/`) and export manifest files (`Export/`) for one-click installation and routing.

---

## 🚀 Key Features

### Reader & Public Experience

- **Curated Blog Homepage (`Blog.html`)**:
  - Hero header with typed/dynamic headlines and publication subtitle.
  - Live search input filtering posts by title, excerpt, and content.
  - Category dropdown filter loaded dynamically from active categories.
  - Multi-criteria sorting:
    - *Latest*
    - *Oldest*
    - *Most Viewed*
    - *Most Liked*
    - *Most Discussed*
    - *Title (A–Z / Z–A)*
  - Responsive article grid with reading time calculations, author avatar, category badges, published date, view counts, and engagement stats.
  - Interactive pagination controls.

- **Article Reader View (`Post.html`)**:
  - Immersive typography optimized for long-form reading.
  - Dynamic cover image rendering with fallback avatar generation.
  - Dynamic author card with profile information and social links.
  - **Live Reactions & Engagement**:
    - Post like counter with instantaneous API synchronization.
    - Automatic view count incrementation on post view.
  - **Social Sharing**:
    - Quick-share buttons for Twitter/X, Facebook, LinkedIn, and Clipboard copy.
  - **Nested Comment System**:
    - Form to submit comments with instant feedback.
    - Comment like counter.
    - Nested comment support and user avatars.
  - **Community Moderation**:
    - Built-in modal dialog allowing readers to report content with specified reasons and notes.
  - **Related Posts & Category Navigation**: Keeps readers engaged with related reading recommendations.

### Editorial & Admin Management

ThemeBlog provides an administrative suite powered by the `Admin-layout.html` framework:

- **Admin Dashboard (`Admin-dashboard.html`)**:
  - Key publication metrics (total published posts, view counts, comments, pending moderation tickets).
  - Quick action links and real-time activity feed.
- **Post Management (`Manage-post.html`)**:
  - Create, edit, and preview blog posts.
  - Rich text formatting support.
  - Category and tag assignments, cover image uploads, and slug generation.
  - Instant publish / draft status toggling.
- **Category Management (`Manage-category.html`)**:
  - Create, update, toggle status (active/inactive), and delete blog categories.
- **Tag Management (`Manage-tag.html`)**:
  - Organize posts with tags for granular taxonomy and searchability.
- **Comment Moderation (`Manage-comment.html`)**:
  - Review submitted comments, approve, reject, flag as spam, or delete.
- **Report & Flag Resolution (`Manage-report.html`)**:
  - Review reader-submitted flags on posts or comments, track review status, and resolve issues directly.
- **Theme Settings (`Manage-settings.html`)**:
  - Centralized customization panel for layout settings, display preferences, and theme options.

---

## 🎨 Design System & Styling

ThemeBlog is built upon custom design tokens implemented through Tailwind CSS and vanilla CSS:

### Color Palette

| Token | Hex Value | Usage |
| :--- | :--- | :--- |
| `background` / `paper` | `#faf6f0` / `#fbfaf6` | Warm off-white page background |
| `surface` | `#ffffff` | Card and component surfaces |
| `foreground` / `ink` | `#2b2724` / `#171623` | High-contrast body typography |
| `muted` / `ink-soft` | `#7a7268` / `#56526b` | Captions, dates, and secondary text |
| `border` / `line` | `#e8e0d5` / `#e3ddc9` | Subtle structural dividers |
| `primary` | `#08cf72` | Main brand and action green |
| `accent` / `coral` | `#e0674f` / `#e4572e` | Brand accents, buttons, and callouts |
| `violet` | `#7c5cfc` | Secondary category accents and badges |
| `amber` | `#f2a93b` | Warning states and category indicators |
| `teal` | `#1fa7a0` | Accent badges and category indicators |
| `pink` | `#e85d9c` | Editorial highlight accents |

### Typography Pairing

- **Headlines & Masthead**: `"Fraunces"`, Georgia, serif (optical sizing enabled for display elegance).
- **Body Text**: `"Source Serif 4"` / `"Inter"`, system-ui, sans-serif (optimized legibility).
- **Meta & Code**: `"IBM Plex Mono"`, ui-monospace, monospace.

---

## 📁 Directory Structure

```text
ThemeBlog/
├── Assets/
│   ├── admin/                    # Admin-specific assets
│   │   ├── css/index.php
│   │   ├── js/index.php
│   │   └── index.php
│   ├── css/
│   │   ├── Style.css             # Main stylesheet & custom utility classes
│   │   └── index.php
│   ├── js/
│   │   ├── Script.js             # Global utilities (SweetAlert2, API fetcher, loader, timeAgo)
│   │   ├── Tailwind-config.js    # Tailwind CSS extended theme configuration
│   │   └── index.php
│   └── index.php
├── Components/                   # Modular reusable UI components
│   ├── admin/
│   │   ├── Admin-header.html     # Admin dashboard header
│   │   ├── Admin-sidebar.html    # Dynamic sidebar menu with API menu loader
│   │   ├── Admin-top-header.html # Admin top bar with user profile/notifications
│   │   └── index.php
│   ├── ContentLoadBody.html      # Dynamic body loader component
│   ├── Footer.html               # Public footer with navigation & copyright
│   ├── Header.html               # Editorial masthead with gradient title
│   ├── Top-header.html           # Public top notice bar
│   └── index.php
├── Export/                       # LifeTech OCMS package export manifests
│   ├── content.json              # Component, layout, view, and asset mappings
│   ├── menu.json                 # Menu structure and hierarchy definitions
│   ├── page.json                 # Route paths, page names, and HTTP handlers
│   ├── pageContent.json          # Page-to-component linkage data
│   ├── table.json                # Associated database schema descriptors
│   └── index.php
├── Layouts/                      # Structural template layouts
│   ├── Admin-layout.html         # Base master layout for admin interfaces
│   └── index.php
├── Views/                        # Core views and rendered pages
│   ├── admin/
│   │   ├── Admin-dashboard.html  # Admin analytics & overview
│   │   ├── Manage-category.html  # Category CRUD view
│   │   ├── Manage-comment.html   # Comment moderation view
│   │   ├── Manage-post.html      # Post authoring and management
│   │   ├── Manage-report.html    # User reports resolution view
│   │   ├── Manage-settings.html  # Theme configuration view
│   │   ├── Manage-tag.html       # Tag management view
│   │   └── index.php
│   ├── Blog.html                 # Main blog catalog / archive view
│   ├── Post.html                 # Single post reading view
│   └── index.php
├── ddm/                          # LifeTech Data Definition & Model files (.lifetech)
│   ├── Admin-dashboard.View.lifetech
│   ├── Admin-header.Component.lifetech
│   ├── Admin-layout.Layout.lifetech
│   ├── Admin-sidebar.Component.lifetech
│   ├── Admin-top-header.Component.lifetech
│   ├── Blog.View.lifetech
│   ├── ContentLoadBody.Component.lifetech
│   ├── Footer.Component.lifetech
│   ├── Header.Component.lifetech
│   ├── Manage-category.View.lifetech
│   ├── Manage-comment.View.lifetech
│   ├── Manage-post.View.lifetech
│   ├── Manage-report.View.lifetech
│   ├── Manage-settings.View.lifetech
│   ├── Manage-tag.View.lifetech
│   ├── Post.View.lifetech
│   ├── Script.Asset.lifetech
│   ├── Style.Asset.lifetech
│   ├── Tailwind-config.Asset.lifetech
│   ├── Top-header.Component.lifetech
│   └── index.php
├── .gitignore                    # Git ignore file for development cleanliness
├── LICENSE                       # MIT License
├── README.md                     # Project documentation
├── index.php                     # Redirect handler for security
└── package.json                  # Theme manifest for LifeTech OCMS
```

---

## ⚙️ Dependencies & Prerequisites

1. **LifeTech OCMS Engine**: Version `2.7.4` or higher.
2. **Backend Module**: **`MdBlog`** (v1.0.0+) providing the required API endpoints:
   - `/blogs/posts` (GET, POST, PUT, DELETE, slug lookup, reactions, view counter)
   - `/blogs/categories` (GET, POST, PUT, DELETE, status toggle)
   - `/blogs/tags` (GET, POST, PUT, DELETE, status toggle)
   - `/blogs/comments` (GET, POST, status updates, like toggle)
   - `/blogs/reports` (POST, status updates, incident review)
   - `/blogs/settings` (GET, PUT, theme settings persistence)
   - `/menus/is-navigation` (Dynamic menu loading)
3. **External Libraries (Loaded via CDN)**:
   - [Tailwind CSS CDN](https://cdn.tailwindcss.com)
   - [SweetAlert2](https://cdn.jsdelivr.net/npm/sweetalert2@11)
   - [FontAwesome 6](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css)
   - [RemixIcon](https://cdn.jsdelivr.net/npm/remixicon@3.5.0/fonts/remixicon.css)

---

## 🛠️ Installation & Setup

### Method 1: LifeTech OCMS Admin Package Installer

1. Compress the `ThemeBlog` directory as a ZIP file (or use `ThemeBlog.zip`).
2. Log into your **LifeTech OCMS** administrative console.
3. Navigate to **System > Package Manager > Themes**.
4. Click **Install / Upload Theme** and upload `ThemeBlog.zip`.
5. Once installation finishes, activate **ThemeBlog** as your active blog theme.
6. Ensure that **`MdBlog`** is enabled in the Modules section.

### Method 2: Manual Directory Deployment

1. Copy the `ThemeBlog/` folder into your LifeTech OCMS themes root:
   ```text
   /themes/ThemeBlog/
   ```
2. In the LifeTech OCMS backend dashboard, run **Synchronize Packages** or import the configuration files located in `Export/`.
3. Set `ThemeBlog` as the active theme for blog routes.

---

## 🧭 Pages & Routing

| Page Name | Route Path | Description | Access |
| :--- | :--- | :--- | :--- |
| `Blog.html` | `/ThemeBlog/Blog` | Main blog listing, search, and category filters | Public |
| `Post.html` | `/ThemeBlog/blog/post/{slug}` | Single article reader view with comments & reactions | Public |
| `Admin-dashboard.html` | `/ThemeBlog/Admin-dashboard` | Administrative analytics and activity overview | Admin |
| `Manage-post.html` | `/ThemeBlog/Manage-post` | Create, edit, publish, and delete articles | Admin |
| `Manage-category.html` | `/ThemeBlog/Manage-category` | Category management and taxonomy configuration | Admin |
| `Manage-tag.html` | `/ThemeBlog/Manage-tag` | Tag management and keyword assignments | Admin |
| `Manage-comment.html` | `/ThemeBlog/Manage-comment` | Comment moderation and review | Admin |
| `Manage-report.html` | `/ThemeBlog/Manage-report` | Reported posts/comments resolution queue | Admin |
| `Manage-settings.html` | `/ThemeBlog/Manage-settings` | Theme parameters and blog customization settings | Admin |

---

## 📦 Package Metadata & DDM Export

The theme manifest is declared in `package.json`:

```json
{
    "ltId": "178791436476666",
    "packageName": "ThemeBlog",
    "packageType": "theme",
    "version": "1.0.0",
    "dependsOn": [
        {
            "packageName": "MdBlog",
            "version": "1.0.0"
        }
    ],
    "isPublished": null,
    "readme": "README.md",
    "languageUsed": "html, tailwind/css, javascript",
    "description": "Theme Blog",
    "ltVersion": "2.7.4"
}
```

- **Export Manifests (`Export/`)**:
  - `content.json`: Declares checksums, component names, sort orders, and resource types.
  - `menu.json`: Configures the hierarchical navigation tree for the theme.
  - `page.json`: Registers page routes, slugs, and HTTP handlers.
  - `pageContent.json`: Links pages to their respective layout and content components.
  - `table.json`: Records metadata regarding database integration.

---

## 🐙 Git & GitHub Setup

To initialize this project as a standalone repository and push to GitHub:

```bash
# Navigate to the ThemeBlog project directory
cd /path/to/ThemeBlog

# Initialize git repository (if not already initialized)
git init

# Check the branch name (standard is main)
git branch -M main

# Add all files
git add .

# Create the initial commit
git commit -m "feat: initial commit for ThemeBlog v1.0.0"

# Add the remote repository
git remote add origin https://github.com/adedayoAdetunji/ThemeBlog.git

# Push to GitHub
git push -u origin main
```

---

## 📄 Contributing & License

Contributions, bug reports, and feature requests are welcome!

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for complete details.

Copyright (c) 2024–2026, **LifetechOCMS** & **Adedayo Adetunji**.
