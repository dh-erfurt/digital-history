# NLP-Methoden in der Digital History
## Named Entity Recognition
*Named Entity Recognition (NER)* bezeichnet die Aufgabe, Entitäten in Texten zu erkennen und zu klassifizieren (z. B. Personen, Orte, Organisationen, Zeitangaben etc.) {cite:p}`li_survey_2022`. Gerade im Kontext der Geschichtswissenschaften ist es hilfreich zu wissen, wer in historischen Quellen erwähnt wird und welche Orte und Institutionen dabei eine Rolle spielen. *NER* ist also eine wichtige Basis für weitergehende Analysen, z. B. für die Untersuchung historischer Kommunikationsnetze, geografischer Bezüge oder institutioneller Strukturen.

```{figure} ../img/ner.png
:alt: Beispiel Named Entity Recognition
:name: ner
:align: left

In dem Beispieltext sind Entitäten wie Orte, Organisationen und numerische Angaben ausgezeichnet.
```
<br/>

LLMs, deren Hauptaufgabe es ist, Sprache zu verstehen, haben sich als sehr hilfreich für *NER* erwiesen. 

{numref}`ner` zeigt einen Beispieltext, in dem Entitäten gekennzeichnet wurden. Anhand dieses kurzen Beispiels wird auch ein zentrales Problem der *NER* deutlich, nämlich die Ambiguität zwischen Ort und Organisation (z. B. „Universität Erfurt“).
## Topic Modelling
*Topic Modelling* ist ein weiteres Anwendungsgebiet von LLMs und untersucht, welche Themen in einer großen Textsammlung vorkommen. Im Kontext der Geschichtswissenschaft lässt sich so z. B. aufzeigen, welche Themen in Zeitungen einer Epoche dominieren. 

Sinnvoll ist das vor allem bei großen Textsammlungen, doch auch für kurze Textausschnitte kann *Topic Modelling* vorgenommen werden, hier anhand obigen Zeitungsartikels mithilfe von *ChatGPT*.

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
Im Rahmen von *Sentiment Analysis* wir die Stimmung und/oder emotionale Haltung eines Texts eingeschätzt, was in geschichtswissenschaftlicher Forschung u. a. bei der Bewertung von politischen Reden, Zeitungsartikeln und Briefen oder im Allgemeinen bei der Auswertung öffentlicher Meinung unterstützen kann. Auch hierbei können LLMs effizient eingesetzt werden.   
TODO: Unterscheidung Sentiment / Emotion

Im Folgenden betrachten wir diesen Beispieltext aus der Rhein-Ruhr-Zeitung vom 07.01.1919. [[Quelle](https://www.deutsche-digitale-bibliothek.de/newspaper/item/ZBJ3S5LCHJIKSQHDTL4URASFOIV4RYXY?issuepage=8)]

```{dropdown} Zeitungsartikel

Erfurt, der Ort der Nationalversammlung!
Nach Weimar, Leipzig und Nürnberg ist nunmehr von den Volksbeauftragten als Ort der Nationalversammlung Erfurt in Aussicht genommen. 
Es ist auch Aussicht vorhanden, dass die uralte Metropole Thüringens, das als Binnen- und Industriestadt gleich geschätzte Erfurt, die kommende deutsche Nationalversammlung in ihren Mauern sehen wird.
Alle politischen Parteien Deutschlands verknüpfen mit dem Namen Erfurt besondere Erinnerungen an ihre eigene Geschichte.
```

Eine simple *Sentimentsanalyse* mit *ChatGPT* ergibt Folgendes:

| Satz                                                                                                                       | Tonlage / Sentiment               | Hinweise                                                                          |
| -------------------------------------------------------------------------------------------------------------------------- | --------------------------------- | --------------------------------------------------------------------------------- |
| *Erfurt, der Ort der Nationalversammlung!*                                                                                 | **Positiv / Feierlich**           | Ausrufezeichen, Betonung auf Bedeutung und Ehre                                   |
| *\[...] ist nunmehr von den Volksbeauftragten als Ort der Nationalversammlung Erfurt in Aussicht genommen.*                | **Neutral bis leicht positiv**    | Sachliche Mitteilung, aber durch die Auswahl Erfurts mitschwingende Wertschätzung |
| *\[...] die uralte Metropole Thüringens, das als Binnen- und Industriestadt gleich geschätzte Erfurt \[...]*               | **Positiv / wertschätzend**       | Lobende Adjektive: "uralte Metropole", "geschätzt"                                |
| *\[...] die kommende deutsche Nationalversammlung in ihren Mauern sehen wird.*                                             | **Positiv / hoffnungsvoll**       | Zukunftsgerichtet, mit stolzem Unterton                                           |
| *Alle politischen Parteien Deutschlands verknüpfen mit dem Namen Erfurt besondere Erinnerungen an ihre eigene Geschichte.* | **Reflexiv / positiv konnotiert** | Appell an nationale Erinnerungskultur, identitätsstiftend
## Textklassifikation
Genre, Thema, Autorenschaft

### Stilometrie/Autorschaftsanalyse
Auch Stilometrie – die Analyse individueller Schreibstile anhand sprachlicher Merkmale (z. B. Wortwahl, Satzstruktur) – ist ein Anwendungsfeld von LLMs. Ein Ziel kann hier beispielsweise sein, Autorenschaft zu erkennen oder mehrere Autoren in einem Text abzugrenzen.

Für den kurzen Abschnitt aus obigem Beispiel trifft *ChatGPT* folgende Stilometrie-Analyse.

| Merkmal   | Beschreibung                               |
| --------- | ------------------------------------------ |
| Satzlänge | Mittel bis lang, oft komplex               |
| Wortwahl  | Formal, historisch, politisch konnotiert   |
| Stilistik | Nominalstil, geringe Emotionalisierung     |
| Tempus    | Präsens / Futurisch mit prognostischem Ton |
| Funktion  | Informativ und legitimierend (politisch)   |

Auch bei der Stilometrie ist die Methode besonders sinnvoll bei großen Textsammlungen – hier lassen sich die Ähnlichkeiten zwischen verschiedenen Texten messen und Stile quantisieren.

# Anwendung in der Digital History
## Herausforderungen bei historischen Texten
## Werkzeuge und Tools