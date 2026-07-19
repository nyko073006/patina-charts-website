---
title: Datenschutzerklärung — Patina Charts
layout: default
permalink: /privacy/
---

# Datenschutzerklärung

Stand: 8. Mai 2026

Diese Datenschutzerklärung informiert dich nach Artikel 13 DSGVO über die Verarbeitung
personenbezogener Daten bei Nutzung der Patina-Charts-iOS-App.

## 1. Verantwortlicher

**Niklas Julian Humplik**
Hermann-Löns-Straße 10
89537 Giengen an der Brenz
Deutschland

E-Mail: nyko@patinasouthside.de

## 2. Welche Daten werden verarbeitet

### 2.1 Berater-Identität (lokal + optional Cloud)

Wenn du dich in der App registrierst:
- E-Mail-Adresse
- Passwort (verschlüsselt gespeichert via Supabase Auth)
- Optional: Name, Firma, Profilbild, Vermittlerregister-Nr., Anschrift, Telefon
  (für Statusinformation im PDF nach § 15 VersVermV)

**Rechtsgrundlage:** Art. 6 Abs. 1 lit. b DSGVO (Vertragserfüllung).

### 2.2 Mandanten-Daten (lokal)

Wenn du Beratungs-Mandanten in der App anlegst:
- Name (frei wählbar — kann anonymisiert sein)
- Beratungs-Eingaben (Sparrate, Steuerprofil, Bedarf, gewählter Tarif)
- Optional Notizen, Beratungstermine

**Diese Daten liegen ausschließlich lokal auf deinem Gerät** (SwiftData) und werden
**nicht** an einen Server übertragen — außer du aktivierst explizit den
Team-Sync (dann via Supabase, siehe 3.1).

**Rechtsgrundlage:** Art. 6 Abs. 1 lit. b DSGVO (du als Verantwortlicher für
deine Mandanten-Daten — wir als Auftragsverarbeiter wenn Cloud-Sync aktiv ist;
ansonsten reine On-Device-Verarbeitung ohne unsere Beteiligung).

### 2.3 Apple-Kalender-Integration (optional)

Wenn du der App Zugriff auf den Apple-Kalender gewährst:
- Lese-/Schreibzugriff auf Kalender-Events
- Erstellung von Beratungsterminen mit Mandanten-Namen in den Notizen

**Wir senden keine Kalender-Daten an einen Server.** Die Integration läuft
ausschließlich lokal über Apple's EventKit-API.

**Rechtsgrundlage:** Art. 6 Abs. 1 lit. a DSGVO (Einwilligung).

### 2.4 In-App-Käufe via Apple StoreKit

Beim Abschluss eines Abonnements verarbeitet **Apple Inc.** als eigenständig
Verantwortlicher die Zahlungs- und Steuerdaten. Wir erhalten von Apple lediglich
die Information, ob ein Abo aktiv ist (Receipt-Verifikation).

Apple's Datenschutzerklärung: [apple.com/legal/privacy](https://www.apple.com/legal/privacy/)

### 2.5 Tarif-Datenbank

Die App lädt regelmäßig eine öffentliche JSON-Datei mit Versicherungs-Tarifdaten
von GitHub. Dabei werden **keine personenbezogenen Daten übertragen** — nur die
IP-Adresse deines Geräts und der HTTP-User-Agent (technisch unvermeidbar bei
jedem Web-Request).

**Empfänger:** GitHub Inc., 88 Colin P Kelly Jr St, San Francisco, CA 94107, USA.
GitHub bietet ein DSGVO-konformes DPA an.

### 2.6 Kein Tracking, kein Analytics

Die App nutzt **kein Tracking**, kein Analytics-SDK (Firebase, Mixpanel, Amplitude o.Ä.),
keinen Werbe-Identifier (IDFA) und keine Crash-Reporter mit personenbezogenem Bezug.
Eine App-Tracking-Transparency-Abfrage (ATT) entfällt daher.

### 2.7 Zielgruppe / Altersgrenze

Die App richtet sich ausschließlich an gewerbliche Versicherungs- und Finanzberater
(B2B). Sie ist nicht für Personen unter 18 Jahren bestimmt.

## 3. Auftragsverarbeiter

### 3.1 Supabase Inc. (Authentifizierung + optionaler Team-Sync)

- Speichert E-Mail + verschlüsselte Anmeldedaten
- Speichert Mandanten-Daten **nur** wenn Team-Sync aktiviert ist
- Sitz: USA, Server-Region: Frankfurt (EU)
- Auftragsverarbeitungsvertrag (DPA): [supabase.com/legal/dpa](https://supabase.com/legal/dpa)

### 3.2 Apple Inc. (Plattform + Zahlungen)

- iOS/iPadOS-Plattform-Services (CloudKit nicht aktiv)
- App-Store-Subscription-Verwaltung
- Sitz: USA, EU-Tochter Apple Distribution International Ltd. (Irland)
- Datenschutz: [apple.com/legal/privacy](https://www.apple.com/legal/privacy/)

### 3.3 Anthropic PBC (nur Backend, keine Endkunden-Daten)

Für die interne Wartung der Tarif-Datenbank werden öffentliche Versicherungs-
Produktinformationsblätter (PIBs) durch ein Anthropic-LLM ausgelesen. **Es werden
keine Endkunden-, Mandanten- oder Berater-Daten an Anthropic übertragen** —
nur öffentliche PDFs der Versicherungs-Anbieter.

## 4. Speicherdauer

- **Berater-Account-Daten:** bis zur Löschung des Accounts durch dich
- **Mandanten-Daten lokal:** bis du sie selbst löschst (App-Deinstallation =
  Vollständige Löschung)
- **Subscription-Daten:** gemäß Apple's Aufbewahrungsfristen
- **HTTP-Logs (GitHub-Tarif-Fetch):** gemäß GitHub's Vorgaben (typisch wenige Tage)

## 5. Deine Rechte

Nach Art. 15–22 DSGVO hast du das Recht auf:

- **Auskunft** über die zu deiner Person gespeicherten Daten
- **Berichtigung** unrichtiger Daten
- **Löschung** („Recht auf Vergessenwerden")
- **Einschränkung der Verarbeitung**
- **Datenübertragbarkeit** in einem maschinenlesbaren Format
- **Widerspruch** gegen die Verarbeitung
- **Widerruf** erteilter Einwilligungen (z.B. Kalender-Zugriff) — gilt für die
  Zukunft, beeinträchtigt nicht die Rechtmäßigkeit bisheriger Verarbeitung

Zur Ausübung dieser Rechte: schreib an **nyko@patinasouthside.de**.

## 6. Beschwerderecht

Du hast das Recht, dich bei einer Datenschutz-Aufsichtsbehörde zu beschweren.
Zuständig ist:

**Der Landesbeauftragte für den Datenschutz und die Informationsfreiheit
Baden-Württemberg**
Lautenschlagerstraße 20
70173 Stuttgart
[baden-wuerttemberg.datenschutz.de](https://www.baden-wuerttemberg.datenschutz.de)

## 7. Änderungen dieser Datenschutzerklärung

Wir passen diese Erklärung an, wenn sich Funktionen oder rechtliche Anforderungen
ändern. Die jeweils aktuelle Fassung findest du unter dieser URL.

---

[Startseite](../) · [Impressum](../impressum/) · [Support](../support/)
