# KI Telefon-Agent — Website Redesign v2

Komplettes Redesign von [ki-telefon-agent.com](https://ki-telefon-agent.com) im Stil von famulor.de:
Schwarz-**Gold**-Weiß-Sektionsrhythmus (Akzent `#e6c76a`), Glas-Karten, Scroll-Animationen, **branchenübergreifende** Positionierung — echte Fotos aus 23 Branchen statt KI-Renders.

**Echte Mehrseiten-Navigation** (kein One-Pager): jeder Menüpunkt führt auf eine eigene Unterseite, inkl. dedizierter Seiten `so-funktionierts.html` und `branchen.html`. Branchen-Bildbibliothek unter `assets/img/branchen/` (`<slug>-1..4.jpg`, Slugs ohne Umlaute, z. B. `rechtsanwalte`, `immobilienburos`, `wirtschaftsprufer`).

## Struktur

- Statisches HTML/CSS/JS — kein Build-Schritt, direkt GitHub-Pages-fähig
- `assets/css/styles.css` — komplettes Design-System (Design-Tokens oben in `:root`)
- `assets/js/app.js` — Nav, Scroll-Reveal, Headline-Rotation, Tabs, FAQ, Marquees, Cookie-Banner, Formular
- `assets/img/` — alle Bilder lokal gesichert (von der alten WordPress-Seite übernommen)
- `assets/docs/` — AVV-PDF

## Seiten

Start (`index.html`), Preise, Use-Cases, onOffice, Custom-CRM, Termin, Über uns, Interview,
Blog + 10 Artikel, Impressum, Datenschutz, AGB, AVV.

## Offene Punkte (vor Go-Live)

1. **Testanruf-Formular** (`index.html`, `termin.html`): kein Backend angebunden — Webhook/Endpoint in `assets/js/app.js` → `submitForm()` eintragen.
2. **Buchungs-Widget**: aktuell LeadConnector (`Fcnc6EwPDHMhTtiSCgDk`) — ersetzen, sobald Franks neuer Kalender-Link vorliegt.
3. **Tracking-IDs** (GA4, Meta-Pixel, MS Clarity) in `app.js` → `loadTracking()` nachtragen (lädt erst nach Cookie-Consent).
4. **Testimonial-Video André Schneider** wird noch von der alten Domain geladen (99 MB, zu groß fürs Repo) — vor Abschaltung der alten Seite umziehen.
