# KLARSPORT — Produktwebsite

Statische Website zu KLARSPORT, einem hypotonischen Elektrolytgetränk
(Zitrone-Limette, 500-ml-Glasflasche, vier Zutaten, rund 15 Kalorien pro Flasche).

Produkt und Firma sind erfunden. Die Seite ist als Abschlussprojekt einer
Marketing-Weiterbildung entstanden („KI im Marketing", Woche 6). Die
Produktbilder sind mit KI erstellt und tragen den Hinweis „Mit KI erstellt
(ChatGPT)"; das Kundenzitat auf der Seite ist ein gekennzeichneter
Übungs-Platzhalter.

## Ansehen

Kein Build, keine Abhängigkeiten. `index.html` im Browser öffnen genügt.

Wer einen lokalen Server bevorzugt:

```
python3 -m http.server 8000
```

Dann http://localhost:8000 aufrufen.

## Aufbau

```
index.html      komplette Seite: HTML, CSS und JS in einer Datei
images/         Produktfotos und Logo, je als .webp mit .jpg/.png als Fallback
fonts/          Archivo und IBM Plex Sans, lokal eingebunden (SIL OFL, Lizenzen liegen bei)
docs/           Kampagnenhintergrund: Produkt, Zielgruppe, Persona, Markenstimme, Texte
CLAUDE.md       Arbeitsanweisung für Claude Code, inklusive aller Textregeln
```

Die Seite besteht aus drei Ansichten in einer Datei: der Startseite, einer
Bestellseite (`#bestellen`) und einer Seite zur Verfügbarkeit
(`#verfuegbarkeit`). Umgeschaltet wird über `location.hash`, ein kleines Skript
am Ende der Datei blendet die jeweils anderen Bereiche aus.

Abschnitte der Startseite: Hero mit Kernbotschaft, Zutatenstreifen, Produkt mit
Nährwerttabelle vom Etikett, Kaliumvergleich mit Mineralwasser, Kundenstimme und
ehrliche Grenze, Bezugswege, Footer.

Die Seite unterstützt hellen und dunklen Modus über
`prefers-color-scheme` und lässt sich zusätzlich per `data-theme` auf dem
`<html>`-Element festlegen.

## Inhaltliche Regeln

Alle Texte folgen einer festgelegten Markenstimme, und jede Zahl auf der Seite
stammt vom (fiktiven) Produktetikett. Beides steht in `CLAUDE.md`, ausführlich
belegt in `docs/`. Wer Texte ändert, sollte dort zuerst nachsehen.

## Offene Punkte

- **Firmenname:** In den Unterlagen heißt die Firma KlarPuls GmbH, auf der
  Website und im Logo steht Klarfrisch GmbH. Noch nicht entschieden.
- Impressum, Datenschutz, AGB und Karriere sind Platzhalter im Footer.
- Der Onlineshop ist nicht angebunden; die Bestellseite weist darauf hin.
