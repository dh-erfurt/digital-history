# Digitale Editionen
 
Digitale Editionen sind ein zentraler Forschungsschwerpunkt in den Digital Humanities. Sie widmen sich der digitalen Erschließung, Edition und Veröffentlichung kultureller Güter (z. B. historischer Textsammlungen) und machen diese für Wissenschaft und Öffentlichkeit gleichermaßen zugänglich und nutzbar. Im Vergleich zu klassischen Druckeditionen bieten sie erweiterte Möglichkeiten, etwa die Integration multimedialer Inhalte oder die Einbindung interaktiver Funktionalität. 

Dieses Kapitel wird nach einer initialen Begriffsklärung grundlegende Konzepte darlegen und Möglichkeiten und Herausforderungen digitaler Editionspraxis diskutieren.

Diese Seite befindet sich im Aufbau.

<!--
https://zenodo.org/records/10698210
# Begriffsklärung
Digitale Editionen werden oft auch wahlweise als *Scholarly Digital Editions* oder *Digital Scholarly Editions* bezeichnet, was bereits ihren Anspruch deutlich macht: Es handelt sich um *wissenschaftliche* digitale Editionen von Kulturgütern. Die Verlagerung der kritischen Edition ins Digitale bewirkte eine reiche Definitions- und Methodendiskussion, so dass im Bezug auf eine einheitliche, allgemeingültige Definition Uneinigkeit herrscht {cite:p}`fritze_wohin_2019`.

Patrick Sahle definiert den Begriff wie folgt: „A scholarly edition is the critical representation of historic documents“ {cite:p}`sahle_what_2016`. Zum Verständnis dieser Definition ist es nötig, ihre zentralen Konzepte zu klären: 
- *Repräsentation*: Übertragung/Umcodierung eines Dokuments in ein anderes (oder das gleiche) Medium, z.B. Faksimile, Transkription
- *kritisch*: wissenschaftliche Auseinandersetzung mit dem Material (u.a. textuelle, bibliographische, materielle, visuelle Kritik), die reflektiert und regelgeleitet erfolgen soll (z.B. Festlegen von Transkriptionsrichtlinien, Annotation von Entitäten, Bewerten von Varianten)
- *Dokument*: materielles Dokument stets als Ausgangspunkt, Editionen nicht immer mit klar abgegrenztem Text, sondern z.B. auch von physischen Objekten
- *historisch*: zeitlicher Abstand zwischen Dokumententstehung und Rezeption (zeitgenössische Texte benötigen im Gegensatz zu historischen Dokumenten oft keine editorische Vermittlung, sondern „sprechen für sich selbst“)

Digitale Editionen erfüllen die gleiche grundlegende Aufgabe: Auch sie sollen historische Dokumente kritisch repräsentieren. 
Gegenüber klassischen Printeditionen bieten sie jedoch einige Vorteile, die sich aus den technischen Potenzialen und erweiterten Funktionalitäten digitaler Umgebungen ergeben:
- Multimodalität
- Variantenanzeige / parallele Ansichten
- Durchsuchbarkeit und Filterung (u.a. nach Metadaten)
- Interaktive Nutzungsmöglichkeiten
- nicht-lineare Navigations- und Darstellungsformen
- erweiterte Kontextualisierungsmöglichkeiten (durch ergänzende Informationen)
- (nachträgliche) Erweiterbarkeit und Aktualisierbarkeit der Edition

Bei ihrer Umsetzung gibt es einige Leitziele {cite:p}`fritze_wohin_2019`:
- Zugänglichkeit
- Durchsuchbarkeit 
- Benutzerfreundlichkeit
- Berechenbarkeit (Inhalte könenn von Computern analysiert, durchsucht und weiterverarbeitet werden → standardisierte Datenformate, klare Annotationen, APIs etc.)

Digitale Editionen sind insbesondere keine
- digitialisierten Printeditionen
- digitalen Facsimiles ohne editorischen Apparat
- Datenpublikationen, 
sondern eine eigene Form innerhalb der wissenschaftlichen Editionspraxis im digitalen Raum.

# Editionsformen und Typen
## Typen
*Transkription* bezeichnet in der Editionswissenschaft die „Übertragung eines historischen Quellentexts in ein modernes Medium, heutzutage i.d.R. maschinenlesbarer Text“{cite:p}`klug_transkription_2021`. Es gibt mehrere Transkriptionsansätze, die für digitale Editionen sinnvoll sein können. 

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

Der diplomatischen Transkription steht die *normalisierte* Transkription gegenüber: Hier werden historische oder individuelle Schreibweisen an eine standardisierte Norm angepasst. Das kann unter anderem Klein- und Großschreibung, Interpunktion, Konsonantenverdoppelung oder Getrennt- und Zusammenbeschreibung betreffen {cite:p}`galka_normalisierung_2021`. Dieses Vorgehen verbessert u.a. die Verständlichkeit und die computergestützte Auswertbarkeit des Textes.

Gerade bei digitalen Editionen bietet es sich an, mehrere Transkriptionsvarianten zur Verfügung zu stellen, welche das Editionsprojekt interdisziplinär nutzbar machen.

In jedem Fall sollten editorische Entscheidungen, wie genau transkribiert wird, in den *Transkriptionsrichtlinien* genau dokumentiert werden.

## Textsorten
Textsorten, die sich besonders für digitale Editionen eignen, sind Briefe, Tagebücher, Notizbücher und Manuskripte, prinzipiell sind aber digitale Editionen vielfältiger textueller Dokumente und, darüber hinaus, physischer Kulturobjekte möglich.

# Aufbau und Bestandteile
- TEI/XML + Seite pro Dokument (Facsimile, Metadaten)
- Annotation, Varianten
- Suchfunktionen, Filter
- Visualisierungen
- drum herum

# Herausforderungen 
- Nachhaltigkeit/Langzeitarchivierung
- Editionsrichtlinieen
- Automatisierung
- Workflows
  
# Nutzung
- Forschungszugänge z.B. historisch, sprachwissenschaftlich
- Möglichkeiten der Nachnutzung (APIs, Downloads)
- Grenzen: Code nicht transparent, nicht komplette Daten

# Beispiele

[Sammlung digitaler Editionen](https://www.digitale-edition.de/exist/apps/editions-browser/$app/index.html)

# Ausblick
- semantische Vernetzung Linked Data
- kollaboratives Edieren
- KI im Editionsprozess

# Quellen und weiterführende Informationen

Das [KONDE Weißbuch zum Thema *Digitale Edition*](https://www.digitale-edition.at/context:konde) ist eine Open Educational Resource, die sich spezifisch mit *Digitalen Editionen* befasst, zentrale Begrifflichkeiten klärt, Möglichkeiten aufzeigt und Beispiele nennt.

## Zitierte Literatur
```{bibliography}
:filter: docname in docnames
```
-->