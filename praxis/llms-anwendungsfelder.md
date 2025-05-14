# Weitere Anwendungsfelder für LLMs

LLMs wie ChatGPT können nicht nur beim Verfassen von Texten unterstützen, sondern bieten darüber hinaus vielfältige Einsatzmöglichkeiten, auch besonders im Bereich der Geschichtswissenschaften.

–	Orte, Personen, Zeitangaben in einem Text identifizieren (NER)
–	Netzwerkanalyse
–	Topic Modelling
–	Quellenarbeit mit KI

## Arbeit mit historischen Quellen
Bei der Transkription von historischen Quellen kommt oft *Optical Character Recognition (OCR)* zum Einsatz. *OCR*-Tools werden oft mithilfe von KI verbessert. LLMs können auch hilfreich dabei sein, den Output von OCR zu bereinigen, indem sie Fehler erkennen und korrigieren.

## Verstehen und Analysieren von Text
Ein zentrales Anwendungsfeld von LLMs ist nicht nur das Verfassen, sondern auch das Verstehen und die Analyse von Texten. Für die Geschichtswissenschaften hilfreich können u.a. *Named Entity Recognition*, *Sentiment Analysis*, *Topic Modelling* und *Stilometrie*-Analysen sein. 

### Named Entity Recognition
![](ner.png)

*Named Entity Recognition (NER)* bezeichnet die Aufgabe, Entitäten in Texten zu erkennen und zu klassifizieren (z.B. Personen, Orte, Organisationen, Zeitangaben etc.) {cite:p}`ner`. Gerade im Kontext der Geschichtswissenschaften ist es hilfreich zu wissen, wer in historischen Quellen erwähnt wird und welche Orte und eine Institutionen dabei eine Rolle spielen. *NER* ist also eine wichtige Basis für weitergehende Analysen, z.B. für die Untersuchung historischer Kommunikationsnetze, geografischer Bezüge oder institutioneller Strukturen.

LLMs, deren Hauptaufgabe es ist, ... 
- Ambiguität zwischen Ort und Organisation (z.B. "Universität Erfurt")


### Sentiment Analysis
- Einschätzen der Stimmung/emotionalen Haltung eines Texts
- Kontext Geschichtswissenschaften: z.B. Bewertung politischer Reden, zeitungsartikel, Briefe, Auswertung öffentlicher Meinung
- Beispiel: https://www.deutsche-digitale-bibliothek.de/newspaper/item/ZBJ3S5LCHJIKSQHDTL4URASFOIV4RYXY?issuepage=8
Erfurt, der Ort der Nationalversammtung!
Nach Weimar, Leipzig und Nürnberg ist nunmehr von den Volksbeauftragten als Ort der Nationalversammlung Erfurt in Aussicht genommen. Es ist auch Aussicht vorhanden, dass die uralte Metropole Thüringens, das als Binnen- und Industriestadt gleich geschätzte Erfurt, die kommende deutsche Nationalversammlung in ihren Mauern sehen wird.
Alle politischen Parteien Deutschlands verknüpfen mit dem Namen Erfurt besondere Erinnerungen an ihre eigene Geschichte.

| Satz                                                                                                                       | Tonlage / Sentiment               | Hinweise                                                                          |
| -------------------------------------------------------------------------------------------------------------------------- | --------------------------------- | --------------------------------------------------------------------------------- |
| *Erfurt, der Ort der Nationalversammlung!*                                                                                 | **Positiv / Feierlich**           | Ausrufezeichen, Betonung auf Bedeutung und Ehre                                   |
| *\[...] ist nunmehr von den Volksbeauftragten als Ort der Nationalversammlung Erfurt in Aussicht genommen.*                | **Neutral bis leicht positiv**    | Sachliche Mitteilung, aber durch die Auswahl Erfurts mitschwingende Wertschätzung |
| *\[...] die uralte Metropole Thüringens, das als Binnen- und Industriestadt gleich geschätzte Erfurt \[...]*               | **Positiv / wertschätzend**       | Lobende Adjektive: "uralte Metropole", "geschätzt"                                |
| *\[...] die kommende deutsche Nationalversammlung in ihren Mauern sehen wird.*                                             | **Positiv / hoffnungsvoll**       | Zukunftsgerichtet, mit stolzem Unterton                                           |
| *Alle politischen Parteien Deutschlands verknüpfen mit dem Namen Erfurt besondere Erinnerungen an ihre eigene Geschichte.* | **Reflexiv / positiv konnotiert** | Appell an nationale Erinnerungskultur, identitätsstiftend                         |


### Topic Modelling 
- *Topic Modelling*: Welche Themen kommen in einer großen Textsammlung vor?
- Kontext Geschichtswissenschaft: Welche Themen dominieren z.B. in Zeitungen einer Epoche? 
- Beispiel (für kurzen Textausschnitt):
    - Identifizierte Themen (Topics):
         - Ort der Nationalversammlung
         Begriffe: „Nationalversammlung“, „Volksbeauftragte“, „in Aussicht genommen“, „kommende“
         Bedeutung: Der Text berichtet, dass Erfurt als möglicher Veranstaltungsort für eine deutsche Nationalversammlung diskutiert wird.

    - Symbolische Bedeutung Erfurts für die Parteien
        - Begriffe: „besondere Erinnerungen“, „eigene Geschichte“, „alle politischen Parteien“
        - Bedeutung: Erfurt wird als Ort mit historischer Bedeutung für verschiedene politische Bewegungen dargestellt.

    - Charakteristik der Stadt Erfurt
        - Begriffe: „uralte Metropole Thüringens“, „Binnenstadt“, „Industriestadt“
        - Bedeutung: Die Stadt wird geographisch und wirtschaftlich eingeordnet und gewürdigt.
- oder Beispiel von hier: https://journalofdigitalhumanities.org/2-1/topic-modeling-and-digital-humanities-by-david-m-blei/ ?

### Stilometrie/Autorschaftsanalyse
- Analyse individueller Schreibstile anhand sprachlicher Merkmale (z.B. Wortwahl, Satzstruktur)
- Ziel: Erkennung des Autors oder Abgrenzung mehrerer Autoren in einem Text
- Kontext Geschichtswissenschaft: Zuschreibung an bestimmte Autoren, Analyse kollektiver Autorenschaft
- Beispiel: 

| Merkmal   | Beschreibung                               |
| --------- | ------------------------------------------ |
| Satzlänge | Mittel bis lang, oft komplex               |
| Wortwahl  | Formal, historisch, politisch konnotiert   |
| Stilistik | Nominalstil, geringe Emotionalisierung     |
| Tempus    | Präsens / Futurisch mit prognostischem Ton |
| Funktion  | Informativ und legitimierend (politisch)   |


# Fazit 
evtl hier was zu Netzwerkanalyse - Karten - Visualisierung


# Quellen und weiterführende Links
Die Chancen und Herausforderungen von LLMs in der Geschichtswissenschaft schlüsselt auch [dieser](https://dhdhi.hypotheses.org/9197) Blogbeitrag auf. 

Darüber hinaus gibt es viele hilfreiche Online-Ressourcen, z.B. 
- [Überblick/Tutorial zu Named Entity Recognition mit Python](https://www.geeksforgeeks.org/named-entity-recognition/)

## Zitierte Literatur
```{bibliography}
:filter: docname in docnames
```
