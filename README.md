🌿 LilyStudio

Eine browserbasierte All-in-One-Lösung für Materialverwaltung, Einkauf, Produktion und Kalkulation – entwickelt für Maker, Kreativbetriebe und kleine Unternehmen, die ihre Materialien und Arbeitsabläufe übersichtlich an einem Ort verwalten möchten.

LilyStudio ist als eigenes Praxisprojekt entstanden und wird kontinuierlich anhand realer Anforderungen weiterentwickelt.

✨ Besonderheiten

📦 Umfangreiche Materialverwaltung – Materialien lassen sich mit Kategorien, Materialarten, Farben, Maßen, Formen, Einheiten, Lagerorten, Lieferanten, Artikelnummern, Einkaufspreisen, Beständen und weiteren Informationen erfassen und verwalten.

🗂️ Flexible Kategorien & Stammdaten – Kategorien können hierarchisch organisiert werden. Farben, Lieferanten, Lagerorte, Einheiten und weitere Stammdaten werden zentral gepflegt und stehen anschließend im gesamten System zur Verfügung.

🖼️ Bildbasierte Materialübersicht – Materialien können mit mehreren Bildern hinterlegt werden. Ein Hauptbild sorgt für eine schnelle visuelle Orientierung in Übersichten und Bearbeitungsansichten.

🔎 Schnelle Navigation & Filterung – dynamisch erzeugte Kategorie-Kacheln, Unterkategorie-Shortcuts, Filter und Sortierungen ermöglichen auch bei einem größeren Materialbestand eine übersichtliche Navigation.

✏️ Sammel- & Tabellenbearbeitung – mehrere Materialien können gleichzeitig ausgewählt und entweder gemeinsam oder individuell in einer tabellarischen Ansicht bearbeitet werden.

📉 Intelligentes Nachbestellmanagement – Meldebestände erkennen Materialien mit niedrigem Bestand. Nachbestellungen können priorisiert, zurückgestellt oder bewusst ausgeschlossen werden.

🛒 Eigene Nachbestellplanung – offene Nachbesteller werden in einer separaten Tabellenansicht mit Bildern, Lieferanten, Beständen, Prioritäten und Notizen organisiert. Filter, Sortierung und Drag & Drop unterstützen die Planung größerer Bestellungen.

🏷️ Mehrere Beschaffungszustände – Materialien können unter anderem als automatisch nachzubestellen, zurückgestellt, nicht nachzubestellen oder nicht mehr verfügbar gekennzeichnet werden.

🚚 Lieferanten & Bezugsquellen – Materialien lassen sich Lieferanten und bevorzugten Bezugsquellen zuordnen und mit relevanten Einkaufsinformationen ergänzen.

📜 Bestands- & Einkaufshistorie – Bestandsbewegungen und Einkäufe bleiben nachvollziehbar, sodass nicht nur der aktuelle Bestand, sondern auch dessen Entwicklung sichtbar ist.

🧮 Kalkulation & Produktion – LilyStudio geht über eine reine Inventarliste hinaus und verbindet die Materialverwaltung mit Funktionen für Produktkalkulation und Produktionsabläufe.

💾 Lokale Nutzung – LilyStudio ist als leichtgewichtige browserbasierte Anwendung konzipiert und benötigt kein großes externes Software-Ökosystem.

📦 Materialverwaltung

Das Herzstück von LilyStudio ist die Materialdatenbank.

Ein Material kann nicht nur mit einem Namen und Bestand erfasst werden, sondern mit zahlreichen Informationen beschrieben und strukturiert werden. Dazu gehören beispielsweise:

Kategorie und Materialart
Farbe
Breite bzw. Größe
Form
Einheit
Lagerort
Lieferant und Bezugsquelle
Artikelnummer
Einkaufspreis
aktueller Bestand und Meldebestand
Bilder und Hauptbild
Notizen
Nachbestellstatus und Priorität

Kategorien können verschachtelt werden, sodass auch umfangreichere Materiallager sinnvoll strukturiert bleiben.

🛒 Einkauf & Nachbestellung

LilyStudio erkennt anhand der hinterlegten Meldebestände, welche Materialien nachbestellt werden sollten.

Dabei bedeutet ein niedriger Bestand jedoch nicht automatisch, dass ein Material tatsächlich auf der Einkaufsliste landen muss. Materialien können beispielsweise bewusst zurückgestellt, nicht nachbestellt oder als nicht mehr verfügbar gekennzeichnet werden.

Die Nachbestellplanung bietet eine eigene tabellarische Arbeitsansicht mit:

Materialbild und Bezeichnung
Lieferant
Bestand und Meldebestand
mehrstufiger Priorisierung
individuellen Notizen
Filtern und Gruppierungen
sortierbaren Spalten
manueller Reihenfolge per Drag & Drop

Damit wird aus einer einfachen Warnung bei niedrigem Bestand eine tatsächliche Einkaufsplanung.

✏️ Mehrfachbearbeitung

Gerade bei großen Materialbeständen wäre es umständlich, jeden Datensatz einzeln öffnen zu müssen.

LilyStudio bietet deshalb zwei unterschiedliche Wege zur Mehrfachbearbeitung:

Sammelbearbeitung
Ein Wert kann gleichzeitig auf mehrere ausgewählte Materialien angewendet werden.

Tabellenbearbeitung
Ausgewählte Materialien werden gemeinsam in einer Tabelle dargestellt und können dort trotzdem individuell bearbeitet werden.

Die Materialauswahl unterstützt dabei auch größere zusammenhängende Auswahlbereiche.

🏭 Produktion & Kalkulation

LilyStudio ist nicht nur als Lagerverwaltung gedacht.

Materialbestand, Einkauf, Produktdaten und Produktion sollen innerhalb einer gemeinsamen Anwendung miteinander verbunden werden. Dadurch können Materialien nicht nur verwaltet, sondern auch im Kontext der daraus entstehenden Produkte betrachtet werden.

Die Bereiche Produkte, Produktion und Kalkulation werden deshalb unabhängig voneinander weiterentwickelt und greifen auf dieselbe zentrale Materialbasis zurück.

🎯 Projektziel

Viele klassische Warenwirtschafts- und Inventarsysteme sind für kleine kreative Unternehmen entweder zu umfangreich, zu unflexibel oder mit laufenden Kosten verbunden.

LilyStudio verfolgt deshalb einen anderen Ansatz:

Eine übersichtliche und flexibel erweiterbare Arbeitsumgebung, die sich an den tatsächlichen Abläufen kleiner Produktions- und Kreativbetriebe orientiert.

Das Projekt wird iterativ entwickelt. Neue Funktionen entstehen nicht anhand eines theoretischen Feature-Katalogs, sondern aus konkreten Anforderungen im täglichen Einsatz.

🛠️ Technologien
HTML5 – Struktur und Benutzeroberfläche
CSS3 – responsives Layout, Komponenten und Benutzerinteraktionen
Vanilla JavaScript – Anwendungslogik ohne Frontend-Framework
Browser APIs – lokale Datenhaltung und interaktive Funktionen
Drag & Drop – unter anderem für Priorisierung und Organisation

LilyStudio verwendet bewusst kein React, Vue, Angular oder vergleichbares Frontend-Framework.

📁 Projektstruktur

LilyStudio wird modular innerhalb einer browserbasierten Anwendung weiterentwickelt.

Die vollständige interne Projektstruktur und Implementierungsdetails werden in diesem Repository bewusst nicht veröffentlicht.

🚧 Entwicklungsstand

LilyStudio befindet sich in aktiver Entwicklung.

Die Anwendung wird regelmäßig erweitert und optimiert. Neben neuen Funktionen gehören dazu insbesondere Verbesserungen an Bedienung, Datenverwaltung, Performance und Workflows für größere Materialbestände.

Änderungen der einzelnen Versionen werden im Changelog dokumentiert.

🔒 Quellcode

Dieses Repository dient in erster Linie der Dokumentation und Präsentation des Projekts sowie seiner Weiterentwicklung.

Der vollständige Quellcode von LilyStudio ist derzeit nicht öffentlich verfügbar.

Screenshots, Funktionsbeschreibungen und Changelogs zeigen den Entwicklungsstand des Projekts, ohne die vollständige Implementierung offenzulegen.

🗺️ Weiterentwicklung

LilyStudio wird kontinuierlich ausgebaut. Geplant sind unter anderem weitere Verbesserungen in den Bereichen:

Materialverwaltung · Einkauf · Nachbestellung · Produkte · Produktion · Kalkulation · Auswertungen · Benutzerfreundlichkeit

Der Fokus liegt dabei darauf, auch bei wachsenden Datenbeständen eine schnelle und übersichtliche Bedienung zu erhalten.

📌 Status

Aktive Entwicklung · Vanilla JavaScript · Browserbasiert
