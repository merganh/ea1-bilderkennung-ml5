# EA 1: Bilderkennung mit ml5

Einsendeaufgabe 1, TH Lübeck, Sommersemester 2026.

Eine einseitige Web-App, die das vortrainierte MobileNet über
[ml5.js](https://docs.ml5js.org/) im Browser ausführt. Sechs Beispielbilder werden
direkt nach dem Laden klassifiziert; zusätzlich kann ein eigenes Bild per
Drag-and-Drop oder Datei-Dialog geladen werden.

## Lokal ausführen

Wegen CORS-Restriktionen muss die Seite über einen lokalen Server geöffnet werden,
nicht über `file://`:

```bash
python -m http.server 47823
# dann im Browser: http://localhost:47823
```

Hinweis für Windows: Port 8000 (und teilweise auch 8080) ist häufig durch
Hyper-V / WSL reserviert und führt zu `WinError 10013`. Ein hoher Port wie
47823 ist in der Regel frei. Welche Ports reserviert sind, lässt sich mit
`netsh interface ipv4 show excludedportrange protocol=tcp` prüfen.

## Aufbau

- `index.html`: gesamte Anwendung in einer Datei (HTML, CSS und JS inline)
- `images/`: die sechs Beispielbilder

## Abhängigkeiten

Nur über CDN, kein Build-Schritt:

- ml5.js 1.2.2
- Chart.js 4.4.7
