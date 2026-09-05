# Innsbruck Event-Radar — Daten

Täglich gesammelte Veranstaltungstermine im Raum Innsbruck
(Innsbruck plus rund 30 km). Dieses Repository enthält **nur die
Ausgabe**; der Sammler liegt woanders.

Stand: 2026-09-05 · **789 Termine**, davon 54 neu seit dem letzten Lauf.

| Datei | Inhalt |
|---|---|
| `events.json` | Einzeltermine plus Serientermine der nächsten 21 Tage |
| `serien.json` | wiederkehrende Formate, auf 90 Tage ausgerechnet |
| `neu.json` | Zugänge seit dem letzten Lauf |
| `events.ics` | Kalenderdatei zum Abonnieren |
| `status.json` | welche Quelle wie viel geliefert hat |
| `gesundheit.json` | was sich beim Zustand der Quellen geändert hat |

Abrufadresse mit CORS (`Access-Control-Allow-Origin: *`):

```
https://raw.githubusercontent.com/brunokuehn/innsbruck-event-radar/main/events.json
```

## Datenvertrag

Ein JSON-Array. Jeder Eintrag hat neun feste Felder — `titel`,
`datum`, `bis`, `zeit`, `ort`, `url`, `quelle`,
`kategorie`, `anmeldeschluss` — dazu `serie` und `neu`
als Wahrheitswerte. Datumsangaben sind `JJJJ-MM-TT` oder leer,
Uhrzeiten `HH:MM` oder leer. `kategorie` ist eine von
`sport`, `musik`, `kultur`, `kurse`, `markt`, `mix`.
