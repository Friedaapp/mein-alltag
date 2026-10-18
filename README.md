# Mein Alltag – Wochenkalender

Diese Version behält die Supabase-Synchronisierung für Aufgaben, Termine und Einkaufsliste bei und ergänzt eine Wochenübersicht.

## Vor dem Hochladen
Öffne `index.html` im Editor und prüfe die Zeilen `SUPABASE_URL` und `SUPABASE_PUBLIC_KEY`. Falls dort Platzhalter stehen, trage deine Project URL und den öffentlichen Publishable Key (oder den alten öffentlichen `anon`-Key) ein. Verwende niemals `service_role` oder `secret`.

## Hochladen
Lade alle vier Dateien (`index.html`, `manifest.json`, `sw.js`, `README.md`) über GitHub → Add file → Upload files in das Repository `mein-alltag` hoch und bestätige mit Commit changes.

## Funktionen
Aufgaben, Termine und Einkaufsliste werden mit Supabase synchronisiert. Die Kalenderansicht zeigt Montag bis Sonntag, mit Navigation zur vorigen und nächsten Woche sowie Schnellwahl eines Datums beim Anlegen eines Termins.
