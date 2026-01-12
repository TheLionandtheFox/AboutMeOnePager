# CSS Farben & Hintergründe

> Eine ausführliche Erklärung mit vielen praktischen Beispielen

## Einführung: Farben in CSS

Farben sind eines der wichtigsten Gestaltungsmittel im Webdesign. Sie beeinflussen die Stimmung, Lesbarkeit und Markenidentität einer Website. CSS bietet verschiedene Möglichkeiten, Farben zu definieren – von einfachen Farbnamen bis zu komplexen Farbräumen mit Transparenz.

---

## Teil 1: Die `color`-Eigenschaft

Die `color`-Eigenschaft in CSS bestimmt die Farbe des Textes innerhalb eines Elements. Sie ist eine der am häufigsten verwendeten CSS-Eigenschaften und bildet die Grundlage für lesbare und ansprechende Typografie.

### Grundlegende Syntax

```css
p {
    color: red;
}
```

Diese einfache Regel färbt den Text aller `<p>`-Elemente rot. Die `color`-Eigenschaft wird vererbt – das bedeutet, wenn man sie auf ein Elternelement setzt, erben alle Kindelemente diese Farbe, sofern sie nicht explizit überschrieben wird.

### Farbdefinition: Verschiedene Formate

CSS unterstützt mehrere Formate zur Farbangabe, jedes mit seinen eigenen Vor- und Nachteilen.

---

### 1. Farbnamen (Named Colors)

CSS kennt 147 vordefinierte Farbnamen wie `red`, `blue`, `green`, `white`, `black` usw. Diese sind intuitiv und leicht zu merken.

```css
h1 {
    color: crimson;
}

p {
    color: navy;
}

.highlight {
    color: gold;
}
```

**Vorteile:**

- Einfach zu schreiben und zu merken
- Gut für schnelles Prototyping
- Selbstdokumentierend (man sieht sofort, welche Farbe gemeint ist)

**Nachteile:**

- Begrenzte Auswahl (nur 147 Farben)
- Nicht präzise genug für professionelles Design
- Verschiedene Browser können Farbnamen minimal unterschiedlich interpretieren

**Häufige Farbnamen:**

- `white` (#FFFFFF) – Weiß
- `black` (#000000) – Schwarz
- `red` (#FF0000) – Rot
- `blue` (#0000FF) – Blau
- `green` (#008000) – Grün
- `gray` / `grey` (#808080) – Grau
- `darkgray` (#A9A9A9) – Dunkelgrau
- `lightgray` (#D3D3D3) – Hellgrau
- `silver` (#C0C0C0) – Silber

**Anwendungsfall:** Farbnamen eignen sich hauptsächlich für Entwicklungsumgebungen, schnelles Testen oder wenn man sehr gebräuchliche Farben benötigt. Für professionelle Projekte sollte man präzisere Formate verwenden.

---

### 2. Hexadezimal (Hex-Codes)

Hexadezimale Farbcodes sind das am häufigsten verwendete Format in professionellem Webdesign. Sie bestehen aus einem Hash-Symbol (#) gefolgt von 6 Zeichen (0-9 und A-F), die die Rot-, Grün- und Blau-Anteile der Farbe repräsentieren.

```css
p {
    color: #ff0000;  /* Rot */
}

h2 {
    color: #0000ff;  /* Blau */
}

.text {
    color: #3498db;  /* Ein helles Blau */
}
```

**Aufbau eines Hex-Codes:**

`#RRGGBB` – wobei:

- **RR** = Rot (00 bis FF)
- **GG** = Grün (00 bis FF)
- **BB** = Blau (00 bis FF)

Jedes Paar kann Werte von 00 (keine Farbe) bis FF (maximale Farbe) annehmen. FF in Hexadezimal entspricht 255 in Dezimal.

**Beispiele mit Erklärung:**

```css
#000000  /* Schwarz (kein Rot, kein Grün, kein Blau) */
#FFFFFF  /* Weiß (maximales Rot, Grün und Blau) */
#FF0000  /* Reines Rot (nur Rot-Kanal voll) */
#00FF00  /* Reines Grün */
#0000FF  /* Reines Blau */
#808080  /* Mittleres Grau (alle Kanäle bei 50%) */
#FF00FF  /* Magenta (Rot + Blau) */
#00FFFF  /* Cyan (Grün + Blau) */
#FFFF00  /* Gelb (Rot + Grün) */
```

**Kurzform (3-stellig):**

Wenn beide Zeichen eines Farbkanals identisch sind, kann man die Kurzform verwenden:

```css
#f00  /* Gleich wie #ff0000 (Rot) */
#0f0  /* Gleich wie #00ff00 (Grün) */
#00f  /* Gleich wie #0000ff (Blau) */
#fff  /* Gleich wie #ffffff (Weiß) */
#000  /* Gleich wie #000000 (Schwarz) */
#369  /* Gleich wie #336699 */
```

Der Browser erweitert automatisch: `#f00` wird zu `#ff0000`.

**Hex mit Transparenz (8-stellig):**

Moderne Browser unterstützen auch 8-stellige Hex-Codes für Transparenz:

```css
#ff000080  /* Rot mit 50% Transparenz */
#3498dbff  /* Volles Blau (FF = 100% opak) */
#00000000  /* Komplett transparent */
```

Die letzten zwei Zeichen (00-FF) bestimmen den Alpha-Kanal (Transparenz):

- `00` = komplett transparent
- `80` = 50% transparent
- `FF` = komplett deckend

**Vorteile:**

- Präzise Farbdefinition (16,7 Millionen Farben möglich)
- Kompakte Schreibweise
- Weit verbreitet und von allen Design-Tools unterstützt
- Gut lesbar, wenn man das System versteht

**Nachteile:**

- Nicht intuitiv für Anfänger
- Schwer, Farben "im Kopf" zu mischen
- Transparenz erfordert 8-stellige Codes (nicht alle Tools unterstützen das)

**Praxis-Tipp:** Man kann Hex-Codes aus Design-Tools (Figma, Photoshop, etc.) kopieren oder Online-Farbwähler nutzen. Moderne Code-Editoren zeigen oft eine Farbvorschau neben dem Code an.

---

### 3. RGB (Red Green Blue)

RGB definiert Farben durch Mischung von Rot, Grün und Blau. Jeder Kanal kann Werte von 0 bis 255 annehmen (insgesamt 256 Stufen pro Kanal).

```css
p {
    color: rgb(255, 0, 0);    /* Rot */
    color: rgb(0, 255, 0);    /* Grün */
    color: rgb(0, 0, 255);    /* Blau */
    color: rgb(128, 128, 128); /* Mittleres Grau */
}
```

**Syntax:**

```css
rgb(rot, grün, blau)
```

Jeder Wert ist eine Zahl von 0 bis 255.

**Wie RGB funktioniert:**

RGB ist ein additives Farbmodell – man startet mit Schwarz (keine Farbe) und addiert Licht:

- `rgb(0, 0, 0)` = Schwarz (kein Licht)
- `rgb(255, 255, 255)` = Weiß (alle Lichter voll)
- `rgb(255, 0, 0)` = Rot (nur roter Kanal)
- `rgb(255, 255, 0)` = Gelb (Rot + Grün = Gelb)
- `rgb(0, 255, 255)` = Cyan (Grün + Blau = Cyan)

**Vorteile von RGB:**

- Intuitiver als Hex, da man mit Dezimalzahlen arbeitet
- Einfacher zu verstehen, welche Farbe entsteht
- Leichter programmatisch zu manipulieren (z.B. mit JavaScript)

**Nachteile:**

- Längere Schreibweise als Hex
- Keine Transparenz (dafür gibt es RGBA)

**Umrechnung Hex zu RGB:**

Um einen Hex-Code zu RGB umzurechnen:

1. Teile den Hex-Code in drei Paare: RR GG BB
2. Rechne jedes Paar von Hexadezimal zu Dezimal um

Beispiel: `#3498db`

- `34` (hex) = 52 (dezimal)
- `98` (hex) = 152 (dezimal)
- `db` (hex) = 219 (dezimal)
- Ergebnis: `rgb(52, 152, 219)`

**Praxis-Beispiel:**

```css
.button-primary {
    background-color: rgb(52, 152, 219);  /* Ein helles Blau */
    color: rgb(255, 255, 255);            /* Weißer Text */
}

.button-primary:hover {
    background-color: rgb(41, 128, 185);  /* Dunkleres Blau beim Hover */
}
```

---

### 4. RGBA (RGB mit Alpha/Transparenz)

RGBA erweitert RGB um einen vierten Wert: den Alpha-Kanal für Transparenz. Alpha reicht von 0 (komplett transparent) bis 1 (komplett deckend).

```css
p {
    color: rgba(255, 0, 0, 0.5);   /* Rotes Halbtransparent */
    color: rgba(0, 0, 0, 0.8);     /* Fast deckend Schwarz */
    color: rgba(255, 255, 255, 0.1); /* Fast transparent Weiß */
}
```

**Syntax:**

```css
rgba(rot, grün, blau, alpha)
```

- **rot, grün, blau**: 0-255
- **alpha**: 0.0 bis 1.0 (oder 0% bis 100%)

**Alpha-Werte verstehen:**

- `0` oder `0.0` = komplett transparent (unsichtbar)
- `0.5` = 50% transparent (halbtransparent)
- `1` oder `1.0` = komplett deckend (keine Transparenz)

**Wichtiger Unterschied zu `opacity`:**

`rgba()` macht nur die Farbe transparent, während `opacity` das gesamte Element samt Inhalt transparent macht:

```css
/* Nur der Hintergrund ist transparent */
.box {
    background-color: rgba(0, 0, 0, 0.5);
    color: white;  /* Text bleibt voll deckend */
}

/* Das GESAMTE Element wird transparent (inkl. Text!) */
.box {
    background-color: black;
    opacity: 0.5;  /* Text wird auch transparent */
}
```

**Praxis-Beispiele:**

Beispiel 1: **Overlay über Bild**

```css
.image-overlay {
    position: relative;
}

.image-overlay::after {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);  /* Dunkles Overlay */
}
```

Beispiel 2: **Glasmorphismus-Effekt**

```css
.glass-card {
    background-color: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.2);
}
```

Beispiel 3: **Sanfter Schatten mit Transparenz**

```css
.card {
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1),
                0 2px 4px rgba(0, 0, 0, 0.06);
}
```

Die Transparenz ermöglicht es, dass Schatten natürlicher aussehen und sich an den Hintergrund anpassen.

Beispiel 4: **Hover-Effekt mit Transparenz**

```css
.button {
    background-color: rgb(52, 152, 219);
    transition: background-color 0.3s;
}

.button:hover {
    background-color: rgba(52, 152, 219, 0.8);
}
```

---

### 5. HSL (Hue, Saturation, Lightness)

HSL ist ein alternatives Farbmodell, das für Menschen intuitiver ist als RGB. Es definiert Farben durch Farbton, Sättigung und Helligkeit.

```css
p {
    color: hsl(0, 100%, 50%);     /* Rot */
    color: hsl(120, 100%, 50%);   /* Grün */
    color: hsl(240, 100%, 50%);   /* Blau */
    color: hsl(0, 0%, 50%);       /* Grau */
}
```

**Syntax:**

```css
hsl(hue, saturation, lightness)
```

**Die drei Komponenten erklärt:**

1. **Hue (Farbton)**: 0-360 Grad auf dem Farbkreis
   - 0° / 360° = Rot
   - 60° = Gelb
   - 120° = Grün
   - 180° = Cyan
   - 240° = Blau
   - 300° = Magenta

2. **Saturation (Sättigung)**: 0% bis 100%
   - 0% = Graustufe (keine Farbe)
   - 50% = Mäßig gesättigt
   - 100% = Voll gesättigt (kräftige Farbe)

3. **Lightness (Helligkeit)**: 0% bis 100%
   - 0% = Schwarz
   - 50% = Normale Farbe
   - 100% = Weiß

**Visualisierung:**

```css
/* Gleicher Farbton (Rot), unterschiedliche Sättigung */
hsl(0, 100%, 50%)  /* Kräftiges Rot */
hsl(0, 75%, 50%)   /* Weniger gesättigtes Rot */
hsl(0, 50%, 50%)   /* Noch weniger gesättigt */
hsl(0, 0%, 50%)    /* Grau (keine Sättigung) */

/* Gleicher Farbton (Blau), unterschiedliche Helligkeit */
hsl(240, 100%, 10%)  /* Sehr dunkles Blau */
hsl(240, 100%, 30%)  /* Dunkles Blau */
hsl(240, 100%, 50%)  /* Normal Blau */
hsl(240, 100%, 70%)  /* Helles Blau */
hsl(240, 100%, 90%)  /* Sehr helles Blau */
```

**Vorteile von HSL:**

- Intuitiver für Menschen (man denkt eher in "Farbton" als in RGB-Werten)
- Einfach, Farbvariationen zu erstellen (z.B. hellere/dunklere Versionen)
- Perfekt für programmatische Farbgenerierung
- Großartig für konsistente Farbpaletten

Praxis-Beispiel: **Farbpalette generieren**

```css
:root {
    --hue: 210;  /* Blau-Farbton */
}

.color-primary {
    background-color: hsl(var(--hue), 80%, 50%);
}

.color-primary-light {
    background-color: hsl(var(--hue), 80%, 70%);  /* Hellere Version */
}

.color-primary-dark {
    background-color: hsl(var(--hue), 80%, 30%);  /* Dunklere Version */
}

.color-primary-pale {
    background-color: hsl(var(--hue), 30%, 90%);  /* Sehr blass */
}
```

Durch Änderung nur der `--hue`-Variable kann man die gesamte Farbpalette auf einen anderen Farbton umstellen!

---

### 6. HSLA (HSL mit Alpha)

Wie RGBA erweitert HSLA das HSL-Format um Transparenz.

```css
p {
    color: hsla(0, 100%, 50%, 0.5);    /* Halbtransparentes Rot */
    color: hsla(120, 100%, 50%, 0.3);  /* 30% deckend Grün */
}
```

**Syntax:**

```css
hsla(hue, saturation, lightness, alpha)
```

Praxis-Beispiel: **Dynamisches Theme mit Transparenz**

```css
:root {
    --theme-hue: 210;
}

.overlay {
    background-color: hsla(var(--theme-hue), 50%, 30%, 0.9);
}

.highlight {
    background-color: hsla(var(--theme-hue), 80%, 60%, 0.2);
}
```

---

## Moderne Farbformate (Bonus)

### HWB (Hue, Whiteness, Blackness)

Ein neueres, noch intuitiveres Format (seit 2021 in allen modernen Browsern):

```css
p {
    color: hwb(0 0% 0%);      /* Reines Rot */
    color: hwb(0 50% 0%);     /* Rot mit 50% Weiß gemischt */
    color: hwb(0 0% 50%);     /* Rot mit 50% Schwarz gemischt */
}
```

---

## Teil 2: Hintergründe

Hintergründe sind ein essentielles Gestaltungselement in CSS. Sie können einfarbig sein, Bilder enthalten, Verläufe verwenden oder aus mehreren Schichten bestehen.

### `background-color` - Hintergrundfarbe

Die `background-color`-Eigenschaft setzt eine solide Hintergrundfarbe für ein Element. Sie akzeptiert alle Farbformate, die wir bereits besprochen haben.

```css
div {
    background-color: lightblue;
}

.header {
    background-color: #3498db;
}

.overlay {
    background-color: rgba(0, 0, 0, 0.5);
}
```

**Wichtig zu verstehen:** Die Hintergrundfarbe füllt den gesamten Bereich des Elements, einschließlich Padding, aber nicht das Margin. Die Hintergrundfarbe erstreckt sich bis zum äußeren Rand des Borders.

**Box-Model und Hintergrundfarbe:**

```
┌─────────── Margin (transparent) ───────────┐
│ ┌─────── Border ──────┐                    │
│ │ ┌─── Padding ────┐  │ ← background-color │
│ │ │   Content      │  │ ← füllt bis hier   │
│ │ └────────────────┘  │                    │
│ └─────────────────────┘                    │
└────────────────────────────────────────────┘
```
