# Prompting und Prompt Engineering 

## Was ist ein Prompt?

In der Informatik bedeutet ein *prompt* die Aufforderung an Nutzer*innen, eine Eingabe (input) zu tätigen. Bezogen auf KI-Chatbots ist ein prompt die Frage bzw. Aufgabe, die man stellt.


### Überlegen Sie:

- Wie stellen Sie eine Anfragean einen KI-Chatbot?
- Haben Sie Strategien, die Sie anwenden?
- Was funktioniert besonders gut? Was funktioniert nicht gut?
- Was macht aus Ihrer Sicht einen guten Prompt aus?


## Prompt Engineering

Prompt engineering beschreibt die Optimierung der Kommunikation mit einem KI-Tool (d. h. des  prompts), um eine optimale oder zumindest zufriedenstellende Ausgabe bzw. Antwort zu erhalten.
Verschiedene Faktoren beeinflussen die Qualität des outputs. Einige sehr wesentliche hängen mit denzugrundeliegenden Trainigsdaten, der Funktionsweise und den Anpassungen des Sprachmodells zusammen und können nicht von Nutzer*innen beeinflusst werden. Der Faktor, den Nutzer*innen beeinflussen können, ist allein die Anfrage.

Hierfür gibt es übergeordnete Strategien, die je nach eingesetztem Werkzeug – nachfolgend am Beispiel con ChatGPT – etwas unterschiedlich ausfallen.
Diese sind: context, role/persona, expectation.

---

### Crafting a great prompt

![width:650px](/SoSe2025/bilder/prompt-crafting.png)
Quelle: OpenAI, Introduction to Prompt Engineering, 8.3.2025, https://academy.openai.com/home/videos/introduction-to-prompt-engineering-2025-02-13

---

#### Prompt Engineering: weitere Strategien

- Delimiters (Trennungszeichen, z. B. Doppelpunkt oder Anführungszeichen)
- Schritt-für-Schritt-Anleitung
- Angabe von output-Format (Tabelle, bestimmtes Datenformat)
- Paramater kennen (verstehen, wie chatGPT mit input umgeht, welche Formate unterstützt werden etc., siehe Developer Dokumentation unter https://platform.openai.com/docs)

---

#### Beispiel: 

"Hilf mir, mich auf meine Klausur in Kommunikationswissenschaft vorzubereiten."

Was passiert, wenn man eine solche Anfrage stellt?

![width:400px;](/SoSe2025/bilder/chatGPT-output-clarify.png)

----

#### Verbesserungsmöglichkeit

"Hilf mir, mich auf meine Klausur in Kommunikationswissenschaft vorzubereiten."


"Ich bin Student*in an einer Universität und schreibe in 5 Tagen eine Klausur im Seminar "Theorien und Konzepte der Kommunikationswissenschaft". Kannst du mir 10 multiple-choice Fragen zu Theorien und Konzepten der der Kommunikationswissenschaft stellen?"

---

### Grund„regeln“

- Rolle definieren („Du bist ein Experte für…“)
- Zielgruppe nennen („Schüler:innen einer Grundschule“)
- Format festlegen (Liste, Gliederung, ausformulierter Text…)
- Kontext geben (Fachrichtung, Tonfall, Anwendungsziel)

Prompt engineering best practices for ChatGPT, OpenAI:
https://help.openai.com/en/articles/6654000-best-practices-for-prompt-engineering-with-the-openai-api


Introduction to ChatGPT Edu: Your AI-Powered Academic Companion
https://academy.openai.com/home/collections/chatgpt-on-campus-2025-03-20

---

### Auf was kann Prompt Engineering keinen Einfluss nehmen?

- Bias in den Trainingsdaten
- Begrenztes Wissen (Cutoff, kein Echtzeit-Wissen)
- Halluzinationen (Modell erfindet Inhalte, die wie Fakten aussehen)
- Grundlegende „Fähigkeit“ des Modells

---