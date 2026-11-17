# Schlafplatz-Finder

Offline-fähige Webapp für die Unterkunftswahl im Rennen.

## Dateien

| Datei | Zweck |
| --- | --- |
| `index.html` | Die App |
| `sw.js` | Speichert die App für den Offline-Start |
| `manifest.webmanifest`, `icon-*.png` | Name und Icon auf dem Home-Bildschirm |

## Auf GitHub Pages stellen

1. Neues Repository anlegen (z. B. `schlafplatz-finder`) und alle Dateien in den Hauptordner hochladen.
2. Unter *Settings → Pages* als Quelle den Branch `main` und den Ordner `/ (root)` wählen.
3. Nach ca. 1 Minute läuft die App unter `https://<benutzername>.github.io/schlafplatz-finder/`.

Geht auch auf jedem anderen Webspace mit HTTPS. Service Worker funktionieren nur über HTTPS (oder `localhost`).

## Aufs iPhone

1. Die Adresse in **Safari** öffnen, einmal neu laden.
2. Im Setup muss bei «Offline» **bereit** stehen.
3. *Teilen → Zum Home-Bildschirm*. Ab dann immer über das Icon starten.
4. Test: Flugmodus an, App über das Icon öffnen.

Wichtig: Die Daten (Route, Unterkünfte, Status) liegen in der Home-Bildschirm-App, **nicht** in Safari. Route und Unterkünfte deshalb erst importieren, nachdem die App auf dem Home-Bildschirm liegt. Vor dem Rennen im Setup eine Sicherung exportieren.

## Updates

Nach einer Änderung an `index.html` in `sw.js` die `VERSION` erhöhen (z. B. `spf-v2`) und beides hochladen. Die App meldet beim nächsten Start mit Netz «Neue Version verfügbar», im Setup auf «Neue Version laden» tippen. Die gespeicherten Daten bleiben erhalten.
