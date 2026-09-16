# mycoachpath.com

Statische Version von mycoachpath.com, gezogen von one.com (Stand: 15.09.2026) und aufbereitet für Netlify.

## Struktur

```
site/                 Publish-Verzeichnis (Netlify: publish = "site")
  index.html          /
  cc/                 /cc                 Coaching Calculator
  possibility-sheet/  /possibility-sheet
  thank-you/          /thank-you
  imprint/            /imprint
  privacy-policy/     /privacy-policy
  disclaimer/         /disclaimer
  404.html
  robots.txt
  sitemap.xml
  assets/onecdn.io/   Bilder, Fonts, JS-Bundles, CSS (lokal, ex one.com CDN)
netlify.toml          Build- und Header-Konfiguration
```

## Deploy

Netlify baut nichts, es wird nur `site/` ausgeliefert. Repo verbinden, Branch `main`,
publish directory `site`. Alternativ: Ordner `site/` auf https://app.netlify.com/drop ziehen.

## Lokal ansehen

```
cd site && python3 -m http.server 8787
```

## Hinweise

- CSS und JS liegen inline im HTML (so hat one.com exportiert). Änderungen gehen
  direkt im HTML, einen visuellen Editor gibt es nicht mehr.
- Alle Assets sind lokal, die Seite hängt nicht mehr an one.com.
- Externe Abhängigkeiten, die bewusst extern bleiben: Google Tag Manager,
  Facebook Pixel, Crispforms (Bewerbungsformular), Loom (Video auf /possibility-sheet).
- Der one.com Analytics-Call auf `/_api/stats-service` läuft ins Leere. Ohne Wirkung.
