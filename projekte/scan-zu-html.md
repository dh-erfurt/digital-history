# Von der Quelle zur webbasierten Präsentation
Im Rahmen des Seminars "Von der historischen Quelle zur digitalen Präsentation – datengestützte Forschung, Analyse und Methodik" werden im Wintersemester 2025/2026 von Studierenden digitale Repräsentationen diverser Briefe erarbeitet. 

Datengrundlage hierfür bilden Erfurt betreffende Briefe der Bände 6 bis 14 der [Nürnberger Briefbücher](http://lme70.informatik.uni-erlangen.de:8060/exist/apps/nuernberger-briefbuecher/uebersicht.html), die als Scan und automatisiert transkribiert zur Verfügung stehen. Jede\*r Studierende übernimmt die Verantwortung für einen Brief. 

## Scan und Transkription
Zu Beginn des Praxisteils wird den Studierenden der Scan eines Briefes bereitgestellt. Anhand verschiedener OCR-Tools (frei zugängliche Online-Tools, Kraken) testen die Studierenden die Möglichkeiten automatisierter Transkription und identifizieren Herausforderungen, die mittelalterliche Handschriften mit sich bringen:
- verschiedene Schriften und Schreibstile (NBB: 10 Schreiber in den ersten 5 Briefbüchern)
- materialbedingte Schwierigkeiten: Beschädigungen, Verfärbungen etc.
- verkettete Buchstaben und Abkürzungen
- fehlende Standardisierung
- dekorative Elemente / Illustrationen
- Durchstreichungen


## Normalisierung
Den Studierenden wird eine automatisiert erstellte Transkription ihres Briefes zur Verfügung gestellt. 
<!-- hier noch INfos dazu, wie die erstellt wurde -->
Sie überprüfen manuell die Transkription anhand der Scans und normalisieren im Anschluss den transkribierten Text, z. B. durch Ersetzen des Schaft-S. 

```python
text = "hern Nyclaſen hopgarten Probſten des Stiffts cʒu ſant Auguſtin cʒu Erfforden"

normalized_text = re.sub("ſ", "s", text)

print(normalized_text)
``` 

Sie orientieren sich bei der Normalisierung an den [Transkriptionsrichtlinien](http://lme70.informatik.uni-erlangen.de:8060/exist/apps/nuernberger-briefbuecher/editionsprinzipien.html) der digitalen Edition der Nürnberger Briefbücher (Band 2 bis 5).

## Named Entity Recognition

Um das Konzept kennenzulernen, üben die Studierenden zunächst mit Wikipedia-Artikeln, für die aufgrund ihrer Verwendung von Standardsprache viele NER-Technologien gut funktionieren.
Die Studierenden versuchen zunächst, [Named Entity Recognition](../praxis/nlp-methoden-in-der-digital-history.md) mithilfe von ChatGPT o. ä. durchzuführen. Darüber hinaus testen sie die NER-Funktionalität von `spaCy`.

```python
import spacy

nlp = spacy.load('de_core_news_sm')

text = "Erfurt ist seit 1991 ... Evangelischen Kirche in Mitteldeutschland."

doc = nlp(text)
for ent in doc.ents:
    print(ent.text, ent.start_char, ent.end_char, ent.label_)
```

Im Anschluss versuchen sie, NER für die historischen Briefe durchzuführen und reflektieren, was hierbei Hürden sein könnten. 

Es werden Möglichkeiten aufgezeigt, die Performance zu verbessern: 
- weitere Normalisierung des Textes
- spezialisierte Modelle, insbesondere `xlm-roberta`
- Finetuning des `spaCy`-Modells mit Trainingsdaten

## Text zu TEI
In einem nächsten Schritt geht es darum, die identifizierten Entitäten und diplomatischen und normalisierten Fassungen der Briefe in einem einheitlichen [TEI](../theorie/xml.md)-Format zu modellieren.
Die Studierenden stellen fest, welche Besonderheiten das Briefformat bei der Datenmodellierung mit sich bringt:
- Spezifika von Briefen:
    - Absender
    - Empfänger
    - erwähnte Orte/Personen/Organisationen (als Metadaten/im Text?)
- Einbindung des Facsimile (=Scan)
- Anrede/Grußformel
- zwei Textversionen: diplomatisch + normalisiert
- Wie gehen wir damit um, wenn ein Brief mehrere Seiten hat? (d.h. auch mehrere Facsimiles)

In Gruppenarbeit erarbeiten sie ein TEI-Template, das sich für Briefe des Nürnberger Rates eignet. 

## TEI zu HTML (mittels XSLT)
Zum Abschluss transformieren die Studierenden ihre Brief-XML-Dateien mittels [XSLT](../theorie/xml.md) in ein HTML-Format. 
Dazu lernen sie zunächst grundlegende Konzepte von XSLT kennen und üben anhand einfacher XML-Beispiele. 
Abschließend erstellen sie, aufbauend auf einem simplen XSL-Stylesheet für die Briefbücher-XMLs, individuelle Stylesheets und schaffen so eine digitale Präsentation ihres Briefes im HTML-Format.


## Ergebnisse
Nach Abschluss des Seminars werden hier die Ergebnisse veröffentlicht, die die Studierenden erarbeitet haben.
<!-- hier link zu ergebnissen>##