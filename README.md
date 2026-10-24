# ks-Radlobby

Unveränderte Build-Quellen aus [kartensammlung-overlay-builds](https://github.com/peter-alexander/kartensammlung-overlay-builds).

Der Workflow **Build and publish Radlobby datasets** ist ausschließlich manuell auszulösen und erzeugt alle sechs Ausgaben gemeinsam. Kein Upload auf Lima-City.

GitHub Pages veröffentlicht die Dateien unter `https://peter-alexander.github.io/ks-Radlobby/`:

- `rge_analyse.pmtiles`
- `radparken.pmtiles`
- `sitzmoeglichkeiten.pmtiles`
- `radlkarte.pmtiles`
- `Kuka_Entries.json`
- `RadnetzDashboard.geojson`
- `asset-versions.json` (Schema 1; relative Dateinamen, Unix-Timestamps)

**Einrichtung:** Unter Settings → Pages → Build and deployment als Quelle **GitHub Actions** auswählen. Erst danach den Workflow manuell starten. Die alten Build-Quellen und die bestehende Veröffentlichung bleiben unverändert.

Das Manifest wird mit jeder gemeinsamen erfolgreichen Erstellung neu erzeugt. Vor einem produktiven Einsatz der PMTiles HTTP-Range, 206, CORS und den Cache-Buster im Browser prüfen.
