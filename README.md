# Patina Charts — Website

Statische Marketing-, Support- und Datenschutz-Seiten für die Patina-Charts-iOS-App.
Deployed via GitHub Pages mit Jekyll-Theme.

## Setup (einmalig)

1. Auf github.com → New Repository → Name: `patina-charts-website` → Public →
   ohne README/gitignore
2. Lokal:
   ```bash
   cd /Users/nyko/Desktop/ETFvsPolice/website
   git init
   git branch -M main
   git add .
   git commit -m "initial: marketing + support + privacy"
   git remote add origin https://github.com/nyko073006/patina-charts-website.git
   git push -u origin main
   ```
3. GitHub-Repo öffnen → **Settings → Pages**:
   - Source: **Deploy from a branch**
   - Branch: **main** / Folder: **/ (root)**
   - Save
4. Nach 1-3 Minuten ist die Seite live unter
   `https://nyko073006.github.io/patina-charts-website/`

## URLs für App Store Connect

| Apple-Feld | URL |
|---|---|
| Marketing-URL | `https://nyko073006.github.io/patina-charts-website/` |
| Support-URL | `https://nyko073006.github.io/patina-charts-website/support/` |
| Datenschutz-URL | `https://nyko073006.github.io/patina-charts-website/privacy/` |

## Files

- `index.md` — Marketing-Landing
- `support.md` — Support-FAQ + Kontakt + Beschwerdewege
- `privacy.md` — DSGVO-konforme Datenschutzerklärung
- `_config.yml` — Jekyll-Konfiguration (Theme, Sprache)
