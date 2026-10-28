# BG Königsbach – Analyse & Empfehlung

Stand: 28.10.2026

## 1. Befund alte Seite (bg-koenigsbach.de)

**Technik**
- Gebaut mit Adobe GoLive (2008 eingestellt), statisches HTML, Hosting bei Strato.
- Kein responsives Layout: auf dem Handy winzig oder seitlich scrollen.
- Navigation besteht nur aus **Bildern** ohne Alt-Text: für Suchmaschinen und Screenreader unsichtbar, nicht anpassbar ohne Grafikprogramm.
- Dateinamen mit Leerzeichen und Umlauten (`Herbstprüfung BG Königsbach.jpg`), Tippfehler `Komtakt.html`.
- Zeichensatz wird nicht sauber ausgeliefert (Umlaute können als „Ã¼“ erscheinen).

**Inhalt & Userflow**
- Die Startseite enthält **keinen einzigen Satz Text**: nur Banner, Menü-Bilder, ein Foto. Ein Besucher erfährt nicht, was der Verein macht, wann trainiert wird oder wie man mitmacht.
- Die wichtigste Info für Interessierte („Dienstags ab 18:30 Uhr, Platzanlage im Steidig“) steckt versteckt unter „Verein → Chronik“.
- Es gibt keinen Weg „Ich bin neu – wie fange ich an?“ und keinen Kontakt-Button.
- Termine veraltet (zuletzt 2024). „Aktuelles“ zeigt nur ein Bild, die eigentlichen Berichte liegen im „Archiv“.
- Kontaktseite = Liste privater E-Mail-Adressen, ohne Erklärung, wen man wofür anschreibt.
- Impressum verweist noch auf TMG / RStV (seit 2024 DDG bzw. MStV).

**Optik**
- Braun-auf-Braun, Text als Grafik, keine Hierarchie, keine Bildsprache.

## 2. Was der Entwurf anders macht

| Ziel | Umsetzung |
|---|---|
| In 5 Sekunden klar, wer wir sind | Hero: „Rottweiler-Sport in Königsbach-Stein – seit 1988“ + Foto vom Platz |
| Wichtigste Fakten sofort | Leiste: Dienstags 18:30 · Ort · ~30 Mitglieder · Prüfungen |
| Klarer Einstieg für Neue | „So einfach geht's los“ in 3 Schritten + Button „Probetraining anfragen“ |
| Zeigen, was der Verein macht | 3 Karten: Ausbildung/IGP, Zucht/Badenschau, Gemeinschaft |
| Lebendigkeit | Termine + die 3 neuesten Berichte direkt auf der Startseite |
| Handy | Vollständig responsiv, Burger-Menü, große Buttons |
| Datenschutz | Keine Google Fonts, keine eingebettete Karte, kein Tracking |

## 3. Hosting & Pflege – Empfehlung

### Strato
- Kein Connector vorhanden. Strato bietet je nach Paket SFTP (bei vielen Paketen auch SSH). Wer die Zugangsdaten hat, kann per SFTP hochladen – oder automatisiert per GitHub Action.
- **Achtung E-Mail:** Es gibt Adressen auf der Domain (z. B. `jeanbecker@bg-koenigsbach.de`). Vor einem Umzug klären, wer welche Postfächer nutzt.

### Variante A – Micha betreut
- Statische Seite (wie dieser Entwurf) auf **GitHub Pages** oder **Cloudflare Pages**: 0 € Hosting, HTTPS inklusive, eigene Domain möglich.
- Kosten bleiben nur für Domain (+ ggf. Mail): typischerweise ein niedriger zweistelliger Betrag pro Jahr bei einem günstigen Registrar.
- Änderungen: Datei bearbeiten → git push → online.

### Variante B – Verein pflegt selbst (ohne Programmierkenntnisse)
Empfehlung: **gleiche statische Seite + [Pages CMS](https://pagescms.org/)** (Open Source, kostenlos).
- Vereinsmitglied loggt sich im Browser ein und bekommt **Formulare**: „Neuer Termin“, „Neuer Bericht“, „Fotos hochladen“.
- Kein Server, keine Updates, keine Sicherheitslücken wie bei WordPress-Plugins.
- Einmalige Einrichtung durch Micha (Inhalte in Markdown/JSON-Dateien aufteilen, z. B. mit Astro oder Eleventy). Danach braucht man nur einen GitHub-Account.
- Alternative mit ähnlichem Prinzip: [Sveltia CMS](https://github.com/sveltia/sveltia-cms).

**Andere Optionen im Vergleich**

| Option | Kosten | Pflege durch Laien | Nachteil |
|---|---|---|---|
| Statisch + Pages CMS | 0 € + Domain | gut (Formulare) | einmalige Einrichtung nötig |
| WordPress bei Billig-Hoster | wenige €/Monat | sehr gut (bekannt) | Updates/Sicherheit, jemand muss sich kümmern |
| Baukasten (Jimdo, Wix …) | Gratis nur mit Werbung/Fremd-Domain | sehr gut | Abo-Kosten für eigene Domain, Lock-in |
| Google Sites | 0 € | sehr gut | wenig Gestaltung, Datenschutz-Fragen |

**Mein Vorschlag:** Variante A jetzt als Basis aufsetzen und so bauen, dass Variante B (Pages CMS) später ohne Umbau dazukommt. Termine und Berichte von Anfang an als eigene Dateien anlegen.

## 4. Vor dem Livegang klären
- Impressum & Datenschutzerklärung aktualisieren (DDG/MStV, Hosting-Anbieter nennen).
- Nutzung des **ADRK-Logos** mit dem ADRK abstimmen (es ist das Logo des Dachverbands).
- Fotos mit erkennbaren Personen: Einverständnis der Abgebildeten sicherstellen.
- Bessere Logo-Datei (Vektor/SVG) beim ADRK oder Verein anfragen.
- Welche E-Mail-Adresse soll öffentlich als Kontakt stehen? Ideal: `kontakt@bg-koenigsbach.de` als Weiterleitung.
