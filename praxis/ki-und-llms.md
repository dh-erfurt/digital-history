# Grundlagen: KI und LLMs

Künstliche Intelligenz ist nicht nur ein bedeutendes und interdisziplinäres Teilgebiet der Informatik, sondern spätestens seit dem Aufkommen von KI-Chatbots wie *ChatGPT* auch eines der meistdiskutierten gesellschaftlichen Themen. Um informiert und präzise über Chancen und Risiken sprechen zu können, ist es sinnvoll, zunächst zentrale Begrifflichkeiten zu klären und ein grundlegendes Verständnis der Funktionsweise von KI-Technologien zu entwickeln. Beides wird Gegenstand dieses Kapitels sein. 


## Begriffsabgrenzung
```{figure} ../img/ml-verortung.drawio.png
:alt: Begrifssabgrenzung KI - Machine Learning - Deep Learning - LLMs
:name: begriffsabgrenzung-ki
:width: 600px
:align: left

KI-Chatbots wie *ChatGPT*, also *Large Language Models (LLMs)*, machen nur einen kleinen Teil der Technologien aus, die unter *Künstliche Intelligenz* fallen.
```
<br/>

Wenn von KI-Chatbots wie *ChatGPT* o. Ä. gesprochen wird, ist die Rede von *LLMs (Large Language Models)*. Diese machen aber nur einen kleinen Teil der Technologien und Konzepte aus, die unter den Schirm der *künstlichen Intelligenz* fallen, wie {numref}`begriffsabgrenzung-ki` zeigt.

*Künstliche Intelligenz* bezeichnet zunächst einmal nur die Theorie, dass menschliche Intelligenz von einer Maschine gezeigt wird. 

*Machine Learning* (ML), eines der größten und schnellst wachsenden Forschungsgebiete der Informatik, ist ein Teilbereich von KI. ML-Algorithmen verwenden große Datensätze, um Muster zu erkennen und zu lernen, autonome Entscheidungen und Vorhersagen zu treffen {cite:p}`sarkar2018practical`. Neben ML stehen weitere Forschungsansätze, die unter *Künstliche Intelligenz* fallen, z. B. formale Logik, die aber heute seltener diskutiert werden. 

*Deep Learning* (DL) ist wiederum ein Teilbereich von *Machine Learning*, bei dem künstliche neuronale Netze mit vielen Schichten zum Einsatz kommen (die Funktionsweise wird im Folgenden noch näher erläutert). DL ist sehr leistungsfähig und bildet die Grundlage vieler aktueller KI-Anwendungen, erfordert aber auch erhebliche Mengen an Daten- und Rechenressourcen {cite:p}`janiesch_machine_2021`.

Ein besonders sichtbares Anwendungsfeld von DL ist die Verarbeitung natürlicher Sprache, wobei *LLMs* verwendet werden - tiefe neuronale Netze, die mit sehr großen Textmengen trainiert wurden und deren Ziel es ist, Sprache zu verstehen und zu erzeugen {cite:p}`llms`.

## Wie funktioniert Deep Learning?

Was steckt nun eigentlich hinter KI-Anwendungen wie *ChatGPT*? Im Grunde zunächst: sehr viel Mathematik.

```{figure} ../img/ml-beispiel-grundprinzip.drawio.png
:alt: Grundprinzip DL (Input - Model - Output)
:name: grundprinzip
:align: left

Grundprinzip Deep Learning: Input - Model - Output.
```
<br/>

{numref}`grundprinzip` veranschaulicht das Grundprinzip von Deep-Learning-Anwendungen. Ein *DL-Modell* bekommt einen Input, z.B. ein Bild eines Tiers, übergeben und trifft davon ausgehend eine Voraussage (*Prediction*), ob es sich bei diesem Tier um einen Vogel handelt – gibt also einen Output aus.

### Was ist ein Modell?

Zentral für diese Funktionsweise ist das Modell, das den Input verarbeitet und durch Training darauf optimiert wurde, möglichst akkurate *Predictions* basierend auf dem Input zu treffen. Ein Modell ist zunächst einmal ein mathematisches System. Künstliche neuronale Netze sind eine Art von Modellen, die bei *Deep Learning*-Anwendungen verwendet werden. 

```{figure} ../img/ml-beispiel-model-skizze.drawio.png
:alt: Skizze Modell
:name: skizze-modell
:align: left

Skizze Modell (neuronales Netzwerk)
```
<br/>

{numref}`skizze-modell` illustriert ein solches Netzwerk aus Knotenpunkten, die miteinander verbunden sind. Diese Knoten bekommen Informationen von anderen Knoten, rechnen etwas mit ihnen und geben im Anschluss das Ergebnis weiter. Diese Funktionsweise soll im Folgenden an Ausschnitt aus obigem Modell veranschaulicht werden.

```{figure} ../img/ml-beispiel-1.drawio.png
:alt: Ausschnitt ML-Modell
:name: ml-beispiel-ausschnitt
:align: left

Ausschnitt ML-Modell
```
<br/>

{numref}`ml-beispiel-ausschnitt` illustriert diesen Ausschnitt. Die Verbindungen zwischen den Knoten haben Gewichte, die bemessen, wie wichtig die jeweils weitergegebene Information für den Folgeknoten ist.

```{figure} ../img/ml-beispiel-2.drawio.png
:alt: Input
:name: ml-beispiel-input
:align: left

Input
```
<br/>

In {numref}`ml-beispiel-input` bekommt der Modell-Ausschnitt nun einen numerischen Input übergeben. Das könnte z. B. ein Pixelfarbwert sein, wenn es um Bilderkennung geht. 

```{figure} ../img/ml-beispiel-3.drawio.png
:alt: Erster Knoten wird berechnet
:name: ml-beispiel-1
:align: left

Erster Knoten wird berechnet
```
<br/>

Die Berechnung des ersten Knotens erfolgt als Summe der eingehenden Knotenverbindungen, entsprechend ihren Gewichtungen, wie in {numref}`ml-beispiel-1` gezeigt.

```{figure} ../img/ml-beispiel-4.drawio.png
:alt: Zweiter Knoten wird berechnet
:name: ml-beispiel-2
:align: left

Zweiter Knoten wird berechnet
```
<br/>

Ebenso wird der zweite Knotenwert berechnet, s. {numref}`ml-beispiel-2`.

```{figure} ../img/ml-beispiel-5.drawio.png
:alt: Dritter Knoten wird berechnet
:name: ml-beispiel-3
:align: left

Dritter Knoten wird berechnet
```
<br/>

Beim dritten Knotenwert gibt es zwei eingehende Verbindungen, die gewichtet summiert werden, wie in {numref}`ml-beispiel-3` gezeigt wird.

```{figure} ../img/ml-beispiel-6.drawio.png
:alt: Vierter Knoten wird berechnet
:name: ml-beispiel-4
:align: left

Vierter Knoten wird berechnet
```
<br/>

Analog erfolgt die Berechnung des vierten Knotens in {numref}`ml-beispiel-4`.

```{figure} ../img/ml-beispiel-7.drawio.png
:alt: Output
:name: ml-beispiel-output
:align: left

Output
```
<br/>

Auch der Endknoten wird in {numref}`ml-beispiel-output` genauso berechnet. Dieser Wert könnte jetzt z. B. eine Aussage darüber machen, mit welcher Wahrscheinlichkeit es sich bei dem Bild um einen Vogel handelt – in diesem Beispiel mit 89.1 %. 

Modelle erhalten also einen Input, stellen einige Berechnungen damit an und geben einen entsprechenden Output aus. 

### Wie funktioniert das Training des Modells?

Was macht dieses Prinzip nun *intelligent*, d. h., wie kann sich das Modell selbst verbessern?

```{figure} ../img/ml-beispiel-training.drawio.png
:alt: Trainingsmechanismus
:name: trainingsmechanismus
:align: left

Visualisierung des Trainingsmechanismus
```
<br/>

Im Trainingsprozess des Modells macht es immer wieder *Predictions*, basierend auf verschiedenen Input-Daten. Diese *Prediction* wird dann überprüft und, falls sie falsch war, werden die Gewichte des Modells angepasst. Das erfolgt durch den Algorithmus selbst – an dieser Stelle *lernt die Maschine*. Dieser Prozess wird in {numref}`trainingsmechanismus` dargestellt.

Um das Modell so zu trainieren, dass es möglichst akkurate *Predictions* trifft, braucht man eine große Menge an Trainingsdaten, bei denen die „Lösung“ (d. h., ist es ein Vogel?) schon bekannt ist. Mit genügend Wiederholungen des Trainingsvorgangs kann sich das Modell dann für seine Aufgabe optimieren.

Das macht deutlich, dass die Auswahl der Trainingsdaten entscheidend ist – sie sollten möglichst heterogen und vielfältig sein, damit das Modell auf unbekannten Daten gut *generalisieren* kann.

### Wie funktionieren LLMs?
Wie oben beschrieben sind LLMs *Large Language Models*, also sehr große neuronale Netze, die mit erheblichen Mengen an Daten darauf trainiert werden, mit Sprache umzugehen und Sprache zu erzeugen. Insbesondere lernen LLMs:
- wie Wörter typischerweise aufeinander folgen
- welche Sätze Sinn ergeben
- wie Fragen und Antworten zusammenhängen

Das LLM generiert die Ausgabe Textbaustein für Textbaustein, d. h. für jedes Wort wird vorhergesagt, welches darauffolgende Wort am wahrscheinlichsten ist.


# Fazit

KI ist abhängig von seiner Datenbasis und kann Biases seiner Trainingsdaten reproduzieren und verstärken.

KI-Modelle sind statistische Systeme → Die *wahrscheinlichste* Antwort wird zurückgegeben.

KI basiert oft auf sehr großen Modellen und benötigt entsprechende Ressourcen (Rechenleistung, Energie, Datenmengen).


# Quellen und weiterführende Links

Es gibt viele gute Online-Resourcen, die KI definieren und seine Funktionsweise anschaulich erläutern, z. B. kurze Artikel (z. B. [hier](https://youtu.be/LPZh9BOjkQs?si=3tipF644tRCWeLJc)), Erklärvideos (z. B. [hier](https://youtu.be/LPZh9BOjkQs?si=3tipF644tRCWeLJc)) oder Online-Kurse (z. B. [KI-Campus](https://ki-campus.org/courses/kifueralle-hhu)).

## Zitierte Literatur
```{bibliography}
:filter: docname in docnames
```