# Buddy Handyman

A ready-to-deploy Laravel 6 handyman service hub. Use it to showcase services, collect requests, and share a quick demo straight from GitHub.

## Project structure
- `Buddy/` – Laravel application source (routes, views, assets).
- `public/demo.html` – Static, Blade-free version of the landing page for GitHub previews.
- `docs/` – Additional assets, such as screenshots or diagrams.

## Quickstart
1. Clone the repository and move into the app directory:
   ```bash
   git clone <your-fork-url>
   cd Buddy
   ```
2. Copy the environment template and set your secrets:
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```
3. Install backend dependencies and compile the frontend:
   ```bash
   composer install
   npm install
   npm run production
   ```
4. Configure your database in `.env`, then run migrations and (optionally) seed data:
   ```bash
   php artisan migrate --seed
   ```
5. Serve locally:
   ```bash
   php artisan serve
   ```
   Visit `http://localhost:8000` to see the Buddy Handyman landing page.

## Deployment checklist
- Set production environment variables (`APP_ENV=production`, `APP_DEBUG=false`, `APP_URL=https://your-domain`).
- Configure cache and session stores (Redis/Memcached) for scale, or fall back to file drivers for single-host setups.
- Point your web server to the `Buddy/public` directory and ensure `storage` and `bootstrap/cache` are writable.
- Schedule backups for the database and `.env` secrets.
