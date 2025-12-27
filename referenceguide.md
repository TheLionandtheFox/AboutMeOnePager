# HTML Erklärt !! Noch in Arbeit !!

## Wichtige Merkmale

- **Struktur**:
Ist ein Baumstruktur mit einem `<html>`-Tag als **Wurzelelement (Root-Element)**. Innerhalb von `<html>` befinden sich immer genau zwei Bereiche:  
`<head>` (Metadaten) und `<body>` (sichtbare Inhalte).
Elemente werden durch Tags () definiert, die oft Paare bilden (Start- und End-Tag wie `<p>...</p>`). 
Wichtige semantische Strukturelemente sind Überschriften (`<h1>–<h6>`), Absätze (`<p>`), Listen (`<ul>, <ol>`), Abschnitte (`<section>`) und Navigation (`<nav>`), um Inhalte logisch zu gliedern.

- **Sprachfestlegung**:  
Es ist Best Practice, das Attribut `lang` zu verwenden  
(`<html lang="de">`), um Suchmaschinen und Screenreadern  
die Sprache der Seite mitzuteilen.

- **Pflicht-Elemente**:  
Jedes gültige HTML5-Dokument **muss** die Elemente `html`, `head` und `body` enthalten. Wenn man es vergisst, ergänzt es der Browser automatisch (si werden nicht automatisch in die Datei eingefügt, sondern nur im Browser intern ergänzt).
`<!DOCTYPE html>`-Deklaration, die ganz am Anfang der Datei stehen muss, um dem Browser mitzuteilen, dass es sich um HTML5 handelt, und um eine korrekte Darstellung sicherzustellen. 
Jedes HTML5-Dokument **sollte** die Basisstruktur enthalten:
`<!DOCTYPE html>`, `<html>`, `<head>` (mit `<meta charset="UTF-8">` und `<title>`), `<body>`, da diese das Dokument definieren, Metadaten (wie den Titel für Browser-Tabs/Suchmaschinen) bereitstellen und den sichtbaren Inhalt umschließen, wobei auch semantische Tags wie `<header>`, `<nav>`, `<main>`, `<footer>` und Überschriften (`<h1>` bis `<h6>`) für Struktur und SEO entscheidend sind.

## Übersicht Aufbau

    <!DOCTYPE html>
    <html lang="de">
    <head>
        <title>Titel der Seite</title>
    </head>
    <body>
        <h1>Hallo Welt!</h1>
    </body>
    </html>

1. Grundgerüst (Struktur-Tags)

Diese Tags bilden das Skelett jeder Webseite:

## <!DOCTYPE html>

    <!DOCTYPE html>

Die `<!DOCTYPE html>`- Keine Tag im eigentlichen Sinne, sondern die Deklaration für HTML5. Deklaration teilt dem Browser mit, dass es sich um ein **HTML5-Dokument** handelt.  
Sie ist **kein HTML-Tag**, sondern eine notwendige Anweisung für den korrekten Darstellungsmodus.

## **`<html>`** Tag

Das Wurzelelement, umschließt das gesamte Dokument. Es signalisiert dem Browser, dass der gesamte darin enthaltene Code als HTML interpretiert werden soll. Es hat einen offenen und geschlossenen Tag.
Es umschließt alle anderen Elemente einer Webseite (außer der `<!DOCTYPE html>`-Deklaration).  

    <html> </html>

- **`<head>`**: Enthält Metainformationen (Titel, Scripte, CSS-Links), die nicht direkt auf der Seite erscheinen.

    <html> 
        <head> </head>
    </html>

- **`<body>`**: Umschließt den gesamten sichtbaren Inhalt der Webseite.

## 2. Text-Strukturierung & Semantik

Diese Tags geben dem Inhalt Bedeutung und helfen Suchmaschinen (SEO):

- `<h1>` bis `<h6>`: Überschriften (h1 ist die wichtigste).
- `<p>`: Definiert einen Textabsatz (Paragraph).
- `<strong>`: Hebt Text fett hervor (starke semantische Betonung).
- `<em>`: Hebt Text kursiv hervor (Akzentuierung).
- `<br>`: Erzwingt einen Zeilenumbruch (selbstschließendes Tag).
- `<hr>`: Zeichnet eine horizontale Linie zur thematischen Trennung.

## 3. Listen & Verweise

- `<a>`: Erstellt einen Hyperlink (Attribut `href` erforderlich).
- `<ul>`: Ungeordnete Liste.
- `<ol>`: Geordnete Liste.
- `<li>`: Einzelnes Listenelement.

## 4. Medien & Container

- `<img>`: Bindet ein Bild ein (`src` und `alt` sind Pflicht).
- `<div>`: Allgemeiner Block-Container für Layout und CSS.
- `<span>`: Inline-Container für Textabschnitte.

## 5. Semantische HTML5-Tags (Layout)

Diese Tags verbessern Struktur, Barrierefreiheit und SEO:

- `<header>`: Kopfbereich einer Seite oder eines Abschnitts.
- `<nav>`: Navigationsbereich.
- `<main>`: Hauptinhalt der Seite.
- `<section>`: Thematischer Abschnitt.
- `<article>`: Eigenständiger Inhalt (z. B. Blogpost).
- `<footer>`: Fußbereich der Seite.
