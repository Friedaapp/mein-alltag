# Mein Alltag – Supabase-Version

## Vor dem Hochladen
1. Öffne `index.html` in einem Texteditor.
2. Suche nach `SUPABASE_URL` und `SUPABASE_PUBLIC_KEY`.
3. Ersetze `HIER_PROJECT_URL_EINTRAGEN` durch deine Supabase Project URL.
4. Ersetze `HIER_PUBLISHABLE_KEY_EINTRAGEN` durch den öffentlichen Publishable Key (oder den alten `anon`-Key).
5. Niemals einen `service_role`- oder `secret`-Key einsetzen.

## Hochladen
Lade `index.html`, `manifest.json`, `sw.js` und `README.md` in dein GitHub-Repository `mein-alltag` hoch und bestätige die Änderungen. Danach einige Minuten warten und die App in Edge/Android neu laden.

## Daten
Aufgaben werden mit Supabase synchronisiert. Termine und Einkaufsliste werden in dieser ersten Version lokal auf dem jeweiligen Gerät gespeichert. Wetterdaten kommen von Open-Meteo. Sportlinks führen zu offiziellen Seiten.
