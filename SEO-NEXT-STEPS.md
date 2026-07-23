# SEO — offene Punkte & nächste Schritte

Stand: 2026-07-23. Ergebnis des claude-seo-Audits, abgearbeitet bis auf die
unten genannten Punkte, die **deinen Input oder deine Aktion** brauchen.

## Braucht deinen Input (Code steht bereit)

- **H1 — Produkt-Screenshots.** Die Feature-Seite hat jetzt eine
  front-matter-getriebene Bild-Schleife (`figures:` in
  `_funktionen/fondspolice-etf-vergleich.md`). Leg echte Screenshots in
  `/assets/screenshots/` und trag sie ein (Format im Kommentar dort). Zwei
  hochwertige Assets: (1) Live-ETF-vs-Fondspolice-Chart, (2) Sample-IDD-PDF
  (geschwärzt). Solange leer, rendert nichts (kein Broken-Image).
- **H4 — Autor-E-E-A-T.** Schema hat jetzt `sameAs` (App Store) + `jobTitle`.
  Für vollständige YMYL-Autorität fehlt: eine kurze „Über den Entwickler"-Sektion
  mit echtem Background/Qualifikation + `sameAs`-Eintrag für dein LinkedIn.
  Gib mir 2–3 Sätze Bio + LinkedIn-URL.
- **M1 — FAQ-Review.** 4 FAQ-Antworten in `_data/faq.yml` wurden für
  AI-Citation erweitert (offline, Tarif-Aktualität, IDD, Kündigung). Da YMYL:
  **bitte fachlich gegenlesen** vor dem nächsten Deploy.

## Deine Aktion (kein Site-Code)

- **L3 — Search-Console & Co. (schnell, hoher Hebel).**
  - GSC: Verify-Token liegt schon in `_config.yml` — nach dem Deploy in der
    [Search Console](https://search.google.com/search-console) „Verify" klicken,
    dann die neue `sitemap.xml` einreichen.
  - [Bing Webmaster Tools](https://www.bing.com/webmasters) anlegen (füttert
    Copilot-Zitate + IndexNow).
  - Moz Free-API-Key (2.500 Rows/Monat) → hebt das nächste Backlink-Audit auf
    Tier 1 (DA/PA, Anchor-Text, Spam-Score).
- **L2 — Brand-Signale (stärkster GEO-Hebel).** Der Audit zeigte ~0 externe
  Erwähnungen. Konkret: 1 YouTube-Demo (90-Sek-Vergleich + PDF-Export),
  1 LinkedIn-Unternehmensseite, 1 echte, sachliche Erwähnung in einer
  Vermittler-/Makler-Community (z.B. AssCompact, r/Finanzen).
- **L1 — Ratgeber-Seiten (mittelfristig).** Die `_ratgeber`-Collection ist
  angelegt (`/ratgeber/:name/`, article-Layout automatisch). 2–3 Standalone-
  Erklärseiten à 400–600 W., jeweils Frage-H1, direkte 40–60-Wort-Definition
  zuerst, dann Vertiefung, CTA zurück zum Rechner:
  - „Vorabpauschale einfach erklärt (2026)"
  - „Halbeinkünfteverfahren bei Fondspolicen — wann greift die 12/62-Regel?"
  - „Teilfreistellung: ETF-Depot vs. Versicherungsmantel"
  Sag Bescheid, dann entwerfe ich die erste als Vorlage.

## Bereits erledigt & deployed

C1 (Hero-LCP), H2 (Tarif-Zahl vereinheitlicht: 57 gesamt / 30+ namentliche
Teilmenge), M2 (Meta-Descriptions), M3 (Sitemap lastmod), M5 (robots/noindex),
M6 (Preis-Typing), H3 (Header-Bug + Mobile-Hamburger), H1-Struktur
(SoftwareApplication-Schema, Orphan-Link, Frage-H2s, FAQ-Block), H4-Schema,
M4 (Bilder → WebP). Details: Commit-History.

## Bewusst zurückgestellt

- **H5 — Security-Header:** GitHub Pages kann keine eigenen Header injizieren.
  Optionen: Cloudflare (free) davor + Transform Rules, oder Hosting-Wechsel.
- **M4 — Font-Trim:** 8 Weights (Newsreader/Inter je 400/500/600/700) sind quer
  über beide Familien im Einsatz — Trimmen braucht einen Per-Selektor-Audit.
  Kandidat: auf je eine Variable-Font-Datei umstellen (8 → 2 Dateien). Separat:
  `font-weight:300` wird 1× genutzt, aber es gibt keine 300-Datei.
