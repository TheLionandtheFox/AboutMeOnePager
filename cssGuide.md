# CSS Erklärt

> **Status:** Noch in Arbeit

## Was ist CSS?

**CSS (Cascading Style Sheets)** ist eine Stylesheet-Sprache, die das Aussehen und Layout von HTML-Elementen steuert. Während HTML die Struktur einer Webseite definiert, bestimmt CSS deren visuelle Gestaltung.

### Wichtige Merkmale

- **Trennung von Inhalt und Design**: während HTML für Struktur ist, ist CSS für Styling.
- **Wiederverwendbarkeit**: Eine CSS-Regel kann auf viele Elemente angewendet werden.
- **Kaskadierung**: Spätere Regeln überschreiben frühere Regeln
- **Spezifität**: Genauere Selektoren haben Vorrang vor allgemeinen.

---

## Grundlegende CSS-Syntax

```css
selektor {
    eigenschaft: wert;
    eigenschaft: wert;
}
```

**Beispiel:**

```css
p {
    color: blue;
    font-size: 16px;
}
```

---

## CSS in HTML einbinden

### 1. Inline-CSS (direkt im HTML-Element)

```html
<p style="color: red; font-size: 20px;">Text</p>
```

**Nachteile**: Nicht wiederverwendbar, schlechte Wartbarkeit, unübersichtlich, zu viel unnötige Arbeit = nicht effizient

### 2. Internes CSS (im `<style>`-Tag)

```html
<head>
    <style>
        p { color: blue; }
    </style>
</head>
```

**Verwendung**: Für einzelne Seiten mit spezifischem Styling, wenn der Code kurz und übersichtlich ist. Gut für einen One-Pager.

### 3. Externes CSS (separate .css-Datei) **EMPFOHLEN**

```html
<head>
    <link rel="stylesheet" href="style.css">
</head>
```

**Vorteile**: Beste Wartbarkeit, Wiederverwendbarkeit, Browser-Caching, man kann mehrere seiten mit demselben oder für jede Seite eigene style erstellen, effiziente und schnellere Arbeit, flexibel

---

## Wichtigste CSS-Regeln und Konzepte

### 1. Das Box-Modell

Jedes HTML-Element ist eine rechteckige Box mit folgenden Bereichen (von innen nach außen):

1. **Content** (Inhalt): Der eigentliche Text/Bild
2. **Padding** (Innenabstand): Raum zwischen Inhalt und Rahmen
3. **Border** (Rahmen): Umrandung des Elements
4. **Margin** (Außenabstand): Raum zwischen Element und anderen Elementen

```css
.box {
    width: 200px;           /* Breite des Inhalts */
    padding: 20px;          /* Innenabstand */
    border: 2px solid black; /* Rahmen */
    margin: 10px;           /* Außenabstand */
}
```

### 2. Spezifität (Wichtigkeit von Selektoren)

CSS-Regeln werden nach ihrer Spezifität angewendet. Je spezifischer, desto höher die Priorität:

1. **Inline-Styles** (höchste Priorität): `style="color: red"`
2. **IDs**: `#header { color: red }`
3. **Klassen, Attribute, Pseudo-Klassen**: `.button { color: red} `, `[type="text"]`, `:hover`
4. **Elemente**: `p { color: red }`, `div { color: red }`

```css
/* Niedrige Spezifität */
p { color: black; }

/* Höhere Spezifität */
.text { color: blue; }

/* Noch höhere Spezifität */
#wichtig { color: red; }
```

### 3. Die Kaskade

Wenn mehrere Regeln auf dasselbe Element zutreffen, gewinnt:

1. Die Regel mit höherer Spezifität
2. Bei gleicher Spezifität: die zuletzt definierte Regel

```css
p { color: blue; }
p { color: red; }  /* Diese Regel gewinnt */
```

---
