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

Wenn von KI-Chatbots wie *ChatGPT* o.ä. gesprochen wird, ist die Rede von *LLMs (Large Language Models)*. Diese machen aber nur einen kleinen Teil der Technologien und Konzepte aus, die unter den Schirm der *künstlichen Intelligenz* fallen, wie {numref}`begriffsabgrenzung-ki` zeigt.

*Künstliche Intelligenz* bezeichnet zunächst einmal nur die Theorie, dass menschliche Intelligenz von einer Maschine gezeigt wird. 

*Machine Learning* (ML), eines der größten und schnellstwachsenden Forschungsgebiete der Informatik, ist ein Teilbereich von KI. ML-Algorithmen verwenden große Datensätze, um Muster zu erkennen und zu lernen, autonome Entscheidungen und Vorhersagen zu treffen {cite:p}`sarkar2018practical`. Neben ML stehen weitere Forschungsansätze, die unter *Künstliche Intelligenz* fallen, z.B. formale Logik, die aber heute seltener diskutiert werden. 

*Deep Learning* (DL) ist wiederum ein Teilbereich von *Machine Learning*, bei dem künstliche neuronale Netze mit vielen Schichten zum Einsatz kommen (die Funktionsweise wird im Folgenden noch näher erläutert werden). DL ist sehr leistungsfähig und bildet die Grundlage vieler aktueller KI-Anwendungen, erfordert aber auch erhebliche Mengen an Daten- und Rechenressourcen {cite:p}`janiesch_machine_2021`.

Ein besonders sichtbares Anwendungsfeld von DL ist die Verarbeitung natürlicher Sprache, wobei *LLMs* verwendet werden - tiefe neuronale Netze, die mit sehr großen Textmengen trainiert wurden und deren Ziel es ist, Sprache zu verstehen und zu erzeugen {cite:p}`llms`.

## Wie funktioniert Deep Learning?

Was steckt nun eigentlich hinter KI-Anwendungen wie *ChatGPT*? Im Grunde erstmal: sehr viel Mathematik.

```{figure} ../img/ml-beispiel-grundprinzip.drawio.png
:alt: Grundprinzip DL: Input - Model - Output
:name: grundprinzip
:width: 600px
:align: left

Grundprinzip Deep Learning: Input - Model - Output.
```


Die Graphik {numref}`grundprinzip` veranschaulicht das Grundprinzip von Deep-Learning-Anwendungen. Ein *DL-Modell* bekommt einen Input, z.B. ein Bild eines Tiers, übergeben und trifft davon ausgehend eine Voraussage, ob es sich bei diesem Tier um einen Vogel handelt - gibt also einen Output aus.

### Was ist ein Modell?

```{figure} ../img/ml-beispiel-model-skizze.drawio.png
:alt: Skizze Modell
:width: 600px
:align: left

Skizze Modell (neuronales Netzwerk)
```

```{figure} ../img/ml-beispiel-1.drawio.png
:alt: Ausschnitt ML-Modell
:width: 600px
:align: left

Ausschnitt ML-Modell
```

```{figure} ../img/ml-beispiel-2.drawio.png
:alt: Input
:width: 600px
:align: left

Input
```

```{figure} ../img/ml-beispiel-3.drawio.png
:alt: Erster Knoten wird berechnet
:width: 600px
:align: left

Erster Knoten wird berechnet
```

```{figure} ../img/ml-beispiel-4.drawio.png
:alt: Zweiter Knoten wird berechnet
:width: 600px
:align: left

Zweiter Knoten wird berechnet
```

```{figure} ../img/ml-beispiel-5.drawio.png
:alt: Dritter Knoten wird berechnet
:width: 600px
:align: left

Dritter Knoten wird berechnet
```

```{figure} ../img/ml-beispiel-6.drawio.png
:alt: Vierter Knoten wird berechnet
:width: 600px
:align: left

Vierter Knoten wird berechnet
```

```{figure} ../img/ml-beispiel-7.drawio.png
:alt: Output
:width: 600px
:align: left

Output
```

### Wie funktioniert das Training des Modells?

```{figure} ../img/ml-beispiel-training.drawio.png
:alt: Trainingsmechanismus
:width: 600px
:align: left

Visualisierung des Trainingsmechanismus
```

### LLMs


# Was sollten wir daraus mitnehmen?

```{bibliography}
:filter: docname in docnames
```