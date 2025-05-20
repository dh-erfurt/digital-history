# Fehler und falsche Informationen in KI-Chatbots

Es ist sehr wichtig, sich bewusst zu machen, dass KI-Chatbots trotz ihrer vielfältigen Einsatzmöglichkeiten und Potenziale nicht fehlerfrei sind.
Zu den typischen Fehler- und Risikoquellen zählen u. a. 

- *Halluzinationen*: KI-Chatbots können auf überzeugende Weise faktisch falsche Informationen erzeugen. Sie haben weder Weltwissen noch ein Bewusstsein oder Meinungen, auch wenn ihre Antworten diesen Eindruck erwecken können.

- fehlende Kontexttiefe: KI-Chatbots *verstehen* Sprache nicht im menschlichen Sinne, sondern berechnen lediglich aufgrund von statistischen Modellen die nächste Wortfolge.

- *Bias*: Da KI-Chatbots auf großen Mengen bestehender Daten trainiert wurden, können sie gesellschaftliche Vorurteile, Stereotype, Verzerrungen und Diskriminierungen reproduzieren.

- Instabilität: Selbst bei identischen Prompts können die Antworten von KI-Chatbots variieren, da sie auf statistischen Modellen basieren.


Dazu einige Beispiele:

```{figure} ../img/chatgpt-fehler.drawio.png
:alt: Beispiel Konversation mit KI-Chatbot
:name: jakob-viehausen
:width: 600px
:align: left

Bei der Frage nach einem erfundenen Bürger Erfurts antwortet der KI-Chatbot überzeugend, aber faktisch falsch.
```
<br/>

In {numref}`jakob-viehausen` antwortet *ChatGPT* bei der Frage nach einem erfundenen Erfurter Bürger mit halluzinierten Informationen, die in ihrer Fülle und Darstellung überzeugend echt wirken.

```{figure} ../img/europa.png
:alt: Generierte Karte der Länder Europas
:name: europa
:width: 500px
:align: left

Soll eine Karte mit den Ländern Europas erzeugt werden, werden die Grenzen der KI schnell deutlich.
```
<br/>

```{figure} ../img/capitals.png
:alt: Generierte Karte der Hauptstädte Europas
:name: capitals
:width: 500px
:align: left

Beim Generieren einer Karte mit europäischen Hauptstädten fallen noch stärkere Halluzinationen auf.
```
<br/>

Gerade auch beim Generieren von Bildmaterial sind KI-Anwendungen fehlerhaft, wie anhand der erzeugten Karten der Länder Europas ({numref}`europa`) und ihrer Hauptstädte ({numref}`capitals`) schnell klar wird.


Halluzinationen in Text- und Bildausgaben wie in obigen Beispielen führen deutlich vor Augen, dass KI-Chatbots keine absolute *Wahrheit* liefern, sondern lediglich plausibel klingende Inhalte erzeugen. Für den wissenschaftlichen wie gesellschaftlichen Einsatz bedeutet das: KI-Chatbots können ein mächtiges Werkzeug sein, ihre Ausgaben müssen aber stets kritisch überprüft und kontextualisiert werden.
