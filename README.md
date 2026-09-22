# ThemeBlog

Lightweight Lifetech theme project built with HTML, Tailwind CSS and JavaScript.

## Summary

ThemeBlog is a reusable theme and admin layout prepared for Lifetech OCMS (PHP). It includes frontend templates, admin views, Lifetech-compatible `ddm/` exports, and sample JSON data in `Export/`.

## Features

- Lifetech-friendly structure and DDM assets
- Ready-to-edit theme components and layouts
- Tailwind-ready CSS and simple JS interactivity

## Requirements

- PHP 8.0+ (recommended)
- MySQL 5.7+
- Composer (for Lifetech OCMS installation)

This project is designed to be used inside a Lifetech OCMS installation. See Lifetech docs: https://www.lifetech.host/hubs/Docs

## Quick Start (Lifetech)

1. Install Lifetech OCMS (recommended via Composer):

```bash
composer create-project lifetechocms/lifetechocms "your-project-name"
```

2. Place this theme into the Lifetech packages/themes folder locally:

```
packages/themes/ThemeBlog/contents/  <-- copy project files into `contents`
```

3. Use the Lifetech admin to install or import the theme package (Lifetech supports ZIP theme installs). Lifetech requires theme filenames to start with `Theme` when exported/imported.

4. Start your local server (XAMPP, WAMP, Docker, or PHP built-in) and visit the Lifetech admin to finish theme installation and preview.

## Development (Lifetech + PHP)

- Recommended dev flow:
  1.  Run Lifetech locally (XAMPP/WAMP/Docker) with PHP 8+ and MySQL.
  2.  Edit theme files locally under `packages/themes/ThemeBlog/contents/` and use Lifetech's auto-sync or the admin theme preview to see changes.
  3.  To create a distributable theme, export the theme from Lifetech admin (ZIP) or package files following Lifetech theme structure.

- Helpful Lifetech docs & examples:
  - Lifetech Docs: https://www.lifetech.host/hubs/Docs

## Project Structure (high level)

- `Assets/` — CSS, JS, admin assets
- `Components/` — Header, Footer and reusable components
- `Layouts/` — Main layout templates
- `Views/` — Page views (blog, post, admin pages)
- `ddm/` — Lifetech DDM components and view assets
- `Export/` — sample JSON exports

## Security & Sensitive Files

I ran a quick scan for common sensitive files and found none committed (no `.env`, private keys, or credentials present). I added standard sensitive patterns to `.gitignore` to prevent accidental commits.

## License

This project is released under the MIT License — see [LICENSE](LICENSE).

## Contributing

Contributions are welcome. If you're targeting Lifetech integration, open a PR and reference Lifetech docs where relevant.
