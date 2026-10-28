# BG Königsbach e.V. – Website-Prototyp

Entwurf für eine neue Startseite der [BG Königsbach e.V.](https://bg-koenigsbach.de/) (Bezirksgruppe im ADRK).
Reines HTML/CSS ohne Build-Schritt, ohne externe Abhängigkeiten, läuft direkt auf GitHub Pages.

```
index.html            Startseite
assets/css/style.css  Styles (Farben als CSS-Variablen oben in der Datei)
assets/img/           Logo + Fotos (von der bestehenden Seite übernommen, verkleinert)
ANALYSE.md            Analyse der alten Seite + Empfehlung Hosting/Pflege
.nojekyll             GitHub Pages ohne Jekyll ausliefern
```

Lokal ansehen: `index.html` im Browser öffnen.

## Veröffentlichen (GitHub Pages)

```bash
cd /Users/mg/Projekte/Private/BG-Koenigsbach
git init -b main
git add .
git commit -m "Prototyp neue Startseite"
git remote add origin git@github-private:GrumpyMikey/bg-koenigsbach.git
git push -u origin main

# Pages aktivieren (oder in GitHub: Settings → Pages → Branch: main / root)
gh api -X POST repos/GrumpyMikey/bg-koenigsbach/pages \
  -f "source[branch]=main" -f "source[path]=/"
```

Danach erreichbar unter: https://grumpymikey.github.io/bg-koenigsbach/

Hinweis: Die Seite hat `noindex` gesetzt, damit der Prototyp nicht in Suchmaschinen landet.
Bei privatem Repo braucht GitHub Pages einen bezahlten Plan – für den Prototyp das Repo also öffentlich lassen.

## Offene Punkte im Entwurf

- Termine sind Platzhalter (auf der alten Seite stehen nur Termine von 2024)
- Impressum / Datenschutz verlinken noch ins Leere
- „Alle Beiträge“ und die News-Links führen noch nirgends hin
- Logo ist nur in niedriger Auflösung vorhanden (aus dem alten Banner ausgeschnitten)
