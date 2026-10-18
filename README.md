# Mein Alltag – Supabase-Version mit Synchronisierung

## Vor dem Hochladen
1. Öffne `index.html` mit einem Texteditor.
2. Prüfe, ob `SUPABASE_URL` deine Supabase Project URL enthält.
3. Prüfe, ob `SUPABASE_PUBLIC_KEY` deinen öffentlichen Publishable Key (oder den alten öffentlichen `anon`-Key) enthält.
4. Niemals einen `service_role`- oder `secret`-Key einsetzen.

## Hochladen
Lade `index.html`, `manifest.json`, `sw.js` und `README.md` in dein GitHub-Repository `mein-alltag` hoch und bestätige die Änderungen. Warte danach kurz und lade die App auf PC und Android neu.

## Synchronisierte Daten
- Aufgaben: Supabase-Tabelle `tasks`
- Termine: Supabase-Tabelle `events`
- Einkaufsliste: Supabase-Tabelle `shopping_items`

Alle drei Tabellen verwenden Row Level Security und ordnen Einträge dem angemeldeten Konto zu. Wetterdaten kommen von Open-Meteo. Sportlinks führen zu offiziellen Seiten.
