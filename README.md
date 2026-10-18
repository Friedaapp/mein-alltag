# Mein Alltag – Prototyp 0.1

Ein einfacher, mobilfreundlicher Prototyp für Android und iPhone.

## Was funktioniert bereits?
- Startseite mit Tagesübersicht
- Aufgaben anlegen, als privat/beruflich markieren, Fälligkeitsdatum setzen, abhaken und löschen
- Termine lokal speichern
- Einkaufsliste verwalten und Artikel abhaken
- Wetter und 5-Tage-Vorhersage über Open-Meteo laden (Standortfreigabe oder Ortssuche)
- Links zu den Vereinsseiten von Borussia Dortmund, Hannover 96, TSV Havelse und TV Lohnde

## Noch nicht enthalten
- Synchronisierung zwischen mehreren Geräten
- Anmeldung/Cloud-Datenbank
- Anbindung an Google-/Apple-/Outlook-Kalender
- Automatische Sport-Spielpläne, Live-Ergebnisse und Tabellen
- Push-Benachrichtigungen

## So startest du

### Einfachster Weg zum Ausprobieren
1. Entpacke die ZIP-Datei.
2. Öffne `index.html` im Browser.
3. Aufgaben, Termine und Einkaufsliste kannst du sofort verwenden.
4. Wetter benötigt eine Internetverbindung. Standortfreigabe funktioniert je nach Browser nur in einem sicheren Kontext (HTTPS oder localhost); alternativ kannst du einen Ort eingeben.

### Auf dem iPhone/Android installieren
Eine installierbare Web-App benötigt eine HTTPS-Adresse. Lade die Dateien auf einen statischen Hostingdienst hoch (zum Beispiel GitHub Pages oder Netlify). Öffne anschließend die HTTPS-Adresse auf dem Smartphone:
- iPhone: Teilen → „Zum Home-Bildschirm“
- Android/Chrome: Menü → „App installieren“ oder „Zum Startbildschirm hinzufügen“

Für die Wetter-API wird Open-Meteo verwendet. Die Aufgaben, Termine und Einkaufslisten liegen in dieser Version nur im lokalen Speicher des jeweiligen Browsers. Browserdaten nicht löschen, wenn du die Einträge behalten möchtest.

## Dateien
- `index.html` – App, Oberfläche und Funktionen
- `manifest.json` – Installationsinformationen
- `sw.js` – einfacher Service Worker für Offline-Grundfunktionen
