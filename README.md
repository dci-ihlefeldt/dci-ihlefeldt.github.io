# Landingpage Diane C. Ihlefeldt

Statische Website (HTML/CSS, ohne Build-Schritt) für GitHub Pages.

## Aufbau

```
diane-website/
├── index.html              # Die komplette Seite
├── .nojekyll               # Verhindert Jekyll-Verarbeitung durch GitHub
├── assets/
│   └── diane-portrait.jpg  # Profilfoto (98 KB)
└── README.md               # Diese Datei
```

Gesamtgröße: ~130 KB (vorher: 1,5 MB).

## Lokal ansehen

`index.html` einfach im Browser per Doppelklick öffnen.

## Inhalt anpassen

Alles befindet sich in **`index.html`**. Wichtige Stellen mit Kommentaren markiert:

- **`<title>`**, **`<meta name="description">`** — Titel und Beschreibung für Google.
- **`og:url`**, **`<link rel="canonical">`**, **JSON-LD `url`** — Nach dem GitHub-Pages-Setup an die echte URL anpassen (z. B. `https://dci-ihlefeldt.github.io/`).
- **Hero-Headline** (`<h1>`) — Slogan.
- **Trust-Bar** — Liste der Referenzkunden.
- **Sektion `#cases`** — Drei Projektbeispiele (anonymisiert). Frei austauschbar.
- **Sektion `#referenzen`** — Zitate aus Arbeitszeugnissen.
- **Sektion `#kontakt`** — E-Mail, Telefon, LinkedIn.
- **Sektion `#datenschutz`** — Impressum + DSGVO-Texte.

## Bild austauschen

Neues Foto als JPG (max. 1 MB, idealerweise ca. 1200 × 1600 px, Hochformat) unter `assets/diane-portrait.jpg` ablegen — fertig.

---

## Auf GitHub Pages veröffentlichen

### Schritt 1 — GitHub-Account erstellen (falls noch nicht vorhanden)

1. Auf [github.com](https://github.com/signup) gehen.
2. Mit E-Mail-Adresse registrieren — **Tipp:** als Username etwas wählen, das später in der URL gut aussieht, z. B. `dci-ihlefeldt` oder `diane-ihlefeldt`. Die Adresse Deiner Seite wird dann **`https://USERNAME.github.io`**.
3. Kostenlosen Plan auswählen, E-Mail bestätigen.

### Schritt 2 — Repository anlegen

1. Eingeloggt auf GitHub: oben rechts auf **„+"** → **„New repository"** klicken.
2. **Repository name** muss exakt sein: `USERNAME.github.io` (z. B. `dci-ihlefeldt.github.io`).
3. **Public** auswählen (kostenfrei nur für öffentliche Repositories).
4. **„Add a README file"** weglassen (haben wir schon).
5. Auf **„Create repository"** klicken.

### Schritt 3 — Dateien hochladen (ohne Kommandozeile)

1. Im neuen Repository auf **„uploading an existing file"** klicken (Link mitten auf der Seite).
2. Alle Dateien aus dem Ordner `diane-website` per Drag-and-Drop ins Browserfenster ziehen:
   - `index.html`
   - `.nojekyll` *(Datei beginnt mit Punkt — falls macOS Finder sie nicht zeigt: Cmd-Shift-Punkt drücken)*
   - `README.md`
   - kompletten **`assets/`**-Ordner *(GitHub legt den Ordner automatisch an)*
3. Unten: **„Commit changes"** klicken.

### Schritt 4 — Pages aktivieren

1. Im Repository: **„Settings"** (oben rechts).
2. Linke Seite: **„Pages"**.
3. Bei **Source** auswählen: **„Deploy from a branch"**.
4. **Branch**: `main` und Folder `/ (root)` → **Save**.
5. Nach 1–2 Minuten erscheint oben grün: **„Your site is live at https://USERNAME.github.io"**.

### Schritt 5 — URL in der Seite eintragen (optional, aber empfohlen)

Nach dem ersten erfolgreichen Deploy einmal `index.html` öffnen und alle drei Stellen mit `https://example.github.io/` durch Deine echte URL ersetzen:

- Im `<head>`: `<link rel="canonical" href="...">`
- Im `<head>`: `<meta property="og:url" content="...">`
- Im JSON-LD-Block: `"url": "..."`, `"image": "..."`

Das verbessert SEO und korrekte Vorschauen beim Teilen auf LinkedIn/WhatsApp.

### Schritt 6 — Aktualisieren

Datei direkt im Browser bearbeiten:
1. Datei im Repository öffnen → Stift-Symbol oben rechts.
2. Änderungen vornehmen → unten **„Commit changes"**.
3. Nach 30–60 Sekunden ist die Live-Seite aktualisiert.

---

## Eigene Domain (z. B. `diane-ihlefeldt.de`) später anbinden

1. Im Repository eine Datei `CNAME` (ohne Endung) anlegen mit dem Inhalt: `diane-ihlefeldt.de`
2. Beim Domain-Provider zwei DNS-Einträge setzen:
   - `A`-Record auf `185.199.108.153` (sowie `.109`, `.110`, `.111`)
   - oder `CNAME`-Record auf `USERNAME.github.io.`
3. In GitHub Settings → Pages die Domain eintragen, **„Enforce HTTPS"** aktivieren.

---

## Was diese Version ggü. der vorherigen leistet

- **Performance:** 1,5 MB → ~130 KB (Bild ausgelagert + komprimiert).
- **SEO:** Meta-Description, Open-Graph, Twitter-Card, JSON-LD (Schema.org Person), Theme-Color, Favicon.
- **Navigation:** Saubere `#anchor`-Links statt JavaScript, Skip-Link für Screenreader, mobiles Burger-Menü.
- **Accessibility:** Fokus-Stile, `prefers-reduced-motion`, semantische `<main>`-Struktur, korrekte `<blockquote>`/`<cite>`.
- **Inhalt:** Neue Sektion mit drei anonymisierten Projektbeispielen (Ausgangslage / Lösung / Ergebnis).
- **Mobile:** Kontakt-Buttons mit Icons, Hero-Buttons untereinander, kollabierende Trust-Bar.
- **Print:** Eigene Print-Styles (Navigation und Kontaktblock werden ausgeblendet).
