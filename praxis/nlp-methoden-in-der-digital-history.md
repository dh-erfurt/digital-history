# NLP-Methoden in der Digital History
*Natural Language Processing (NLP)* befasst sich damit, wie Computer natürliche Sprache interpretieren, analysieren und generieren können. Für die Geschichtswissenschaft ermöglicht NLP neue Möglichkeiten der Erschließung großer Textmengen. Dabei reicht das Spektrum der Anwendungen von der Erkennung und Klassifizierung historischer Personen und Orte zur Analyse von Stimmungen, Schreibstilen oder sozialen Netzwerken.

## Optical Character Recognition (OCR)
Um NLP-Methoden auf historische Texte anwenden zu können, müssen sie in maschinenlesbarer Form vorliegen. Da viele Quellen nur als Scans zur Verfügung stehen, ist *Optical Character Recognition (OCR)* als Zwischenschritt notwendig. Dabei werden Zeichenfolgen und Texten automatisch aus gescannten Bildern extrahiert. Gerade historische Texte bringen hier besondere Herausforderungen mit sich: Alte Druckschriften wie Fraktur, verblasste Tinte, beschädigte Seiten und wenig normierte Sprache erschweren den Prozess. Spezialisierte OCR-Engines wie *Tesseract*, *eSriptorium*, *Kraken* und *Transkribus* bieten Modelle, die auf historischen Schriften optimiert wurden. Trotzdem ist häufig Finetuning dieser Modelle nötig und eine Post-OCR-Korrektur bleibt unverzichtbar. Mit dem Aufkommen von leistungsstarken LLMs (s. [Künstliche Intelligenz](kuenstliche-intelligenz.md)) ergeben sich hier neue Potentiale, den OCR-Prozess zu optimieren.


## Named Entity Recognition
*Named Entity Recognition (NER)* bezeichnet die Aufgabe, Entitäten in Texten zu erkennen und zu klassifizieren (z. B. Personen, Orte, Organisationen, Zeitangaben etc.) {cite:p}`li_survey_2022`. Gerade im Kontext der Geschichtswissenschaften ist es hilfreich zu wissen, wer in historischen Quellen erwähnt wird und welche Orte und Institutionen dabei eine Rolle spielen. *NER* ist also eine wichtige Basis für weitergehende Analysen, z. B. für die Untersuchung historischer Kommunikationsnetze, geografischer Bezüge oder institutioneller Strukturen.

Gängige Bibliotheken wie *spaCy*, *NLTK* oder *Stanford NER* bieten derartige Funktionalität einsatzfertig an und lassen sich darüber hinaus für spezifische Korpora trainieren, was bei historischen Texten aufgrund abweichender Orthografie, Ausdrucksweise und Zeichensetzung häufig nötig ist. 
Auch LLMs, deren Hauptaufgabe es ist, Sprache zu verstehen, haben sich als sehr hilfreich für *NER* erwiesen.

```{figure} ../img/ner.png
:alt: Beispiel Named Entity Recognition
:name: ner
:align: left

In dem Beispieltext sind Entitäten wie Orte, Organisationen und numerische Angaben ausgezeichnet.
```
<br/>

{numref}`ner` zeigt einen Beispieltext, in dem Entitäten gekennzeichnet wurden. Anhand dieses kurzen Beispiels wird auch ein zentrales Problem der *NER* deutlich, nämlich die Ambiguität zwischen Ort und Organisation (z. B. „Universität Erfurt“).


## Topic Modelling
*Topic Modelling* ist ein weiteres Anwendungsgebiet von NLP und untersucht, welche Themen in einer großen Textsammlung vorkommen. Im Kontext der Geschichtswissenschaft lässt sich so z. B. aufzeigen, welche Themen in Zeitungen einer Epoche dominieren. 

Sinnvoll ist das vor allem bei großen Textsammlungen, doch auch für kurze Textausschnitte kann *Topic Modelling* vorgenommen werden.


Im Folgenden betrachten wir diesen Beispieltext aus der Rhein-Ruhr-Zeitung vom 07.01.1919. [[Quelle](https://www.deutsche-digitale-bibliothek.de/newspaper/item/ZBJ3S5LCHJIKSQHDTL4URASFOIV4RYXY?issuepage=8)]

```{dropdown} Zeitungsartikel

Erfurt, der Ort der Nationalversammlung!
Nach Weimar, Leipzig und Nürnberg ist nunmehr von den Volksbeauftragten als Ort der Nationalversammlung Erfurt in Aussicht genommen. 
Es ist auch Aussicht vorhanden, dass die uralte Metropole Thüringens, das als Binnen- und Industriestadt gleich geschätzte Erfurt, die kommende deutsche Nationalversammlung in ihren Mauern sehen wird.
Alle politischen Parteien Deutschlands verknüpfen mit dem Namen Erfurt besondere Erinnerungen an ihre eigene Geschichte.
```

Ein simples Topic Modelling des Zeitungsartikels mithilfe von *ChatGPT* ergibt Folgendes:

Identifizierte Themen (Topics):
- Ort der Nationalversammlung
    - Begriffe: „Nationalversammlung“, „Volksbeauftragte“, „in Aussicht genommen“, „kommende“
    - Bedeutung: Der Text berichtet, dass Erfurt als möglicher Veranstaltungsort für eine deutsche Nationalversammlung diskutiert wird.

- Symbolische Bedeutung Erfurts für die Parteien
    - Begriffe: „besondere Erinnerungen“, „eigene Geschichte“, „alle politischen Parteien“
    - Bedeutung: Erfurt wird als Ort mit historischer Bedeutung für verschiedene politische Bewegungen dargestellt.

- Charakteristik der Stadt Erfurt
    - Begriffe: „uralte Metropole Thüringens“, „Binnenstadt“, „Industriestadt“
    - Bedeutung: Die Stadt wird geographisch und wirtschaftlich eingeordnet und gewürdigt.

[Hier](https://journalofdigitalhumanities.org/2-1/topic-modeling-and-digital-humanities-by-david-m-blei/) werden beispielsweise 1.8 Millionen Artikel der *New York Times* auf ihre Themen hin untersucht und die Potenziale, die *Topic Modelling* bietet, beleuchtet.


## Sentiment Analysis / Emotion Analysis
Im Rahmen von *Sentiment Analysis* (positiv/negativ/neutral) bzw. *Emotion Analysis* (feinere Untergliederung) wird die Stimmung und/oder emotionale Haltung eines Texts eingeschätzt, was in geschichtswissenschaftlicher Forschung u. a. bei der Bewertung von politischen Reden, Zeitungsartikeln und Briefen oder im Allgemeinen bei der Auswertung öffentlicher Meinung unterstützen kann. Hier stehen klassische, lexikonbasierte Ansätze neueren Machine-Learning-Ansätzen gegenüber. Auch LLMs können effizient eingesetzt werden.   


Eine *Sentiment-* bzw. *Emotionsanalyse* des obigen Zeitungsartikels mittels *ChatGPT* ergibt: 

| Textausschnitt                                                                                                                                 | Sentiment | Emotion                | Erklärung |
| ---------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ---------------------- | --------- |
| "Erfurt, der Ort der Nationalversammlung!"                                                                                                     | Positiv   | Stolz / Bedeutung      | Ausrufezeichen und klare Hervorhebung des Ortes vermitteln feierliche und stolze Stimmung. |
| "Nach Weimar, Leipzig und Nürnberg ist nunmehr ... Erfurt in Aussicht genommen."                                                               | Neutral   | Erwartung / Ankündigung| Nüchterne Mitteilung über die Auswahl des Ortes, ohne emotionale Wertung. |
| "Es ist auch Aussicht vorhanden, dass die uralte Metropole Thüringens ... die kommende deutsche Nationalversammlung in ihren Mauern sehen wird." | Positiv   | Optimismus / Hoffnung  | Formulierung „Aussicht vorhanden“ und positive Zuschreibung („uralte Metropole“) deuten auf zuversichtliche Haltung hin. |
| "das als Binnen- und Industriestadt gleich geschätzte Erfurt"                                                                                  | Positiv   | Anerkennung / Respekt  | Wertschätzende Beschreibung mit gleichzeitiger Betonung von wirtschaftlicher und geographischer Bedeutung. |
| "Alle politischen Parteien Deutschlands verknüpfen mit dem Namen Erfurt besondere Erinnerungen an ihre eigene Geschichte."                     | Positiv   | Nostalgie / Verbundenheit| „Besondere Erinnerungen“ und Bezug auf Geschichte wecken positive, gemeinschaftliche Gefühle. |


## Textklassifikation
Textklassifikation umfasst eine Vielzahl von Methoden, die Texte nach Merkmalen wie Genre, Thema, Stil oder Autorenschaft systematisch einordnen und analysieren. So lassen sich große Textkorpora strukturieren, Muster erkennen und historische Zusammenhänge besser verstehen.
Ein Beispiel dafür ist Stilometrie – die Analyse individueller Schreibstile anhand sprachlicher Merkmale (z. B. Wortwahl, Satzstruktur). Ein Ziel kann hier beispielsweise sein, Autorenschaft zu erkennen oder mehrere Autoren in einem Text abzugrenzen.

Für den kurzen Abschnitt aus obigem Beispiel trifft *ChatGPT* folgende Stilometrie-Analyse.

| Merkmal   | Beschreibung                               |
| --------- | ------------------------------------------ |
| Satzlänge | Mittel bis lang, oft komplex               |
| Wortwahl  | Formal, historisch, politisch konnotiert   |
| Stilistik | Nominalstil, geringe Emotionalisierung     |
| Tempus    | Präsens / Futurisch mit prognostischem Ton |
| Funktion  | Informativ und legitimierend (politisch)   |

Auch bei der Stilometrie ist die Methode besonders sinnvoll im Kontext von großen Textsammlungen – hier lassen sich die Ähnlichkeiten zwischen verschiedenen Texten messen und Stile quantisieren.


# Quellen und weiterführende Ressourcen
Es gibt viele hilfreiche Online-Ressourcen zum Thema NLP, z. B. 
- [Überblick/Tutorial zu Named Entity Recognition mit Python](https://www.geeksforgeeks.org/named-entity-recognition/)
- [Einführung/Tutorial zu Topic Modelling mit Python](https://python-textbook.pythonhumanities.com/04_topic_modeling/04_01_01_intro.html)

## Zitierte Literatur
```{bibliography}
:filter: docname in docnames
```