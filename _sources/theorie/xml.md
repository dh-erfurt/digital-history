# XML
 
XML (Extensible Markup Language) ist ein standardisiertes Format für hierarchisch strukturierte Daten. XML ist sowohl von Menschen als auch von Maschinen lesbar und es ist plattformunabhängig.

In den Digital Humanities ist XML ein zentrales Format und auch Werkzeug, da es erlaubt, geisteswissenschaftliche Daten (Texte, Metadaten, Editionsprojekte, ...) strukturiert und langfristig zugänglich aufzubereiten.

Dieses Kapitel führt in die grundlegenden Prinzipien von XML ein und widmet sich darauf aufbauend den Grundlagen des auf XML basierenden Dokumentenformats zur Kodierung und zum Austausch von Texten **TEI (Text Encoding Initiative)**, der Programmiersprache zur Transformation von XML-Dokumenten **XSLT (eXtensible Stylesheet Language Transformations)** und anderen XML-basierten Technologien. 

## Einführung XML
XML wurde 1998 vom *W3C (World Wide Web Consortium)* als Auszeichnungssprache und einheitliches, plattformunabhängiges und menschen- sowie maschinenlesbares Format für den Austausch strukturierter Daten entwickelt. XML ist eine Metasprache, d. h. eine Sprache, mit der man andere Sprachen definieren kann.

Im Gegensatz zu HTML, der Auszeichnungssprache für Webseiten, beschreibt XML die Bedeutung seiner Inhalte, nicht ihre Formatierung. 

### Beispiel
```xml
<buch>
  <titel>Der Graf von Monte Cristo</titel>
  <autor>Alexandre Dumas</autor>
  <preis>12.99</preis>
</buch>
```

XML verwendet eine hierarchische Struktur bzw. eine Baumform zur Strukturierung der Daten. Es ist möglich, eigene *Tags* (z. B. `buch`, `autor`) zu definieren, XML legt lediglich die Syntax fest. Wichtig ist vor allem, dass jeder öffnende Tag einen schließenden Tag hat und die Verschachtelung korrekt ist, d. h. Tags nicht überlappen dürfen. 

Zwar ist die Benennung der Tags grundsätzlich frei, sie sollte aber aussagekräftig, konsistent und fachlich sinnvoll sein. So ist <titel> besser verständlich als ein unspezifisches <t1>. Oft orientiert man sich an den Inhalten oder am Anwendungsgebiet (z. B. <gedicht>, <vers> in einer Edition von Gedichten). Einheitliche Benennungen erleichtern sowohl das Lesen durch Menschen als auch die Verarbeitung durch Maschinen.

### Weitere zentrale XML-Konzepte
Zentral für XML sind darüber hinaus:
| Konzept          | Beispiel / Syntax                         | Beschreibung |
|-----------------|------------------------------------------|-------------|
| XML-Deklaration  | `<?xml version="1.0" encoding="UTF-8"?>` | Steht ganz oben in der XML-Datei, gibt Version und Zeichencodierung an, optional |
| Attribute        | `<person name="Goethe" birth="1749-08-28"/>` | Zusätzliche Informationen zu einem Element (Metadaten, IDs), stehen im Start-Tag |
| Kommentare       | `<!-- Das ist ein Kommentar -->`         | Wie in HTML, werden vom Parser ignoriert |

### Wohlgeformtheit
Ein XML-Dokument ist **wohlgeformt**, wenn es sich korrekt an die Syntaxregeln von XML hält. Dazu gehört, dass das Dokument genau ein Wurzelelement hat, dass jeder öffnende Tag einen entsprechenden schließenden Tag hat und dass Elemente korrekt ineinander verschachtelt sind. 

Die offizielle Definition von XML-Wohlgeformtheit findet sich [hier](https://www.w3.org/TR/xml/#dt-wellformed).

### Vokabulare 
Ein Vokabular ist eine Sammlung von Elementnamen und Attributen. Es legt fest, welche Tags (und Attribute) erlaubt sind, was sie bedeuten und wie sie verschachtelt werden dürfen. 
Vokabulare machen Gebrauch von XML als Metasprache und ermöglichen Wiederverwendbarkeit und Interoperabilität.
Beispiele für XML-Vokabulare sind TEI (Text Encoding Initiative) für geisteswissenschaftliche Texte, RSS/Atom (Nachrichten-Feeds) oder MODS (Metadata Object Description Schema) für Bibliotheksmetadaten. 


## TEI

*TEI (Text Encoding Initiative)* ist ein internationaler Standard zur Auszeichnung von Texten in den Geisteswissenschaften, der XML zur Codierung verwendet und communitybasiert und -entwickelt ist.
Ziele sind hierbei:
- Strukturierung, Durchsuchbarkeit und Interoperabilität von Texten
- präzise Repräsentation komplexer textueller Strukturen (z. B. Varianten, Kommentare)
- Langzeitarchivierung und Wiederverwendbarkeit
- erleichterte Zusammenarbeit zwischen Projekten durch Standardisierung

TEI ist so konzipiert, dass vielfältige geisteswissenschaftliche Textsorten adäquat modelliert werden können. Gerade für die Arbeit an [digitalen Editionen](../praxis/digitale-editionen.md) ist es zentral. Sichtbar gemacht werden mit TEI sowohl Struktur (Absätze, Gedichtzeilen, Marginalien...) als auch Semantik (z. B. durch [NER-Auszeichnung](../praxis/nlp-methoden-in-der-digital-history.md)).

### Grundlagen

TEI bietet ein umfangreiches Schema mit über 500 Elementen, u. a. 
- `<teiHeader/>`: Metadaten des Textes
- `<div/>`, `<p/>`: Strukturierung in Absätze, Kapitel etc. 
- `<persName/>`, `<placeName/>`: Personen- und Ortsnamen
- `<note>`: Anmerkungen

Der volle Umfang des TEI-Vokabulars ist [hier](https://tei-c.org/release/doc/tei-p5-doc/de/html/) dokumentiert. 

### Beispiel
```{figure} ../img/shakespeare-sonnet.png
:alt: Shakespeare-Sonnett
:name: sonnet
:align: left
:width: 800px

Shakespeares Sonnett 130 als Beispiel für TEI-Codierung [[Quelle Bild](https://books.openedition.org/oep/688#tocfrom1n2)]
```
<br/>


Dieses Sonnett kann folgendermaßen in TEI codiert werden:
```xml
<lg type="sonnet">
    <head>130</head>
        <l>My Mistres eyes are nothing like the Sunne,</l>
        <l>Currall is farre more red, then her lips red,</l>
        <l>If snow be white why then her brests are dun:</l>
        <l>If haires be wiers, black wiers grow on her head:</l>
        <l>I have seene Roses damaskt, red and white,</l>
        <l>But no such Roses see I in her cheekes,</l>
        <l>And in some perfumes is there more delight,</l>
        <l>Then in the breath that from my Mistres reekes.</l>
        <l>I loue to heare her speake, yet well I know.</l>
        <l>That Musicke hath a farre more pleasing sound:</l>
        <l>I graunt I never saw a goddesse goe,</l>
        <l>My Mistress when she walkes treads on the ground.</l>
    <lg type="couplet">
        <l>And yet by heaven I thinke my love as rare,</l>
        <l>As any she beli'd with false compare.</l>
    </lg>
</lg>

```
[Quelle Beispiel](https://www.dh.unibe.ch/dienstleistungen/tei/index_ger.html)

### Weitere Beispiele
- [Editionsrichtlinien "Der Sturm" (digitale Quellenedition zur Geschichte der internationalen Avantgarde)](https://sturm-edition.de/edition.html)
- [TEI-XML-Datenset der Tagebücher, Briefe, Dokumente, Forschungsbeiträge, Chronologieeinträge und Register der edition humboldt digital](https://zenodo.org/records/16541945)
- [Nuremberg Letterbooks: A Multi-Transcriptional Dataset of Early 15th Century Manuscripts for Document Analysis](https://zenodo.org/records/13881575)

## XSLT
*XSLT (Extensible Stylesheet Language Transformations)* ist eine Programmiersprache zur Transformation von XML-Dokumenten, entweder in andere XML-Dokumente (d. h. veränderte Struktur) oder andere Formate (z. B. HTML für die Publikation im Web). Sie wurde im Kontext des World Wide Web Consortium entwickelt und 1999 veröffentlicht. 

Grundlegende Funktionsweise:

Definition eines XSLT-Stylesheets und eines Input-XMLs → XSLT Processor → Ausgabe eines HTML-Dokuments

### Einführungsbeispiel
Es gibt online XSLT-Prozessoren, mit denen man sein Stylesheet testen kann, z. B. https://linangdata.com/xslt-tester/. 

```{dropdown} Beispiel-XML
```xml
<?xml version="1.0" encoding="UTF-8"?>
<books>
    <book>
        <title>Der Graf von Monte Cristo</title>
        <author>Alexandre Dumas</author>
    </book>
</books>
```

```{dropdown} Beispiel-Stylesheet
```xml
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">
   <xsl:template match="/">
      <html>
         <body>
            <xsl:apply-templates/>
         </body>
      </html>
   </xsl:template>
</xsl:stylesheet>

```

- `<xsl:template\>` definiert ein Template, das mit *match* einen Tag des XML-Dokuments anspricht
    - `match="\\"` spricht das Root-Element des XML-Dokuments an, d. h. das ganze Dokument
- `<xsl:apply-templates\>` wendet das Template auf das aktuelle Element an 

Die Funktionsweise wird anhand eines zweiten Beispiels klarer:

```xml
<xsl:template match="title">
  <h1><xsl:apply-templates/></h1>
</xsl:template>
```
Wenn ein `<title>`-Element gefunden wird, wird daraus eine HTML-Überschrift `<h1>` gemacht.


### Beispiel: Stylesheet mit zwei Templates
```{dropdown} Beispiel mit zwei Templates
```xml
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">
    <xsl:template match="/">
        <html>
            <body>
                <xsl:apply-templates/>
            </body>
        </html>
    </xsl:template>
    <xsl:template match="title">
        <h1><xsl:apply-templates/></h1>
    </xsl:template>
</xsl:stylesheet>
```

#### Was passiert hier?
1. Der Prozessor startet mit dem Root-Template `match="/"`.

2. Er erzeugt das Grundgerüst `<html><body>...</body></html>`.

3. Im `<body>` steht \<xsl:apply-templates\/\>: Der Prozessor überprüft: Was liegt direkt unter der Wurzel im XML? → Das Element `<book>`.

4. Er sucht nach einem Template für `<book>`: Gibt es kein passendes Template, wird `apply-templates` auf die Kinder von `<book>` angewendet, dann auf deren Kinder usw.

5. Er findet `<title>` und `<author>`:

    - Für `<title>` existiert ein Template → Template wird angewendet: `<h1>...</h1>`
    - Für `<author>` existiert kein Template → Text wird direkt ausgegeben

### XSLT-Stylesheet-Elemente

```{dropdown} XML-Beispiel
```xml
<?xml version="1.0" encoding="UTF-8"?>
<books>
    <book>
        <title>Der Graf von Monte Cristo</title>
        <author>Alexandre Dumas</author>
        <year>1845</year>
    </book>
    <book>
        <title>I Who Have Never Known Men</title>
        <author>Jacqueline Harpman</author>
        <year>1995</year>
    </book>
    <book>
        <title>Effi Briest</title>
        <author>Theodor Fontante</author>
        <year>1895</year>
    </book>
</books>
```

#### \<xsl:value-of\>-Element
Mit \<xsl:value-of\> kann der Wert eines XML-Elements extrahiert und dem HTML-Output hinzugefügt werden.

z. B.
```xml
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">
   <xsl:template match="/">
      <html>
         <body>
            <xsl:apply-templates/>
         </body>
      </html>
   </xsl:template>
   <xsl:template match="book">
      <h2><xsl:value-of select="title"/></h2>
      <p>Autor: <xsl:value-of select="author"/></p>
      <p>Erscheinungsjahr: <xsl:value-of select="year"/></p>
  </xsl:template>
</xsl:stylesheet>
```

#### \<xsl:if\>-Element
Mit \<xsl:if\> wird eine Bedingung anhand des XML-Inhaltes überprüft.

z. B.
```xml
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">
    <xsl:template match="/">
        <html>
            <body>
                <xsl:apply-templates select="books/book">
                <xsl:sort select="year" data-type="number" order="ascending"/>
                </xsl:apply-templates>
            </body>
        </html>
    </xsl:template>
</xsl:stylesheet>
```

In XML-Code müssen spitze Klammern (<, >) *escapet* werden, wie z. B. hier in der Bedingung, dass Bücher mit Erscheinungsjahr vor 1900 als Klassiker ausgezeichnet werden.

#### \<xsl:sort\>-Element
Mit \<xsl:sort\> kann man die Inhalte sortieren.

z. B. 
```xml
<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">
    <xsl:template match="/">
        <html>
            <body>
                <xsl:apply-templates select="books/book">
                <xsl:sort select="year" data-type="number" order="ascending"/>
                </xsl:apply-templates>
            </body>
        </html>
    </xsl:template>
</xsl:stylesheet>
```

Weitere Elemente und Möglichkeiten eines XSL-Stylesheets finden sich u. a. hier:
- https://www.w3schools.com/xml/xsl_intro.asp
- https://en.wikipedia.org/wiki/XSLT_elements

## Weiterführende Informationen
- TEI Dokumentation: https://tei-c.org/release/doc/tei-p5-doc/de/html/
- Crashkurs TEI: https://www.dh.unibe.ch/dienstleistungen/tei/index_ger.html
- Elsner, Frank: Einführung in XML. https://www.home.uni-osnabrueck.de/elsner/Skripte/xml.pdf
- Thilo Rottach, Sascha Groß. XML kompakt: die wichtigsten Standards. Spektrum 2002. 