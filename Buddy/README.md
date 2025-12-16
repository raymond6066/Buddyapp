# Buddy Handyman

A Laravel 6 app tailored for handyman teams. Use it to present services, capture leads, and onboard customers with a clean, brand-safe landing page.

## Features
- Service-focused landing page with clear value props and CTAs.
- Static demo at `public/demo.html` for quick GitHub previews without running PHP.
- Environment template (`.env.example`) and production-ready defaults.
- Custom branding throughout (no leftover links or logos from the starter kit).

## Run locally
1. Copy the environment file and generate an app key:
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```
2. Install dependencies and build assets:
   ```bash
   composer install
   npm install
   npm run production
   ```
3. Configure your database in `.env`, then migrate:
   ```bash
   php artisan migrate --seed
   ```
4. Serve the app:
   ```bash
   php artisan serve
   ```
   Visit `http://localhost:8000` to see the branded landing page.

## GitHub demo
- Share the static preview at `public/demo.html` (render it with [htmlpreview.github.io](https://htmlpreview.github.io/) once the repo is on GitHub).
- The static file mirrors the Laravel view so stakeholders can review the UI without installing PHP or Composer.

## Deployment notes
- Set `APP_ENV=production`, `APP_DEBUG=false`, and update `APP_URL` for your domain.
- Point your web server’s document root to `public/` and ensure `storage/` plus `bootstrap/cache/` are writable.
- Configure cache/session drivers (Redis or Memcached) before scaling horizontally.
- Rotate secrets and back up your database regularly.

## Branding reminder
All external starter links have been removed. Update copy, colors, and assets to match your handyman brand identity.
