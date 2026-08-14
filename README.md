# KI Telefon-Agent — Website (Übergabe)

Komplette, fertige Website für **AI Voice Impact UG** (ki-telefon-agent.com).
Reines HTML/CSS/JavaScript — **kein Build, kein Framework, keine Datenbank**. Die Dateien können
1:1 auf jeden Webspace hochgeladen werden.

**Live-Vorschau:** https://itisrob.github.io/ki-telefon-agent-v2/

---

## Was ist enthalten

**25 Seiten**

| Bereich | Seiten |
| --- | --- |
| Hauptseiten | `index.html` (Start), `so-funktionierts.html`, `branchen.html`, `preise.html` |
| Lösungen | `use-cases.html`, `onoffice.html`, `custom.html` |
| Kontakt & Unternehmen | `termin.html`, `ueber-uns.html`, `interview.html` |
| Blog | `blog.html` + 10 Artikelseiten |
| Rechtliches | `impressum.html`, `datenschutz.html`, `agb.html`, `avv.html` |

**Ordnerstruktur**

```
├── *.html                  alle Seiten
├── assets/
│   ├── css/styles.css      komplettes Design (Farben ganz oben in :root)
│   ├── js/app.js           Menü, Animationen, Slider, Cookie-Banner, Formular
│   ├── img/                alle Bilder (inkl. branchen/ mit 92 Branchenfotos)
│   └── docs/               AVV-PDF
├── robots.txt              Suchmaschinen-Freigabe
├── sitemap.xml             Seitenverzeichnis für Google
└── .nojekyll               nur für GitHub Pages nötig
```

---

## Website veröffentlichen

**Variante A – klassischer Webspace (FTP/Hosting)**
Den kompletten Inhalt dieses Ordners in das Hauptverzeichnis (meist `/httpdocs`, `/public_html`
oder `/www`) hochladen. Fertig — `index.html` ist automatisch die Startseite.

**Variante B – GitHub Pages / Netlify / Vercel**
Ordner als Repository hochladen bzw. hineinziehen. Es ist keine Konfiguration nötig.

### Nach dem Umzug auf die echte Domain
In allen HTML-Dateien steht im Kopfbereich die Vorschau-Adresse. Vor dem Livegang einmal
suchen & ersetzen:

```
https://itisrob.github.io/ki-telefon-agent-v2/   →   https://ki-telefon-agent.com/
```

Betrifft: `canonical`, `og:url`, `og:image`, `twitter:image`, die JSON-LD-Daten sowie
`robots.txt` und `sitemap.xml`. Danach die `sitemap.xml` in der Google Search Console einreichen.

---

## Inhalte selbst pflegen

| Was ändern? | Wo? |
| --- | --- |
| Texte, Überschriften | direkt in der jeweiligen `.html`-Datei |
| Farben (Gold/Schwarz) | `assets/css/styles.css`, ganz oben im Block `:root` |
| Telefonnummern | Suchen & Ersetzen über alle Dateien (`040 – 7430 2560`, Demo: `040 – 743 069 53`) |
| Kundenstimmen (Slider) | `index.html`, Abschnitt „KUNDENSTIMMEN (Slider)" — eine `<div class="testi-card">` pro Stimme |
| Preise | `preise.html` (Umschalter Standard ↔ onOffice) und `onoffice.html` |
| Blogartikel | jeweilige Artikeldatei + Kachel in `blog.html` |

---

## Vor dem Livegang zu erledigen

1. **Kontaktformular anbinden** — „Testanruf anfordern" (auf `index.html` und `termin.html`)
   zeigt aktuell nur die Danke-Meldung an. In `assets/js/app.js` in der Funktion `submitForm()`
   die Zieladresse (z. B. LeadConnector-, Make- oder Zapier-Webhook) eintragen.
2. **Terminkalender** — eingebunden ist das bestehende LeadConnector-Widget
   (`termin.html`). Sobald der neue Kalender-Link vorliegt, dort austauschen.
3. **Tracking** — Google Analytics, Meta-Pixel und Microsoft Clarity sind vorbereitet, aber
   bewusst noch nicht aktiv. IDs in `assets/js/app.js` in der Funktion `loadTracking()`
   eintragen; sie werden dann erst **nach** Zustimmung im Cookie-Banner geladen (DSGVO).
4. **Domain umstellen** (siehe oben) und Rechtstexte final anwaltlich prüfen lassen.

---

## Technische Eckdaten

- **Responsiv** für Handy, Tablet und Desktop
- **SEO vollständig**: Seitentitel, Beschreibungen, Open-Graph-/Social-Vorschaubilder,
  Canonical-Links, strukturierte Daten (JSON-LD), `robots.txt`, `sitemap.xml`
- **Cookie-Banner** mit Zustimmung vor jedem Tracking
- **Barrierearm & schnell**: keine externen Abhängigkeiten außer der Schriftart (Google Fonts)
  und den eingebetteten Videos
- **Design**: Schwarz-Gold-Weiß, Akzentfarbe `#e6c76a`

---

*Erstellt von GrowPotential · Stand: Juli 2026*
