# Digitale Editionen
 
Digitale Editionen sind ein zentraler Forschungsschwerpunkt in den Digital Humanities. Sie widmen sich der digitalen Erschließung, Edition und Veröffentlichung kultureller Güter (z. B. historischer Textsammlungen) und machen diese für Wissenschaft und Öffentlichkeit gleichermaßen zugänglich und nutzbar. Im Vergleich zu klassischen Druckeditionen bieten sie erweiterte Möglichkeiten, etwa die Integration multimedialer Inhalte oder die Einbindung interaktiver Funktionalität. 

Dieses Kapitel wird nach einer initialen Begriffsklärung grundlegende Konzepte darlegen und Möglichkeiten und Herausforderungen digitaler Editionspraxis diskutieren.

# Begriffsklärung
Digitale Editionen werden oft auch wahlweise als *Scholarly Digital Editions* oder *Digital Scholarly Editions* bezeichnet, was bereits ihren Anspruch deutlich macht: Es handelt sich um *wissenschaftliche* digitale Editionen von Kulturgütern. Die Verlagerung der kritischen Edition ins Digitale bewirkte eine reiche Definitions- und Methodendiskussion, sodass in Bezug auf eine einheitliche, allgemeingültige Definition Uneinigkeit herrscht {cite:p}`fritze_wohin_2019`.

Patrick Sahle definiert den Begriff wie folgt: „A scholarly edition is the critical representation of historic documents“ {cite:p}`sahle_what_2016`. Zum Verständnis dieser Definition ist es nötig, ihre zentralen Konzepte zu klären: 
- *Repräsentation*: Übertragung/Umcodierung eines Dokuments in ein anderes (oder das gleiche) Medium, z. B. Faksimile, Transkription
- *kritisch*: wissenschaftliche Auseinandersetzung mit dem Material (u. a. textuelle, bibliographische, materielle, visuelle Kritik), die reflektiert und regelgeleitet erfolgen soll (z. B. Festlegen von Transkriptionsrichtlinien, Annotation von Entitäten, Bewerten von Varianten)
- *Dokument*: materielles Dokument stets als Ausgangspunkt, Editionen nicht immer mit klar abgegrenztem Text, sondern z. B. auch von physischen Objekten
- *historisch*: zeitlicher Abstand zwischen Dokumententstehung und Rezeption (zeitgenössische Texte benötigen im Gegensatz zu historischen Dokumenten oft keine editorische Vermittlung, sondern „sprechen für sich selbst“)

Digitale Editionen erfüllen die gleiche grundlegende Aufgabe: Auch sie sollen historische Dokumente kritisch repräsentieren. 
Gegenüber klassischen Printeditionen bieten sie jedoch einige Vorteile, die sich aus den technischen Potenzialen und erweiterten Funktionalitäten digitaler Umgebungen ergeben:
- Multimodalität
- Variantenanzeige / parallele Ansichten
- Durchsuchbarkeit und Filterung (u. a. nach Metadaten)
- Interaktive Nutzungsmöglichkeiten
- nicht-lineare Navigations- und Darstellungsformen
- erweiterte Kontextualisierungsmöglichkeiten (durch ergänzende Informationen)
- (nachträgliche) Erweiterbarkeit und Aktualisierbarkeit der Edition

Bei ihrer Umsetzung gibt es einige Leitziele {cite:p}`fritze_wohin_2019`:
- Zugänglichkeit
- Durchsuchbarkeit 
- Benutzerfreundlichkeit
- Berechenbarkeit (Inhalte können von Computern analysiert, durchsucht und weiterverarbeitet werden → standardisierte Datenformate, klare Annotationen, APIs etc.)

Digitale Editionen sind insbesondere **keine**
- digitialisierten Printeditionen
- digitalen Faksimiles ohne editorischen Apparat
- Datenpublikationen, 
  
sondern eine eigene Form innerhalb der wissenschaftlichen Editionspraxis im digitalen Raum.

# Akteur*innen

Digitale Editionen entstehen oft im Rahmen von geisteswissenschaftlichen Forschungsprojekten an Universitäten, Archiven oder Bibliotheken. Durch ihren interdisziplinären Anspruch können Vertreter*innen einiger Disziplinen beteiligt sein: Neben den Digital Humanities sind das u. a. die Informatik und die Literatur-, Sprach- und Geschichtswissenschaften.

# Editionsformen und Typen

## Editionsformen
Wie eingangs erläutert, stehen digitale Editionen den traditionellen gedruckten Editionen gegenüber. Von einer *Hybridedition* spricht man, wenn eine Edition sowohl in digitalen als auch in analogen Medien publiziert wird {cite:p}`jannidis_digitale_2017`.

## Transkriptionstypen
*Transkription* bezeichnet in der Editionswissenschaft die „Übertragung eines historischen Quellentexts in ein modernes Medium, heutzutage i. d. R. maschinenlesbarer Text“ {cite:p}`klug_transkription_2021`. Es gibt mehrere Transkriptionsansätze, die für digitale Editionen sinnvoll sein können. 

Das Ziel einer *diplomatischen* Transkription ist es, die „historische Quelle so layout- und zeichengetreu wie möglich abzubilden“, wobei folgende Aspekte von Relevanz sind {cite:p}`cugliana_diplomatische_2024`:
- Dokumenteigenschaften: Abmessungen, Tinte, Schäden, Änderungen an der Integrität des physischen Objekts.
- Topologie: Struktur und Layout des Dokuments, Kollokation von Schriften und anderen Merkmalen auf der Schreibfläche.
- Handschrift: Anzahl der Hände, Buchstabenformen, Ligaturen.
- Orthographie: Rechtschreibung, diakritische Zeichen.
- Schriftmerkmale: Diese können unterteilt werden in:
  - Lesehilfen: Großschreibung, Zeichensetzung, Abstände.
  - Kurzschrift: Abkürzungen, Symbole, Chiffren.
- Genese: Revisionen, Streichungen, Hinzufügungen, funktionelle Indikatoren und andere Hinweise darauf, wie der Inhalt des Dokuments erstellt wurde.
- Textualität: Absätze, Überschriften, Verse, Tabellen, Listen, Rubriken und andere strukturelle Unterteilungen.
- Semantik: Daten, Namen von Personen und Orten, Schlagwörter.
- Linguistik: Wortarten, Lemmatisierung, Syntax.
- Textdekoration und andere grafische Komponenten: Miniaturen, Zeichnungen, Kritzeleien.

Diese Art der Transkription ist vor allem für sprachhistorische Forschung von Relevanz.

Der diplomatischen Transkription steht die *normalisierte* Transkription gegenüber: Hier werden historische oder individuelle Schreibweisen an eine standardisierte Norm angepasst. Das kann unter anderem Klein- und Großschreibung, Interpunktion, Konsonantenverdoppelung oder Getrennt- und Zusammenbeschreibung betreffen {cite:p}`galka_normalisierung_2021`. Dieses Vorgehen verbessert u. a. die Verständlichkeit und die computergestützte Auswertbarkeit des Textes.

Gerade bei digitalen Editionen bietet es sich an, mehrere Transkriptionsvarianten zur Verfügung zu stellen, welche das Editionsprojekt interdisziplinär nutzbar machen.

In jedem Fall sollten editorische Entscheidungen, wie genau transkribiert wird, in den *Transkriptionsrichtlinien* genau dokumentiert werden.
<!-- evtl. Beispiel für normalisiert vs diplomatisch? -->

## Textsorten
Textsorten, die sich besonders für digitale Editionen eignen, sind Briefe, Tagebücher, Notizbücher und Manuskripte, prinzipiell sind aber digitale Editionen vielfältiger textueller Dokumente und, darüber hinaus, physischer Kulturobjekte vorstell- und umsetzbar.

# Aufbau und Bestandteile
Das Herzstück jeder digitalen Edition ist das edierte *Dokument*, also im Falle einer Briefedition beispielsweise ein einzelner Brief. In der Regel wird dieser in mehreren Repräsentationen bereitgestellt. Neben einem digitalen Faksimile (meistens einem Scan der Originalquelle) liegen oft eine oder mehrere Transkriptionen vor. Ferner werden Metadaten zum Dokument zur Verfügung gestellt, die etwa zu Autor*in, Ort, Datierung oder Überlieferung Aufschluss geben. Diese Dokumente liegen dabei häufig im [TEI/XML-Format](../theorie/xml.md) vor.

Sie sind eingebettet in eine Projektwebsite, die nicht nur den Zugang zu den edierten Dokumenten ermöglicht, sondern auch Hintergrundinformationen zum Projekt und weitere Kontextualisierungen bietet: z. B. durch Editionsrichtlinien, editorische Kommentare oder Visualisierungen wie Zeitachsen, Netzwerkgrafiken oder Karten. Darüber hinaus enthalten viele digitale Editionen weitere funktionale Komponenten wie eine Volltextsuche oder eine Filterfunktion (z. B. nach Datierung, Ort, Person) zum Auffinden relevanter Texte.

All dies wird getragen von einem technischen Unterbau, der u. a. durch Datenbanktechnologien, Webframeworks und Versionierungssysteme realisiert wird.

# Nutzung
Digitale Editionen eröffnen vielfältige Forschungszugänge: Historiker\*innen können, neben der hermeneutischen Auseinandersetzung mit dem Material, historische Kontexte durch Zeitachsen, Georeferenzierung oder Netzwerkanalysen erschließen.  Sprachwissenschaftler\*innen nutzen digitale Editionen als Korpora (s. [**NLP**](natural-language-processing.md)) und können so etwa Varianten, Wortgebrauch oder stilistische Merkmale systematisch auswerten. Auch andere Disziplinen, wie die Literatur- und Religionswissenschaften oder die Kunstgeschichte, profitieren von den vielfältigen Möglichkeiten, die digitale Editionen bieten. Durch die digitale Aufbereitung und Auszeichnung der Texte sind computergestützte Untersuchungen möglich, die mit analogen Mitteln kaum denkbar wären. Nicht zuletzt sind digitale Editionen für die Informatik von Interesse, etwa bei der Entwicklung von Algorithmen für Handschriftenerkennung (z. B. {cite:t}`mayr_data-efficient_2025`) oder für semantische Annotation oder in der Forschung bei Fragen zu Usability, Datenmodellierung und Wissensrepräsentation.
Durch die digitale Aufbereitung und semantische Auszeichnung der Texte sind computergestützte Untersuchungen möglich, die mit analogen Mitteln kaum denkbar wären.

Über [APIs](apis.md) und Downloadfunktionen lassen sich strukturierte Daten exportieren, was wissenschaftliche Nachnutzbarkeit und Weiterverwendung gewährleistet. Jedoch veröffentlichen nicht alle Editionen ihren Quellcode oder bieten vollständige Datensätze an. Teilweise fehlen auch wichtige Informationen zur technischen Infrastruktur und zu den Daten, was nicht den FAIR-Prinzipien entspricht und Möglichkeiten der tieferen Analyse und Reproduzierbarkeit einschränkt.


# Herausforderungen und Chancen
Klar dokumentierte Editionsrichtlinien, die die Prinzipien der Transkription, Annotation, Normalisierung und editorischen Eingriffe festlegen, machen digitale Editionen transparent und nachvollziehbar. Diese konsistent zu halten und umzusetzen, ist oft eine Herausforderung in Projekten, an denen viele Bearbeitende beteiligt sind.

Im Allgemeinen umfasst der Editionsprozess viele Schritte (Digitalisierung, Transkription, Annotation, Kommentierung, technische Umsetzung, Publikation, ...), die im Team sinnvoll aufeinander abgestimmt und dokumentiert werden müssen.

Automatisierte Verfahren, unterstützt von KI-Technologien, wie OCR, automatische Annotation oder Named Entity Recognition, können Editionsworkflows sinnvoll unterstützen. Die Einsatzmöglichkeiten von LLMs bei digitalen Editionen werden unter anderem bei {cite:t}`czmiel_generative_2024` diskutiert. 

Gleichermaßen wirft ihr Einsatz aber auch Fragen der Qualitätssicherung und Transparenz auf. KI-gestützte Tools erfordern nicht nur ein technisches Verständnis durch die Editor*innen, die oft nicht aus technischen Disziplinen kommen, sondern auch eine kritische Reflexion ihrer Resultate.

Eine der größten Herausforderungen, vor denen digitale Editionsprojekte stehen, ist die Frage nach ihrer Nachhaltigkeit, Nachnutzbarkeit und Langzeitarchivierung. Im Gegensatz zu gedruckten Editionen, die, einmal produziert und entsprechend gelagert, leicht Jahrhunderte überstehen, haben digitale Editionen mit ihrem technologischen Unterbau weitaus größere Wartungsanforderungen, entstehen aber oft in zeitlich befristeten Projekten {cite:p}`birr_digitale_2024`, so dass über langfristige institutionelle Unterstützung und Hostingoptionen bereits bei Konzeption des Projektes nachgedacht werden sollte. 
Zur langfristigen Nutzbarkeit digitaler Editionen trägt außerdem bei, wenn offene Standards (wie TEI/XML) verwendet werden, Wert auf klare Dokumentation gelegt wird und Maßnahmen zur Langzeitarchivierung (etwa durch das Verwenden von Repositorien wie Zenodo) getroffen werden.
  

# Beispiele
Es gibt mehrere Kataloge für digitale Editionen, u. a.
- [Sammlung digitaler Editionen](https://www.digitale-edition.de/exist/apps/editions-browser/$app/index.html), von Patrick Sahle, umfassendster Katalog für den deutschsprachigen Raum
- [Catalogue Digital Editions](https://dig-ed-cat.acdh.oeaw.ac.at/), von Greta Franzini

Mit [correspSearch](https://correspsearch.net/de/start.html) kann eine Vielzahl Briefeditionen durchsucht werden (gedruckt und digital).

Einige Einzelbeispiele sollen im Folgenden gelistet werden:
- [Cooking Recipes of the Middle Ages](https://gams.uni-graz.at/context:corema)  
- [The Thomas Gray Archive](https://www.thomasgray.org/)  
- [Anne Frank Manuscripts](https://annefrankmanuscripten.org/en#home)  
- [Die keltischen Götternamen der germanischen Provinzen](https://gams.uni-graz.at/context:fercan)  
- [Paolo Bufalini's Notebook](https://projects.dharc.unibo.it/bufalini-notebook/)

<!--
# Ausblick
- semantische Vernetzung Linked Data
- kollaboratives Edieren
- KI im Editionsprozess
-->

# Quellen und weiterführende Informationen

Das [KONDE Weißbuch zum Thema *Digitale Edition*](https://www.digitale-edition.at/context:konde) ist eine Open Educational Resource, die sich spezifisch mit *Digitalen Editionen* befasst, zentrale Begrifflichkeiten klärt, Möglichkeiten aufzeigt und Beispiele nennt.

## Zitierte Literatur
```{bibliography}
:filter: docname in docnames
```