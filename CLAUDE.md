# CLAUDE.md — Arbeitsanweisung für dieses Repo

Diese Datei wird von Claude Code automatisch gelesen. Sie beschreibt, was dieses
Projekt ist und welche inhaltlichen Regeln für jeden Text gelten, der hier
geschrieben oder geändert wird.

## Was das hier ist

Die Website zum Produkt **KLARSPORT**, einem hypotonischen Elektrolytgetränk.
Sie ist im Rahmen einer Marketing-Weiterbildung („KI im Marketing", Woche 6,
DataSmart Point Academy) als Abschlussprojekt entstanden.

**Wichtig: Produkt und Firma sind erfunden.** Es gibt kein reales Produkt, keine
reale Firma und keine realen Kundinnen oder Kunden. Das Kundenzitat auf der Seite
ist ein Übungs-Platzhalter und als solcher gekennzeichnet. Die Produktbilder sind
mit KI erstellt (ChatGPT) und tragen den Hinweis „Mit KI erstellt (ChatGPT)".
Diese Kennzeichnungen dürfen nicht entfernt werden.

## Technik

Eine statische Website, ohne Build-Schritt, ohne Framework, ohne Abhängigkeiten.

- `index.html` — die komplette Seite: HTML, CSS und JavaScript in einer Datei
- `images/` — Produkt- und Logobilder, jeweils als `.webp` mit `.jpg`/`.png` als Fallback
- `fonts/` — Archivo und IBM Plex Sans, lokal eingebunden (SIL Open Font License)
- `docs/` — der gesamte Kampagnen-Hintergrund (siehe unten)

Zum Ansehen genügt es, `index.html` im Browser zu öffnen. Die Datei enthält drei
Ansichten — Startseite (`#start`), Bestellseite (`#bestellen`) und Verfügbarkeit
(`#verfuegbarkeit`). Umgeschaltet wird über `location.hash` und ein kleines Skript
am Ende der Datei; es gibt keinen Router und keinen Server. Eine weitere Ansicht
kommt dazu, indem man ein `<div id="page-…" class="page-view" hidden>` anlegt und
es im `pages`-Objekt des Skripts einträgt — die Umschaltlogik läuft über dieses
Objekt und braucht sonst keine Änderung.

Beim Arbeiten an der Seite bitte beibehalten: die CSS-Variablen in `:root`
(inklusive der Dark-Mode-Blöcke), die lokalen Schriften statt eines CDN, und die
`<picture>`-Elemente mit WebP-Quelle und klassischem Fallback.

## Markenstimme — gilt für jeden Text auf der Seite

- **Ansprache:** Du. Wir treten als „wir" auf, nie mit Personennamen.
- **Ton:** eher ernst, eher locker, deutlich sachlich, durchgehend respektvoll.
- **Satzbau:** kurze Hauptsätze, höchstens ein Nebensatz. Keine Ausrufezeichen.
- **Diese Wörter benutzen wir:** Zutatenliste · überprüfbar · pro Flasche ·
  Elektrolyte · nach dem Training · kalorienarm
- **Diese Wörter kommen nie vor:** entdecke · innovativ · revolutionär ·
  Genussmoment · Detox · reichhaltig

So klingt es richtig: „Du kommst gerade vom Training. KLARSPORT hat vier Zutaten
und 15 Kalorien pro Flasche – steht so auf dem Etikett."

So nicht: „Entdecke jetzt unser innovatives Elektrolyt-Erlebnis für den ultimativen
Genussmoment nach dem Sport!"

## Kernbotschaft

> „Mit KLARSPORT musst du nach dem Training nicht mehr auf Wasser ausweichen."

Jeder Text auf der Seite soll diese Botschaft tragen. Die Probe: Wenn die Persona
„na und?" sagen kann, steht da noch eine Eigenschaft statt eines Nutzens.

## Zahlen — nur diese, und keine neuen

Keine Zahl ohne Grundlage. Erlaubt sind ausschließlich die Angaben vom
(fiktiven) Etikett:

| Angabe | Wert |
| --- | --- |
| Zutaten | Wasser, Mineralstoffe (Natriumchlorid, Magnesiumcitrat, Kaliumcitrat), natürliches Zitrone-Limette-Aroma, Süßungsmittel Steviolglycoside |
| Energie je 100 ml | 13 kJ / 3 kcal (rund 15 kcal pro 500-ml-Flasche) |
| Fett | 0 g |
| Kohlenhydrate | 0,7 g, davon Zucker 0 g |
| Eiweiß | 0 g |
| Salz | 0,08 g |
| Magnesium | 15 mg |
| Kalium | 50 mg |
| Preis | 2,49 € pro 500-ml-Glasflasche |

Keine Wirkungsversprechen, keine Gesundheitsaussagen, keine Vergleiche mit
fremden Marken. Der Kaliumvergleich im Abschnitt „Im Vergleich" ist die einzige
Gegenüberstellung und nennt bewusst keine Marke.

## Die Persona

Jonas, 32, Bürojob, trainiert dienstags, donnerstags und samstags nach der Arbeit.
Sein Satz: „Ich hab gerade trainiert, und jetzt soll ich literweise Zucker
reinkippen?" Seine bisherige Alternative ist nicht ein Konkurrenzprodukt, sondern
einfach Wasser. Genau deshalb argumentiert die Seite gegen Wasser und nicht gegen
Powerade oder isostar.

## Offener Punkt: der Firmenname

In den Kampagnenunterlagen (`docs/`) heißt die Firma durchgehend **KlarPuls GmbH**.
Auf der Website und im Logo steht dagegen **Klarfrisch GmbH** (`images/logo-klarfrisch.*`).
Das ist ein echter Widerspruch und noch nicht entschieden. Bitte nicht
eigenmächtig vereinheitlichen, sondern nachfragen, welcher Name gilt — am Logo
hängt eine Bilddatei, die dann neu erstellt werden müsste.

## Was auf der Seite noch fehlt

Impressum, Datenschutz, AGB und Karriere sind im Footer als Platzhalter angelegt
und noch nicht verlinkt. Der Onlineshop ist nicht angebunden; die Bestellseite
sagt das ausdrücklich.

Die Kontaktangaben im Footer stehen: Klarfrisch GmbH, Klarstraße 18, 18188
Klarstadt, info@klarfrisch.de. Sie sind wie das ganze Produkt erfunden.

## Hintergrund in `docs/`

Der vollständige Kampagnenhintergrund liegt als Markdown in `docs/`: Produkt und
Zielgruppe, Persona, Markenstimme, Kernbotschaft und die geprüften Texte, die
Bildprompts samt KI-Kennzeichnung sowie der fertige Kampagnenentwurf mit
Redaktionsplan. Wer hier Texte ändert, sollte vorher `docs/04-kampagnenentwurf.md`
gelesen haben.
