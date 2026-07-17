# Patina Charts Website — Redesign „Refined Institutional" (2026-07-18)

Überarbeitung von `patinacharts.de` (Jekyll-Site in diesem Ordner). Ziel: von
„solides SaaS-Landing" zu „Private-Banking-Broschüre, die zufällig eine App ist".
Gleiche Inhalte & Struktur, eine Klasse höher in Typo, Farbtiefe, Weißraum, Detail.

## Festgelegte Entscheidungen

- **Richtung:** „Institutionell verfeinert" — Evolution, kein Bruch. Navy/Grün/Amber
  bleibt die Grundpalette, wird aber verfeinert.
- **Higgsfield:** genau **ein** Asset — ein subtiler Hero-Atmosphären-Backdrop.
  Keine gefälschte App-UI. Der echte Produkt-Screenshot (`login.jpg`) bleibt der Beweis.
- **Content:** bleibt praktisch unangetastet (Hero → Features → Timeline → Preise →
  DSGVO → FAQ → CTA). Nur minimale Markup-Ergänzungen für Hero-Backdrop/Emblem.

## Design-System (das „hochwertiger")

1. **Typografie (größter Hebel):** Headlines in Serif **Newsreader** (editorial,
   vertrauenswürdig, gut auf Deutsch). Body/UI weiter **Inter**. Feineres Letterspacing,
   größere Headline-Skala, sauberer vertikaler Rhythmus.
2. **Fonts DSGVO-konform selbst gehostet** (kein Google-Fonts-Hotlink → IP-Leak, in DE
   abgemahnt; passt zum eigenen DSGVO-Verkaufsargument). woff2 unter `assets/fonts/`,
   `@font-face`, System-Fallback falls Fetch offline scheitert.
3. **Farbe verfeinert:** Navy tiefer/wärmer, Grün gediegener („Gilt/Money-Green" statt
   Startup-Grün), Amber bleibt seltener Akzent. Mehr Hairlines & Ruhe, weniger Fläche.
4. **Layout & Detail:** mehr Weißraum, editorialere Max-Widths, `01–04`-Ziffern in der
   Timeline, feinere Rules/Shadows, ruhigere Hover-States, kleines **Säulen-Emblem**
   (Inline-SVG, passend zum App-Logo) neben dem Wortmark in Header/Footer.
5. **Hero-Backdrop:** subtiler dunkler Navy-Verlauf mit leisem Grün-Schimmer + Gradient-
   Overlay, damit die Headline gestochen bleibt. (Higgsfield, Recraft V4.1, 16:9, 2K,
   Marken-Palette gelockt.)

## Betroffene Dateien

- `assets/css/style.scss` — Kern der Arbeit (Design-System-Rewrite).
- `_layouts/default.html` — Font-Preloads, Emblem-SVG in Header/Footer, ggf. Hero-Backdrop-Hook.
- `index.md` — nur falls Hero-Backdrop-Element nötig (minimal).
- `assets/fonts/` — neue selbstgehostete woff2 (Newsreader, Inter).
- `assets/hero-bg.*` — neues Higgsfield-Bild.

## Verifikation

- `bundle exec jekyll build` (falls lokal verfügbar) → `_site/` prüfen, kein SCSS-Fehler.
- Sichtprüfung Startseite + eine Legal-Seite, Light **und** Dark, Desktop **und** Mobile-Breite.
- Fallback: SCSS-Kompilat/Struktur manuell prüfen, wenn Jekyll nicht läuft.

## Risiko

Niedrig. Kein Content-Risiko, alles per Git reversibel, eine einzige Bildgenerierung.
Kein Commit ohne ausdrückliche Freigabe (global CLAUDE.md).
