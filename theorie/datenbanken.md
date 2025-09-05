# Datenbanken
 
Datenbanken sind strukturierte Sammlungen von Informationen, deren Organisation es erlaubt, Inhalte effizient zu speichern, zu durchsuchen, abzurufen und zu analysieren. Im Wesentlichen machen Datenbanken Informationen sowie die Beziehungen zwischen diesen Informationen sichtbar und nutzbar. 

Für geisteswissenschaftliche Forschung und speziell im Kontext der Digital Humanities sind Datenbanken zentral, da hier oft mit großen Mengen strukturierter Informationen gearbeitet wird (z. B. Texte, Metadaten, Netzwerke). Sie sind ein elementares Werkzeug, das Forschung unterstützt und weitere Zugänge schafft.

Dieses Kapitel widmet sich einführend zentralen Konzepten im Bereich *Datenbanken*.

## Einführung

*"Eine Datenbank hat die Aufgabe, große Datenmengen in einer strukturierten Form widerspruchsfrei zu speichern und vor Verlust und unbefugtem Zugriff zu schützen."* {cite}`buhler_webtechnologien_2018`

Es gibt verschiedene Arten von Datenbanksystemen.
**Relationale Datenbanken** speichern die Daten in Tabellen mit verschiedenen Beziehungen zwischeneinander und sind seit Jahrzehnten weit verbreitet. Sie bestehen aus folgenden Elementen:
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

## Weitere Datenbankkonzepte
**Graphdatenbanken** verwenden Graphen (bestehend aus Knoten und Kanten) zur Darstellung und Speicherung von Daten. Damit eignen sie sich besonders für die Abbildung komplexer Netzwerke, etwa sozialer Beziehungen oder intertextueller Bezüge – ein Ansatz, der in den Digital Humanities häufig eingesetzt wird. Ein verbreitetes System ist Neo4j, das sich z. B. für Netzwerkanalysen eignet.

**NoSQL-Datenbanken** umfassen verschiedene Systeme, die nicht dem klassischen relationalen Modell folgen und für besonders flexible oder skalierbare Anwendungen entwickelt wurden. Beispiele sind MongoDB, das häufig für die Speicherung unstrukturierter oder halbstrukturierter Daten (z. B. Texte, JSON-Dokumente) genutzt wird, sowie eXist-db, eine XML-basierte Datenbank, die speziell in den Geisteswissenschaften Verwendung findet, etwa zur Verwaltung und Edition digitaler Texte.


## Datenbanken in der Praxis
Will man nun in der Praxis eine Datenbank umsetzen, geht man nach folenden Schritten vor:
1. Auswahl eines passenden Datenbankkonzepts (relational, Graphdatenbank, ...)
2. Auswahl eines passenden Tools
    - Microsoft Access (bzw. LibreOffice Base), allerdings begrenzte Skalierbarkeit und Kompatiblität mit anderen Systemen 
    - MySQL / PostgreSQL
    - SQLite etc. 
3. Entwickeln eines Datenmodells (z. B. mithilfe von ERM)
4. Anlegen der Tabellen
5. Einpflegen der Daten
6. Abfragen und Auswertungen


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

## Literatur und weiterführende Informationen
- Andreas Heuer, Gunter Saake, Kai-Uwe Satler, Holger Meyer, Hannes Grunert. Datenbanken. Kompaktkurs. mitp 2020.
- Wolfgang Gerken. Datenbanksysteme für dummies. Wiley Weinheim. 2018.
- Peter Bühler, Patrick Schlaich, Dominik Sinner. Datenmanagement. Daten – Datenbanken – Datensicherheit. Springer Vieweg 2019.
- [SQL Tutorial](https://www.w3schools.com/sql/)
- Andreas Kuczera. Graphentechnologien in den digitalen Geisteswissenschaften. Modellierung – Import – Analyse. https://kuczera.github.io/Graphentechnologien/
- [Vortrag von Andreas Kuczera zum Thema "Graphs in the (Digital) Humanities"](https://neo4j.com/videos/graphs-in-the-digital-humanities-andreas-kuczera-akademie-der-wissenschaften/)

## Zitierte Literatur
```{bibliography}
:filter: docname in docnames
```