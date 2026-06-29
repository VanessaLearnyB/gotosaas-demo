# Go to SAAS demo

Site de démonstration : page d'accueil + changelog. Déployé automatiquement sur
Cloudflare Workers (assets statiques) à chaque push sur `main` via GitHub Actions.

## Structure

- `public/` — fichiers du site (`index.html`, `changelog.html`, `styles.css`)
- `wrangler.toml` — configuration Cloudflare Workers (assets statiques)
- `.github/workflows/deploy.yml` — déploiement automatique via Wrangler

## Déploiement automatique

À chaque push sur `main`, GitHub Actions exécute `wrangler deploy`.

### Secrets GitHub requis (Settings → Secrets and variables → Actions)

| Secret | Valeur |
| --- | --- |
| `CLOUDFLARE_API_TOKEN` | Ton token API Cloudflare (permission *Workers Scripts: Edit*) |
| `CLOUDFLARE_ACCOUNT_ID` | `325c743999080b60a61e5832310755fa` |
