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
| `nutzungsbedingungen.html` | Nutzungsbedingungen |
| `account-loeschen.html` | Informationen zur Löschung von AQVELIS-Konten |

### Zweisprachigkeit (DE/EN)

Die deutschen Seiten liegen im Root, die englischen unter `en/`. Jede Seite
enthält einen sichtbaren „DE | EN“-Link zur exakten Gegenseite (reines HTML,
kein JavaScript, keine automatische Weiterleitung) sowie `canonical`- und
`hreflang`-Angaben (`de`, `en`, `x-default` → deutsche Seite).

| Deutsch | Englisch |
| --- | --- |
| `index.html` | `en/index.html` |
| `support.html` | `en/support.html` |
| `datenschutz.html` | `en/privacy.html` |
| `impressum.html` | `en/legal-notice.html` |
| `nutzungsbedingungen.html` | `en/terms.html` |
| `account-loeschen.html` | `en/account-deletion.html` |

Die englischen Rechtstexte sind Übersetzungen der deutschen Fassungen;
inhaltliche Änderungen werden immer zuerst in der deutschen Seite
vorgenommen und dann in die englische Seite übernommen.

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
`nutzungsbedingungen.html`, `account-loeschen.html` sowie ihre englischen
Gegenstücke unter `en/`) enthalten die Betreiberangaben (Name, Anschrift,
Kontakt) sowie die Beschreibung der eingesetzten Dienste (u. a. Supabase,
Mailtrap). AQVELIS befindet sich derzeit in der Testphase; eine öffentliche
Veröffentlichung ist in Vorbereitung. Die Website weist unter anderem auf
`index.html` darauf hin.
