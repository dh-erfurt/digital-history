# Von der Quelle zur webbasierten Präsentation
Im Rahmen des Seminars "Von der historischen Quelle zur digitalen Präsentation – datengestützte Forschung, Analyse und Methodik" werden im Wintersemester 2025/2026 von Studierenden digitale Repräsentation diverser Briefe erarbeitet. Datengrundlage hierfür bilden Erfurt betreffende Briefe der Bände 6 bis 14 der [Nürnberger Briefbücher](http://lme70.informatik.uni-erlangen.de:8060/exist/apps/nuernberger-briefbuecher/uebersicht.html), die als Scan und automatisiert transkribiert zur Verfügung stehen. 


## Normalisierung
In einem ersten Schritt überprüfen die Studierenden manuell die Transkription anhand der Scans und normalisieren im Anschluss den transkribierten Text, z.B. durch Ersetzen des Schaft-S. 

```python
text = "hern Nyclaſen hopgarten Probſten des Stiffts cʒu ſant Auguſtin cʒu Erfforden"

normalized_text = re.sub("ſ", "s", text)

print(normalized_text)
``` 

Sie orientieren sich bei der Normalisierung an den [Transkriptionsrichtlinien](http://lme70.informatik.uni-erlangen.de:8060/exist/apps/nuernberger-briefbuecher/editionsprinzipien.html) der digitalen Edition der Nürnberger Briefbücher (Band 2 bis 5).

## Named Entity Recognition
Die Studierenden versuchen zunächst, [Named Entity Recognition](../praxis/nlp-methoden-in-der-digital-history.md) mithilfe von ChatGPT o.ä. durchzuführen. Darüber hinaus testen sie anhand von Wikipedia-Artikeln die NER-Fnktionalität von `spaCy`.

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
- spezialisierte Modelle
- Finetuning des `spaCy`-Modells

## Text zu TEI
In einem nächsten Schritt geht es darum, die identifizierten Entitäten und diplomatischen und normalisierten Fassungen der Briefe in einem einheitlichen TEI-Format zu modellieren. Die Studierenden erarbeiten hierzu ein TEI-Template, das sich für Briefe des Nürnberger Rates eignet. 

## TEI zu HTML (mittels XSLT)
Zum Abschluss transformieren die Studierenden ihre Brief-XML-Dateien mittels XSLT in ein HTML-Format. 

<!-- hier link zu ergebnissen>