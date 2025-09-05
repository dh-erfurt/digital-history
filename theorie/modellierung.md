# Modellierung
 
Die Arbeit an und mit Daten ist zentral für die Digital Humanities: Ob bei der Annotation eines Textes, beim Aufbau einer Datenbank zu historischen Personen oder bei der Visualisierung politischer Netzwerke – am Anfang steht die Frage nach der *Datenmodellierung*. Welche Form und Struktur sollten die Daten haben?

*Datenmodelle* bezeichnen formale Modelle, die zur Repräsentation von Objekten dienen. Sie
- ermöglichen komplexe maschinelle Operationen auf den Daten
- dienen als Grundlage der Kommunikation über die Daten
- sichern eine höhere Qualität der Daten, indem sie Bedingungen formulieren, denen Daten bei der Eingabe entsprechen müssen
- ermöglichen den Austausch oder das Zusammenführen von Daten (→ Nachhaltigkeit)

Diese Definition und eine tiefergehende Einführung finden sich bei {cite:p}`jannidis_digital_2017`. Dieses Kapitel erläutert grundlegende Begriffe und Konzepte.

## Einführung
Datenmodellierung bezeichnet einen Prozess, bei dem eine visuelle Darstellung der Daten und ihrer Beziehungen erstellt wird. Das Ergebnis ist ein formales Modell, das ein oder mehrere Objekte repräsentiert (= **Datenmodell**). Das Datenmodell wiederum ist eine Blaupause dafür, wie Daten strukturiert, gespeichert und abgerufen werden, um Konsistenz und Klarheit im Datenmanagement zu gewährleisten. Durch die Datenmodellierung wird ihre Speicherung, beispielsweise in einer Datenbank, vorbereitet.

## Entity-Relationship-Modell (ERM)
Das *Entity-Relationship-Modell* ist eine Art des Datenmodells, das von Peter Chen entwickelt wurde {p:cite}`chen_entity-relationship_1976`. Es stellt dar, wie Daten miteinander in Beziehung stehen, und besteht aus folgenden Elementen:
- *Entity (Entität)*: beschreibt Objekt der realen Welt (z. B. "Person", "Brief"), nicht einzelne Instanzen (z. B. "Max Müller", "Brief vom 4. Mai")
- *Attribut*: beschreibt Entität näher
- *Relation (Beziehung)*: beschreibt, wie Entitäten zueinander in Verbindung stehen

```{figure} ../img/simples-erm.drawio.png
:alt: Beispiel simples ERM Briefe
:name: simples-erm
:align: left

Simples ERM, das den Prozess der Briefkorrespondenz modelliert
```
<br/>

{numref}`simples-erm` zeigt ein simples ERM, in dem der Prozess des Verschickens und Empfangens von Briefkorrespondenz modelliert ist. Jede Entität hat genau einen **Primärschlüssel**, der sie eindeutig identifiziert (`PersonID`, `BriefID`).

In einem komplexeren Szenario kann es auch **Fremdschlüssel** geben, welche auf den Primärschlüssel einer anderen Entität verweisen. **Kardinalitäten** beschreiben, wie viele Entitäten eines Typs an einer Beziehung beteiligt sein können: *z. B.: Jeder Brief wird von einer Person gesendet, eine Person kann n Briefe senden.*

Für ein Szenario, angelehnt an die [Nürnberger Briefbücher](http://lme70.informatik.uni-erlangen.de:8060/exist/apps/nuernberger-briefbuecher/index.html), in dem Briefe von Personen und Städten versendet und empfangen werden können, sie aber von einem Stadtschreiber verfasst werden, reicht obiges ERM nicht mehr aus. 

```{figure} ../img/erm-briefbuecher.drawio.png
:alt: Beispiel-ERM Briefbücher-Korrespondenz
:name: nbb-erm
:align: left

Komplexeres ERM, das den Prozess der Briefkorrespondenz in den Nürnberger Briefbüchern modelliert
```
<br/>

{numref}`nbb-erm` zeigt ein komplexeres ERM, in dem auch diese Informationen erfasst werden können. Hier kommen nicht nur Fremdschlüssel zum Einsatz, sondern auch Unter- bzw. Superklassen (Vererbung), verdeutlicht durch die "Ist"-Beziehung. 

ERMs bieten darüber hinaus auch weitere komplexere Möglichkeiten, Daten und Informationen zu modellieren.


---
# Literatur und weiterführende Informationen
- Andreas Heuer, Gunter Saake, Kai-Uwe Satler, Holger Meyer, Hannes Grunert. Datenbanken. Kompaktkurs. mitp 2020.
- Wolfgang Gerken. Datenbanksysteme für Dummies. Wiley Weinheim 2018.
- Peter Bühler, Patrick Schlaich, Dominik Sinner. Datenmanagement. Daten – Datenbanken – Datensicherheit. Springer Vieweg 2019.
- [Erklärvideo zu ERM](https://studyflix.de/informatik/er-modell-7476?topic_id=16) 
- Ciula A, Eide Ø, Marras C, Sahle P. Modelling between digital and humanities: thinking in practice. Open Book Publishers 2023. https://www.openbookpublishers.com/books/10.11647/OBP.0369
- Ciula A, Eide Ø, Marras C, Sahle P. Models and modelling between digital and humanities. remarks from a multidisciplinary perspective. Historical Social Research/Historische Sozialforschung. 2018 Jan 1;43(4):343-61. https://www.gesis.org/hsr/volltext-archiv/2018/suppl-31-models-and-modelling-between-digital-humanities 


## Zitierte Literatur

```{bibliography}
:filter: docname in docnames
```

