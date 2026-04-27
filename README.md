# EA 1: Bilderkennung mit ml5

Einsendeaufgabe 1, TH Lübeck, Sommersemester 2026.

Eine einseitige Web-App, die das vortrainierte MobileNet über
[ml5.js](https://docs.ml5js.org/) im Browser ausführt. Sechs Beispielbilder werden
direkt nach dem Laden klassifiziert; zusätzlich kann ein eigenes Bild per
Drag-and-Drop oder Datei-Dialog geladen werden.

## Live-Demo

Öffentlich erreichbar unter:
<https://merganh.github.io/ea1-bilderkennung-ml5/>

## Deployment via GitHub Pages

Im Repo ist ein Workflow unter `.github/workflows/pages.yml` hinterlegt, der die
Seite bei jedem Push auf `main` automatisch nach GitHub Pages deployt. Einmalige
Einrichtung im Repo:

1. **Settings → Pages → Build and deployment → Source** auf
   `GitHub Actions` setzen.
2. Push auf `main` (oder unter **Actions** den Workflow „Deploy to GitHub Pages"
   manuell starten).
3. Nach erfolgreichem Run zeigt der Workflow oben die Live-URL an.

## Lokal ausführen

Wegen CORS-Restriktionen muss die Seite über einen lokalen Server geöffnet werden,
nicht über `file://`:

```bash
python -m http.server 8000
# dann im Browser: http://localhost:8000
```

## Aufbau

- `index.html`: gesamte Anwendung in einer Datei (HTML, CSS und JS inline)
- `images/`: die sechs Beispielbilder

## Abhängigkeiten

Nur über CDN, kein Build-Schritt:

- ml5.js 1.2.2
- Chart.js 4.4.7
