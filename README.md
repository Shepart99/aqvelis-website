# aqvelis-website

Offizielle Website für AQVELIS – Smart Water Management für Pools und Aquarien.

Dieses Repository enthält die statische, öffentliche Website von AQVELIS. Sie
wird über GitHub Pages veröffentlicht und ist später unter der Domain
[aqvelis.at](https://aqvelis.at) erreichbar.

## Zweck

Die Website informiert über AQVELIS, eine App für intelligentes
Wassermanagement von Pools und Aquarien (Wasserwerte verwalten, Messungen
dokumentieren, Wasserpflege unterstützen). AQVELIS befindet sich derzeit in
Vorbereitung und ist noch nicht öffentlich verfügbar; die Website weist
darauf an mehreren Stellen deutlich hin.

## Technik

- Reines HTML5 / CSS3, keine Build-Pipeline, kein Framework
- Keine externen Abhängigkeiten (keine CDNs, keine Webfonts, kein Tracking)
- Alle Grafiken (Logo, Icons, Wellen) als eigenes, handgeschriebenes SVG
- Ausschließlich relative Pfade, damit die Seite sowohl unter dem
  GitHub-Pages-Projektpfad (`/aqvelis-website/`) als auch später unter der
  Custom Domain `aqvelis.at` funktioniert

## Seitenstruktur

| Datei | Inhalt |
| --- | --- |
| `index.html` | Startseite: Hero, Funktionen, Pool & Aquarium, Vertrauen, Status |
| `datenschutz.html` | Datenschutzerklärung |
| `impressum.html` | Impressum |
| `support.html` | Support-Informationen |
| `account-loeschen.html` | Informationen zur Löschung von AQVELIS-Konten |

## Lokale Vorschau

Da es sich um eine rein statische Website handelt, genügt ein einfacher
lokaler Webserver, zum Beispiel:

```bash
python -m http.server 8000
```

Anschließend die Seite unter `http://localhost:8000` im Browser öffnen.
Alternativ kann `index.html` auch direkt im Browser geöffnet werden.

## GitHub-Pages-Deployment

1. Im Repository unter **Settings → Pages** als Quelle den Branch `main` und
   das Root-Verzeichnis (`/`) auswählen.
2. Die Website ist danach unter
   `https://<benutzername>.github.io/aqvelis-website/` erreichbar.
3. Für die Custom Domain `aqvelis.at` wird zusätzlich eine `CNAME`-Datei
   sowie die entsprechende DNS-Konfiguration benötigt (noch nicht Teil
   dieses Repositories).

## Aktueller Stand

Die rechtlichen Seiten (`datenschutz.html`, `impressum.html`,
`account-loeschen.html`) enthalten die Betreiberangaben (Name, Anschrift,
Kontakt) sowie die Beschreibung der eingesetzten Dienste (u. a. Supabase,
Mailtrap). AQVELIS selbst befindet sich weiterhin in Vorbereitung und ist
noch nicht öffentlich verfügbar; die Website weist unter anderem auf
`index.html` darauf hin.
