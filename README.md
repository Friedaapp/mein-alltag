# Mein Alltag – neues Design mit Notizen

Enthält:
- Ruhiges Design in Salbeigrün, Creme und Weiß
- Navigation seitlich am PC und unten am Handy
- Startseite mit Wetter, offenen Aufgaben, heutigen Terminen, Einkaufsliste, kommenden Terminen und Teamlinks
- Wochenkalender, Wetter über Open-Meteo
- Supabase-Synchronisierung für Aufgaben, Termine, Einkauf und Notizen
- Fußballlinks für BVB, Hannover 96 und TSV Havelse
- Volleyballlinks für TV Lohnde Frösche Mixed, Männer und Frauen

## Einmalige Einrichtung der Notizen-Tabelle
Bevor du die neue Version benutzt, öffne Supabase → SQL Editor → New query und führe diesen SQL-Code aus:

```sql
create table if not exists public.notes (
  id uuid primary key default gen_random_uuid(),
  user_id uuid not null references auth.users(id) on delete cascade,
  title text not null,
  content text not null default '',
  created_at timestamptz not null default now()
);

alter table public.notes enable row level security;
grant select, insert, delete on public.notes to authenticated;

drop policy if exists "Users can view own notes" on public.notes;
create policy "Users can view own notes"
on public.notes for select to authenticated
using (auth.uid() = user_id);

drop policy if exists "Users can insert own notes" on public.notes;
create policy "Users can insert own notes"
on public.notes for insert to authenticated
with check (auth.uid() = user_id);

drop policy if exists "Users can delete own notes" on public.notes;
create policy "Users can delete own notes"
on public.notes for delete to authenticated
using (auth.uid() = user_id);
```

Klicke anschließend auf **Run**.

## Vor dem Upload
1. Öffne `index.html` im Windows-Editor.
2. Suche nach `HIER_PROJECT_URL_EINTRAGEN` und `HIER_PUBLISHABLE_KEY_EINTRAGEN`.
3. Ersetze beide Platzhalter mit deinen bisherigen Supabase-Werten und speichere.
4. Lade `index.html`, `manifest.json`, `sw.js` und `README.md` in dein GitHub-Repository hoch.

Niemals einen `service_role`- oder Secret-Key in die App eintragen.

Sportlinks öffnen die Originalseiten; Sportdaten werden nicht in der App selbst gespeichert.
