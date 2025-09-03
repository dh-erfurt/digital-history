# Datenbanken
 
Datenbanken sind strukturierte Sammlungen von Informationen, deren Organisation es erlaubt, Inhalte effizient zu speichern, zu durchsuchen, abzurufen und zu analysieren. Im Wesentlichen machen Datenbanken Informationen sowie die Beziehungen zwischen diesen Informationen sichtbar und nutzbar. 

Für geisteswissenschaftliche Forschung und speziell im Kontext der Digital Humanities sind Datenbanken zentral, da hier oft mit großen Mengen strukturierter Informationen gearbeitet wird (z. B. Texte, Metadaten, Netzwerke). Sie sind ein elementares Werkzeug, das Forschung unterstützt und weitere Zugänge schafft.

Dieses Kapitel widmet sich einführend zentralen Konzepten im Bereich *Datenbanken*.

## Einführung

*"Eine Datenbank hat die Aufgabe, große Datenmengen in einer strukturierten Form widerspruchsfrei zu speichern und vor Verlust und unbefugtem Zugriff zu schützen."* {cite}`buhler_webtechnologien_2018`


**Relationale Datenbanken**, die Daten in Tabellen mit verschiedenen Beziehungen zwischeneinander speichern, stehen hierbei anderen Datenbankkonzepten gegenüber (z. B. Graphdatenbanken). Relationale Datenbanken sind jedoch seit Jahrzehnten Standard und bestehen aus folgenden Elementen:
- **Tabelle**: strukturierte Darstellung großer Datenmengen, lassen sich sortieren, filtern und miteinander in Verbindung setzen
- **Datensatz / Tupel**: zusammengehörende Daten (= Reihe in Tabelle), besteht aus mehreren **Datenfelder** und muss über einen **Schlüssel** eindeutig identifizierbar sein
- **Attribute**: gleichartige Datenfelder (= Spalten)

Diese Grundbegriffe werden in {numref}`grundbegriffe-rel-db` veranschaulicht. 

```{figure} ../img/grundbegriffe-db.png
:alt: Grundbegriffe Datenbank
:name: grundbegriffe-rel-db
:align: left

Veranschaulichung der Bestandteile einer relationalen Datenbank, nach {cite}`buhler_datenmanagement_2019`
```
<br/>

## SQL als Datenbankabfragesprache

**SQL (Structured Query Language)** ist eine Abfragesprache für programmunabhängigen Zugriff auf Datenbanken. Sie ermöglicht u. a. das
- Erstellen von Datenbanken und Tabellen
- Eingeben, Ändern und Löschen von Datensätzen
- Abfragen (= Query) von Daten nach gewünschten Kriterien

In folgendem einfachen Beispiel wählt Spalten (`SELECT`) in einer bestimmten Tabellen (`FROM`) aus und wendet Bedingungen / Filter (`WHERE`) auf die Daten an.
```sql
SELECT BriefID, Datum 
FROM Briefe 
WHERE VerfasserID = 1;
```

Mit SQL sind aber auch weitaus komplexere Abfragen möglich.

## Datenbanken in der Praxis
Will man nun in der Praxis eine Datenbank umsetzen, geht man nach folenden Schritten vor:
1. Auswahl eines passenden Tools
    - Microsoft Access (bzw. LibreOffice Base)
    - MySQL / PostgreSQL
    - SQLite etc. 
2. Entwickeln eines Datenmodells (z. B. mithilfe von ERM)
3. Anlegen der Tabellen
4. Einpflegen der Daten
5. Abfragen und Auswertungen


### Wann und wo werden Datenbanken eingesetzt?

Datenbanken sind zentrale Bausteine moderner Informationssysteme und kommen in nahezu allen Bereichen zum Einsatz.
| Bereich             | Beispielhafte Anwendung                                             |
| ------------------- | ------------------------------------------------------------------- |
| Medizin             | Patientendaten, Krankheitsverläufe, Medikamente                     |
| Verwaltung / Staat  | Melderegister, Steuerdaten, Wahlregister                            |
| Bildung             | Notenverwaltung, Kursbelegung, Lernmanagementsysteme (z. B. Moodle) |     |
| Soziale Netzwerke   | Nutzerprofile, Beiträge, Beziehungen                                |
| Apps / Smartphones  | Chatverläufe, Kontaktdaten, Kalendereinträge                        |

In der Digital History finden sich insbesondere folgende Einsatzgebiete:

Bereich                               | Beispielhafte Anwendung                                                                   |
| ------------------------------------- | ----------------------------------------------------------------------------------------- |
| **Quelleneditionen**                  | Speicherung von digitalisierten Briefen, Urkunden, Tagebüchern, inkl. Metadaten           |
| **Personendatenbanken**               | Register historischer Personen (z. B. Gelehrtennetzwerke, Biographien)                    |
| **Orts- und Kartenbezug (GIS)**       | Verknüpfung historischer Orte mit Karten oder Koordinaten (z. B. mittelalterliche Städte) |              |
| **Textanalyse / Korpusdatenbanken**   | Volltexte historischer Dokumente zur Analyse (Stil, Begriffe, Entwicklung)                |
| **Projektdokumentation**              | Speicherung von Projekt-Metadaten, Provenienzen, Arbeitsschritten                         |
| **Museums- und Archivdatenbanken**    | Sammlungen, Digitalisate, Objektbeschreibungen, Inventare                                 |

---
# Literatur und weiterführende Informationen
- Andreas Heuer, Gunter Saake, Kai-Uwe Satler, Holger Meyer, Hannes Grunert. Datenbanken. Kompaktkurs. mitp 2020.
- Wolfgang Gerken. Datenbanksysteme für dummies. Wiley Weinheim. 2018.
- Peter Bühler, Patrick Schlaich, Dominik Sinner. Datenmanagement. Daten – Datenbanken – Datensicherheit. Springer Vieweg 2019.
- [SQL Tutorial](https://www.w3schools.com/sql/)

```{bibliography}
:filter: docname in docnames
```