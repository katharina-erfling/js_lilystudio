# 📝 LilyStudio -- Changelog

Alle wichtigen Änderungen und Entwicklungsschritte von **LilyStudio**.

> LilyStudio wird iterativ anhand realer Arbeitsabläufe
> weiterentwickelt.\
> Der Changelog dokumentiert Funktionen, Verbesserungen und
> Fehlerbehebungen, ohne interne Implementierungsdetails offenzulegen.

------------------------------------------------------------------------
## v1.25.0

### ✨ Neu
- Breiten- und Durchmesservorschläge in der Materialanlage werden jetzt kategoriebasiert verwaltet.
- Bereits verwendete Maße einer Kategorie stehen automatisch als Vorschläge zur Verfügung.
- Neue Maße können direkt zur jeweiligen Kategorie ergänzt werden.
- Escape schließt offene Vorschlagslisten, Auswahlfelder oder den aktuell geöffneten Dialog.

### 🐛 Behoben
- Enter in der Namensvervollständigung speicherte teilweise den Artikel, statt einen Vorschlag zu übernehmen.
- Enter in geöffneten Stammdaten-Auswahlen konnte fälschlich den gesamten Materialdialog speichern.
- Neu angelegte Material-Stammdaten ließen sich teilweise nicht zuverlässig auswählen.

### 🔄 Verbessert
- Enter übernimmt bei Namensvorschlägen standardmäßig den ersten passenden Treffer, wenn noch kein Eintrag aktiv markiert wurde.
- Neu angelegte Materialien werden direkt vollständig als Stammdaten übernommen und ausgewählt.

## v1.24.0

### ✨ Neu
- Preis- und Verfügbarkeitsinformationen der bevorzugten Bezugsquelle sind jetzt direkt im oberen Materialbereich erreichbar.
- Dort können zusätzlich zum aktuellen Einkaufspreis gepflegt werden:
  - Verfügbarkeitsstatus
  - Regulärpreis
  - Aktionsende
  - Aktionsnotiz
- Rabatt gegenüber dem Regulärpreis wird direkt angezeigt.
- Dezenter „Nach oben“-Button ergänzt, der erst nach längerem Scrollen erscheint.

### 🔄 Verbessert
- Preis- und Aktionsinformationen oben im Materialdialog und in der bevorzugten Bezugsquelle werden miteinander synchronisiert.
- Historie und Bestellhistorie erhalten bei mehr als sechs Einträgen einen eigenen Scrollbereich.
- Lange Materialdialoge bleiben dadurch deutlich kompakter und besser navigierbar.

### v1.23.1

#### 🐛 Behoben
- Der in v1.23.0 eingeführte Bezugsquellenvergleich war im Materialdialog teilweise nicht sichtbar und dadurch nicht erreichbar.

#### 🔄 Verbessert
- Der Bezugsquellenbereich besitzt jetzt eine feste Vergleichsleiste.
- Anzahl der hinterlegten Bezugsquellen wird direkt angezeigt.
- Der Bezugsquellenvergleich kann über **„Vergleichen“** unmittelbar oberhalb der Bezugsquellen geöffnet werden.

## v1.23.0

### ✨ Neu
- Bezugsquellen können einen eigenen Verfügbarkeitsstatus erhalten:
  - Normal
  - Abverkauf
  - Ausverkauft
  - Nicht mehr verfügbar
- Regulärpreis und aktueller Einkaufspreis können getrennt gepflegt werden.
- Preisreduzierungen werden automatisch als prozentualer Rabatt berechnet.
- Optionales Enddatum für Preisaktionen ergänzt.
- Eigene Aktionsnotiz pro Bezugsquelle ergänzt.
- Neuer Bezugsquellenvergleich direkt innerhalb eines Materials.
- Vergleichsansicht für Preis, Rabatt, Verfügbarkeit, Gebinde,
  Mindestabnahme und Versandbedingungen.

### 🔄 Verbessert
- Einkaufsbedingungen verschiedener Händler lassen sich direkt miteinander vergleichen.
- Die bevorzugte Bezugsquelle wird im Vergleich hervorgehoben.
- Abverkauf und Verfügbarkeit werden artikelspezifisch je Bezugsquelle verwaltet,
  statt den gesamten Lieferanten oder das Material pauschal zu kennzeichnen.

### v1.22.2

#### ✨ Neu
- Autovervollständigung für Materialnamen ergänzt.
- Bereits verwendete Namen werden während der Eingabe als Vorschläge angeboten.
- Häufig verwendete Bezeichnungen werden bevorzugt angezeigt.
- Vorschläge können per Maus oder Tastatur übernommen werden.

#### 🔄 Verbessert
- Freie Namenseingabe bleibt vollständig erhalten.
- Ähnliche Materialbezeichnungen lassen sich konsistenter wiederverwenden.

### v1.22.1

#### 🐛 Behoben
- Bei der Auswahl einer vorhandenen Breite bzw. eines Durchmessers aus der Vorschlagsliste wurde teilweise nur der Zahlenwert übernommen.
- Die hinterlegte Maßeinheit der Materialart wird jetzt auch bei Auswahl aus vorhandenen Vorschlägen direkt ergänzt.

## v1.22.0

### ✨ Neu
- Bezugsquellen können jetzt um zusätzliche Einkaufsinformationen ergänzt werden.
- Neue Felder für:
  - Gebinde
  - Mindestabnahme
  - Versandkosten
  - Versandkostenfrei ab
  - individuelle Notizen
- Die zusätzlichen Angaben werden direkt an der jeweiligen Bezugsquelle gespeichert und erleichtern den Vergleich mehrerer Lieferanten.

### 🔄 Verbessert
- Bezugsquellen wurden übersichtlicher in mehrere Informationsbereiche gegliedert.
- Vergleichsrelevante Einkaufsbedingungen sind jetzt direkt beim Material sichtbar.

### v1.21.2

#### 🐛 Behoben
- Maßeinheiten bei Breite bzw. Durchmesser gingen nach dem Neuladen teilweise verloren.
- Werte wie `20 mm` wurden nach `F5` teilweise nur noch als `20` angezeigt.

#### 🔄 Verbessert
- Breite bzw. Durchmesser werden jetzt zusätzlich als vollständiger Maßtext inklusive Einheit gespeichert.
- Bestehende Materialien werden beim Laden automatisch auf die hinterlegte Maßeinheit ihrer Materialart abgeglichen.

### v1.21.1

#### 🐛 Behoben
- Die in v1.21.0 eingeführte Vervollständigung neuer Breiten war aufgrund einer falschen Stammdatenreferenz nicht aktiv.
- Neue Breiten werden jetzt zuverlässig gegen die verfügbaren Maße des gewählten Materials geprüft.

#### 🔄 Verbessert
- Neue Breiten und Durchmesser werden über einen eigenen LilyStudio-Dialog zur Übernahme in die Stammdaten angeboten.
- Ein Wert kann alternativ weiterhin nur für den aktuellen Artikel verwendet werden.

## v1.21.0

### ✨ Neu
- Breiten können direkt beim Bearbeiten eines Materials als neue Stammdaten ergänzt werden.
- Wird eine bisher unbekannte Breite eingegeben, bietet LilyStudio beim Speichern automatisch an, diese für die gewählte Materialart zu übernehmen.
- Unterschiedliche Schreibweisen wie `20`, `20mm` und `20 mm` werden beim Abgleich vereinheitlicht.

### 🔄 Verbessert
- Freie Breiteneingaben bleiben weiterhin möglich, auch wenn eine neue Breite nicht in die Stammdaten übernommen werden soll.
- Maßeinheiten werden bei der Vervollständigung automatisch anhand der Materialart berücksichtigt


## 🌿 v1.20 -- Nachbestellmanagement

### v1.20.9

#### 🐛 Behoben
- Beim Löschen eines Historieneintrags wirkte die gesamte Historie teilweise leer, obwohl andere Einträge noch vorhanden waren.
- Eine ältere Bestandsansicht überschrieb nach dem Löschen die kombinierte Materialhistorie.
- Gelöschte Historieneinträge konnten nach erneutem Öffnen teilweise wieder erscheinen und mussten mehrfach gelöscht werden.

#### 🔄 Verbessert
- Löschvorgänge der Historie werden jetzt als abgeschlossener Datenstand gespeichert.
- Historie und Bestellhistorie werden unmittelbar nach dem Löschen sauber aktualisiert.

### v1.20.8

#### ✨ Neu
- Historieneinträge können direkt im Materialdialog gelöscht werden.
- Die Löschfunktion ist bewusst dezent in die Historie integriert und besitzt eine Sicherheitsabfrage.

#### 🔄 Verbessert
- **Enter** speichert ein Material jetzt auch dann, wenn gerade ein Auswahlfeld wie „Form“ fokussiert ist.
- **Shift + Enter** bleibt in mehrzeiligen Notizfeldern für Zeilenumbrüche verfügbar.

#### 🛡️ Sicherheit
- Verknüpfte Einkaufs- und Produktionsbuchungen können nicht versehentlich über die Materialhistorie gelöscht werden und bleiben an ihren jeweiligen Ursprungsdatensatz gebunden.


### v1.20.7

#### 🔄 Verbessert
- Der aktuelle Einkaufspreis eines Materials wird jetzt unabhängig von historischen Warenzugängen gepflegt.
- Einkaufspreise werden in Eingabefeldern sauber auf zwei Nachkommastellen dargestellt.
- Mit **Enter** kann ein Material direkt gespeichert werden.
- **Shift + Enter** bleibt in mehrzeiligen Notizfeldern für Zeilenumbrüche verfügbar.

#### 🐛 Behoben
- Manuell eingetragene Einkaufspreise wurden bei Materialien mit vorhandener Einkaufshistorie teilweise wieder überschrieben.
- JavaScript-Gleitkommaartefakte wie `2,7900000000000005` werden nicht mehr im Preisfeld angezeigt.


### v1.20.6

#### ✨ Neu

-   Nachbestellungen verfügen jetzt über **fünf Prioritätsstufen**:
    -   Sehr hoch
    -   Hoch
    -   Normal
    -   Niedrig
    -   Sehr niedrig
-   Spaltenüberschriften der Nachbestellliste sind anklickbar und
    sortieren die Tabelle.
-   Ein weiterer Klick auf dieselbe Spalte kehrt die Sortierreihenfolge
    um.
-   Die aktive Sortierung wird visuell gekennzeichnet.

#### 🔄 Verbessert

-   **Drag & Drop beeinflusst jetzt direkt die Priorität** eines
    Nachbestellers.
-   Je weiter oben ein Material eingeordnet wird, desto höher wird seine
    Priorität.
-   Die manuelle Reihenfolge wird nach dem Verschieben wieder zur
    maßgeblichen Sortierung.

------------------------------------------------------------------------

### v1.20.5

#### ✨ Neu

-   Eigene Seitennavigation für große Nachbestelllisten.
-   Bis zu **50 Nachbesteller pro Seite**.
-   Filter nach:
    -   Lieferant
    -   Kategorie
    -   Priorität
-   Gruppierung nach:
    -   Lieferant
    -   Kategorie
    -   Priorität

#### 🐛 Behoben

-   Maßeinheiten wie `mm` bleiben bei Breite bzw. Durchmesser nach dem
    Neuladen sichtbar.

------------------------------------------------------------------------

### v1.20.4

#### 🐛 Behoben

-   Im Nachbestellmodus wird die normale Materialkartenansicht nicht
    mehr zusätzlich unter der Nachbestelltabelle angezeigt.
-   Normale Material-Pagination und leere Zustände werden im
    Nachbestellmodus korrekt ausgeblendet.

------------------------------------------------------------------------

### v1.20.3

#### 🔄 Verbessert

-   Nachbesteller werden in **einer gemeinsamen tabellarischen
    Arbeitsansicht** dargestellt.
-   Materialbilder wurden in die Nachbestellliste integriert.
-   Materialname, Kategorie, Lieferant, Bestand, Meldebestand, Priorität
    und Notiz werden gemeinsam angezeigt.
-   Materialien können direkt aus der Nachbestellliste geöffnet werden.
-   Drag & Drop wurde direkt in die Tabelle integriert.

#### 🐛 Behoben

-   Einkaufspreise bleiben nach dem Neuladen erhalten.
-   Die bevorzugte Bezugsquelle überschreibt einen vorhandenen
    Einkaufspreis nicht mehr unbeabsichtigt.
-   Manuelle Drag-&-Drop-Reihenfolgen werden nicht mehr unmittelbar
    durch eine automatische Prioritätssortierung überschrieben.

------------------------------------------------------------------------

### v1.20.2

#### 🐛 Behoben

-   Persistenzfehler beim Neuladen behoben.
-   **Lieferant**, **Form** und **Breite/Durchmesser** bleiben nach `F5`
    erhalten.
-   Neuere Materialfelder werden beim Laden nicht mehr durch ältere
    Datenstrukturen verworfen.
-   Bestehende Referenzen werden beim Start verlustfrei synchronisiert.

------------------------------------------------------------------------

### v1.20.1

#### 🐛 Behoben

-   Lieferantenverknüpfungen wurden stabilisiert.
-   Ein vorhandener Lieferant bleibt erhalten, auch wenn ein
    Dialogzustand vorübergehend leer ist.
-   Material und bevorzugte Bezugsquelle werden zuverlässiger
    miteinander synchronisiert.
-   Bestehende Materialien werden beim Start soweit möglich automatisch
    repariert.

------------------------------------------------------------------------

### v1.20.0

#### ✨ Neu

-   Eigenständiges **Nachbestellmanagement** eingeführt.
-   Materialien können unterschiedliche Nachbestellzustände erhalten:
    -   Automatisch
    -   Zurückgestellt
    -   Nicht nachbestellen
    -   Nicht mehr verfügbar
-   Prioritäten für Nachbesteller eingeführt.
-   Individuelle Nachbestellnotizen ergänzt.
-   Eigene Nachbestellplanung eingeführt.
-   Materialien mit bewusst deaktivierter Nachbestellung werden
    weiterhin sichtbar gekennzeichnet.
-   Die Nachbestellanzahl berücksichtigt nur tatsächlich aktive
    Nachbesteller.
-   Drag & Drop für die manuelle Reihenfolge der Nachbestellplanung
    eingeführt.

------------------------------------------------------------------------

## 🗂️ v1.19 -- Kategorien & Materialnavigation

### v1.19.11

#### 🐛 Behoben

-   Tabellenbearbeitung bei Mehrfachauswahl weiter stabilisiert.
-   Fehlerhafte Einzelwerte führen nicht mehr dazu, dass die gesamte
    Tabellenansicht auf eine reduzierte Darstellung zurückfällt.
-   Auswahlanzahl und Tabellenaufbau wurden robuster miteinander
    synchronisiert.

------------------------------------------------------------------------

### v1.19.10

#### 🔄 Verbessert

-   Tabellenbearbeitung robuster gegen fehlerhafte oder unvollständige
    Materialdaten gemacht.

#### 🐛 Behoben

-   Fehler beim Rendern auswählbarer Tabellenspalten behoben.
-   Lieferant bleibt als bearbeitbare Spalte verfügbar.

------------------------------------------------------------------------

### v1.19.9

#### ✨ Neu

-   **Lieferant** kann jetzt auch über die Mehrfachauswahl geändert
    werden.
-   Lieferantenänderung sowohl in der Sammelbearbeitung als auch in der
    Tabellenbearbeitung möglich.

#### 🔄 Verbessert

-   Bevorzugte Bezugsquelle wird bei einer Lieferantenänderung
    entsprechend aktualisiert.
-   Vorhandene Einkaufsinformationen bleiben soweit möglich erhalten.

------------------------------------------------------------------------

### v1.19.8

#### 🐛 Behoben

-   Lieferant und bevorzugte Bezugsquelle werden zuverlässiger
    synchronisiert.
-   Ein oben im Materialdialog gewählter Lieferant wird in die
    bevorzugte Bezugsquelle übernommen.
-   Falls noch keine Bezugsquelle vorhanden ist, kann diese aus den
    vorhandenen Materialinformationen ergänzt werden.

------------------------------------------------------------------------

### v1.19.7

#### 🧹 Bereinigt

-   Redundantes Feld **„Breite / Größe"** aus dem Bereich
    Bestand/Einheit entfernt.
-   Materialmaße werden nur noch an der fachlich passenden Stelle
    gepflegt.

------------------------------------------------------------------------

### v1.19.6

#### 🐛 Behoben

-   Anfangsbestand eines neu angelegten Materials wird nicht mehr
    fälschlich als **Bestandskorrektur** protokolliert.
-   Der Anfangsbestand gehört jetzt ausschließlich zum Ereignis
    **„Material angelegt"**.

------------------------------------------------------------------------

### v1.19.5

#### 🔄 Verbessert

-   Breite bzw. Materialmaß akzeptiert wieder **freie Texteingaben**.
-   Angaben wie `20 mm`, `2 cm` oder ähnliche Maße sind möglich.
-   Numerische Werte können weiterhin für Filter und Berechnungen
    ausgewertet werden.

------------------------------------------------------------------------

### v1.19.4

#### 🐛 Behoben

-   Breite/Durchmesser ist wieder frei eingebbar.
-   Hinterlegte Breiten dienen als Vorschläge und nicht mehr als
    verpflichtende Auswahl.

------------------------------------------------------------------------

### v1.19.3

#### 🎨 Oberfläche

-   Abstände innerhalb der neuen Kategorie-Kacheln korrigiert.
-   Kategoriename und Materialanzahl werden sauber getrennt und können
    ordentlich umbrechen.

------------------------------------------------------------------------

### v1.19.2

#### 🔄 Verbessert

-   Mehrfachauswahl bleibt auch bei langen Materiallisten gut
    erreichbar.
-   Die Aktionsleiste kann beim Scrollen am unteren Fensterrand
    verfügbar bleiben.
-   Beim Anlegen neuer Materialien werden keine Statusinformationen
    eines zuvor geöffneten Materials übernommen.

------------------------------------------------------------------------

### v1.19.1

#### 🐛 Behoben

-   Navigation aus einer ausgewählten Kategorie zurück zur
    Materialübersicht ergänzt.
-   Breadcrumb-Navigation für Kategorieansichten verbessert.
-   Darstellung im Dialog **„Einkauf erfassen"** bereinigt.

------------------------------------------------------------------------

### v1.19.0

#### ✨ Neu

-   **Hierarchische Kategorien** eingeführt.
-   Kategorien können übergeordnete Kategorien besitzen.
-   Startansicht der Materialien zeigt automatisch erzeugte Kacheln der
    jeweils höchsten Kategorieebene.
-   Klick auf eine Hauptkategorie öffnet direkt die normale
    Materialansicht für diesen Bereich.
-   Unterkategorien können als kompakte Filter-Shortcuts verwendet
    werden.
-   Kategoriepfade und Hierarchien werden bei Import und Sicherung
    erhalten.
-   Kategorie-Zusammenführung berücksichtigt die Baumstruktur.

#### 🎯 Ziel

-   Auch bei mehreren hundert oder tausend Materialien soll die
    Materialübersicht schnell erfassbar bleiben, ohne sich durch unnötig
    viele Kategorieebenen klicken zu müssen.

------------------------------------------------------------------------

## ⚡ v1.18 -- Bedienung & Massenbearbeitung

### v1.18.16

#### 🧹 Bereinigt

-   Direkte Warenzugangserfassung aus dem Materialdialog entfernt.
-   Warenzugänge werden über den dafür vorgesehenen Einkaufsworkflow
    gepflegt.
-   Der normale Materialdialog bleibt auf Stammdaten und direkte
    Materialbearbeitung konzentriert.

------------------------------------------------------------------------

### v1.18.15

#### ✨ Neu

-   **Kompakte Materialhistorie** eingeführt.
-   Anlage eines Materials wird dokumentiert.
-   Manuelle Änderungen an Stammdaten werden nachvollziehbar.
-   Änderungen aus Sammel- und Tabellenbearbeitung können protokolliert
    werden.
-   Reine Bestellhistorie eines Materials wurde in die Materialansicht
    integriert.

#### 🎨 Oberfläche

-   Historienansicht kompakter und übersichtlicher gestaltet.

------------------------------------------------------------------------

### v1.18.13

#### 🔄 Verbessert

-   Tabellenbearbeitung und Materialauswahl weiter stabilisiert.
-   Bearbeitungsabläufe für größere Materialmengen verfeinert.

------------------------------------------------------------------------

### v1.18.12

#### 🔄 Verbessert

-   Vorschaubilder innerhalb der Tabellenbearbeitung optimiert.
-   Bildausschnitte stärker auf das eigentliche Material fokussiert.

------------------------------------------------------------------------

### v1.18.11

#### 🐛 Behoben

-   Öffnen der Tabellenbearbeitung über **„Bearbeiten"**
    wiederhergestellt.

------------------------------------------------------------------------

### v1.18.10

#### ✨ Neu

-   Kleine, nicht bearbeitbare **Materialvorschaubilder** in der ersten
    Spalte der Tabellenbearbeitung ergänzt.

------------------------------------------------------------------------

### v1.18.9

#### 🎨 Oberfläche

-   Bezeichnungen und Modi der Mehrfachbearbeitung vereinfacht.
-   Bearbeitungsarten klarer voneinander getrennt.

------------------------------------------------------------------------

### v1.18.8

#### ✨ Neu

-   Erweiterte **Tabellenbearbeitung** für mehrere ausgewählte
    Materialien.
-   Unterschiedliche Werte können für jedes Material direkt in einer
    gemeinsamen Tabelle gepflegt werden.
-   Bearbeitbare Felder können gezielt ausgewählt werden.
-   Grunddaten wie Bestand, Einkaufspreis und Artikelnummer können in
    die Tabellenbearbeitung einbezogen werden.

------------------------------------------------------------------------

### v1.18.4

#### ✨ Neu

-   Massenbearbeitung deutlich erweitert.
-   Mehrere Materialien können gemeinsam ausgewählt und bearbeitet
    werden.
-   Auswahl nach Materialgruppen bzw. Kategorien unterstützt.
-   Gemeinsame Werte können auf mehrere Materialien angewendet werden.

------------------------------------------------------------------------

### v1.18.3

#### ✨ Neu

-   Grundlage für die **Mehrfachauswahl von Materialien** geschaffen.
-   Auswahlmodus in die Materialübersicht integriert.
-   Auswahloberfläche bewusst kompakt gehalten und erst bei aktiver
    Auswahl eingeblendet.
-   Bereichsauswahl mit **Shift + Mausklick** ergänzt.

------------------------------------------------------------------------

### v1.18.2

#### 🧹 Datenmodell

-   Redundante **Materialart** entfernt.
-   Kategorie und Material/Werkstoff werden klar voneinander getrennt.
-   Beispiel:
    -   Kategorie: `Beschläge`
    -   Material: `Zinkdruckguss`
-   Maße hängen direkt am Material-Stammdatensatz.

------------------------------------------------------------------------

### v1.18.1

#### 🐛 Behoben

-   Navigation und Übergänge zwischen den neuen Komfortfunktionen
    stabilisiert.

------------------------------------------------------------------------

### v1.18.0

#### ✨ Neu

-   **Globale Schnellsuche** eingeführt.
-   Favoriten für häufig verwendete Materialien ergänzt.
-   Schnellzugriff auf Bestandsänderungen.
-   Undo-Funktion für geeignete Aktionen.
-   Komfortfunktionen für Einkauf und Produktion ergänzt.
-   Materialübersicht für schnellere tägliche Arbeitsabläufe erweitert.

------------------------------------------------------------------------

## 📊 v1.17 -- Verbrauch & Auswertung

### v1.17.0

#### ✨ Neu

-   Bestandsbewegungen um echte **Verbrauchsvorgänge** erweitert.
-   Materialverbrauch kann differenzierter ausgewertet werden.
-   Produktions- und Verbrauchsbewegungen bilden eine Grundlage für
    spätere Statistiken.
-   Demo-Daten wurden um realistische Verbrauchsbewegungen ergänzt.

------------------------------------------------------------------------

## 🧾 v1.16 -- Bestandsbewegungen

### v1.16.0

#### ✨ Neu

-   Strukturierte **Bestandsbewegungen** eingeführt.
-   Veränderungen des Materialbestands können nachvollziehbarer
    dokumentiert werden.
-   Grundlage für Verbrauchs-, Produktions- und Korrekturhistorien
    geschaffen.
-   Bestehende Daten werden beim Upgrade ergänzt, ohne vorhandene
    Bestände zu verlieren.

------------------------------------------------------------------------

## 📦 v1.15 -- Chargen & Einkaufskomfort

### v1.15.2

#### 🔄 Verbessert

-   Einkaufserfassung und Bestandsverwaltung weiter aufeinander
    abgestimmt.
-   Sicherungs- und Importabläufe an die erweiterten Datenstrukturen
    angepasst.

------------------------------------------------------------------------

### v1.15.1

#### 🔄 Verbessert

-   Chargen- und Lagerdaten weiter stabilisiert.
-   Export/Sicherung an die erweiterten Bestandsinformationen angepasst.

------------------------------------------------------------------------

### v1.15.0

#### ✨ Neu

-   Chargenbezogene Bestandsverwaltung erweitert.
-   Warenzugänge können differenzierter mit Lagerinformationen geführt
    werden.
-   Einstellungen für Chargen- und Lagerortverwaltung ergänzt.
-   Einkauf und Lagerbestand stärker miteinander verzahnt.

------------------------------------------------------------------------

## 🛡️ v1.14 -- Auswertungen & Datensicherheit

### v1.14.1

#### ✨ Neu

-   Zusätzliche Sicherheitsmechanismen für lokale Daten eingeführt.
-   Sicherheits-Snapshot des aktuellen Datenbestands.
-   Selbstprüfung wichtiger Anwendungsdaten.
-   Sicherungsstatus und Wiederherstellungsinformationen verbessert.

#### 🔄 Verbessert

-   Datensicherung um Versions- und Schemainformationen erweitert.

------------------------------------------------------------------------

### v1.14.0

#### ✨ Neu

-   Neuer **Auswertungsbereich**.
-   Übersichten für unter anderem:
    -   Kategorien
    -   Lieferanten
    -   Lagerorte
    -   Datenqualität
    -   niedrige Bestände
-   Kennzahlen und Bestandsinformationen werden zentral zusammengeführt.

------------------------------------------------------------------------

## 🧮 v1.13 -- Produkte & Kalkulation

### v1.13.4

#### ✨ Neu

-   Produktkonfiguration weiter ausgebaut.
-   Unterschiedliche Verschluss- bzw. Ausstattungsvarianten können bei
    Produkten und Materialbedarf berücksichtigt werden.
-   Stücklisten reagieren flexibler auf Produktvarianten.

------------------------------------------------------------------------

### v1.13.3

#### ✨ Neu

-   Variantenlogik für Produkte erweitert.
-   Materialbedarf kann abhängig von Produktkonfigurationen gesteuert
    werden.

------------------------------------------------------------------------

### v1.13.2

#### ✨ Neu

-   **Variable Produktmaße** eingeführt.
-   Eigene Variablen können für Produkte definiert werden.
-   Materialmengen können anhand von Produktmaßen dynamisch berechnet
    werden.
-   Einheiten wie `mm`, `cm` und `m` können berücksichtigt werden.

------------------------------------------------------------------------

### v1.13.1

#### ✨ Neu

-   Zuschnittberechnung für Teilstücke erweitert.
-   Tatsächliche und nutzbare Maße können unterschieden werden.
-   Herstellbarkeit eines Produkts berücksichtigt verfügbare Teilstücke
    und benötigte Zuschnittmaße.

------------------------------------------------------------------------

### v1.13.0

#### ✨ Neu

-   Eigenständiger Bereich **Produkte** eingeführt.
-   Stücklisten für Produkte.
-   Materialkostenberechnung.
-   Arbeitskosten und Kalkulationsparameter.
-   Berechnung von Produktkosten.
-   Prüfung der Herstellbarkeit anhand verfügbarer Materialien.
-   Picklisten und Fehlmengen für geplante Produktionsmengen.
-   Materialsuchen innerhalb größerer Lagerbestände.

------------------------------------------------------------------------

## ✂️ v1.12 -- Teilstücke & Materialeigenschaften

### v1.12.9

#### 🎨 Oberfläche

-   Zusätzliche Materialinformationen auf den Karten ergänzt.
-   Wichtige Metadaten werden bereits in der Übersicht schneller
    sichtbar.

------------------------------------------------------------------------

### v1.12.7

#### ✨ Neu

-   Neue Stammdaten für **Material/Werkstoff** und **Form**.
-   Material beschreibt den Werkstoff eines Lagerartikels,
    beispielsweise `Zinkdruckguss`.
-   Durchsuchbare Auswahlfelder mit direkter Neuanlage neuer Stammdaten.
-   Bestehende Materialien werden verlustfrei um die neuen Referenzen
    ergänzt.

------------------------------------------------------------------------

### v1.12.0

#### ✨ Neu

-   Verwaltung von **Teilstücken** eingeführt.
-   Reststücke können mit eigenen Abmessungen erfasst werden.
-   Länge und Fläche können ausgewertet werden.
-   Teilstücke können Warenzugängen bzw. Lagerorten zugeordnet werden.
-   Wert eines Teilstücks kann auf Basis des ursprünglichen Materials
    berechnet werden.

------------------------------------------------------------------------

## 🛒 v1.11 -- Einkauf & Warenzugänge

### v1.11.4

#### 🔄 Verbessert

-   Bestand setzt sich nachvollziehbar aus dokumentierten Warenzugängen
    und manuellen Korrekturen zusammen.
-   Direkte Bestandsbearbeitung bleibt möglich, ohne Einkaufshistorien
    zu zerstören.
-   Bei vorhandenen Warenzugängen kann der Einkaufspreis aus diesen
    Beständen abgeleitet werden.
-   Speichervorgänge wurden vereinheitlicht und stabilisiert.

------------------------------------------------------------------------

### v1.11.0

#### ✨ Neu

-   Eigenständiger Bereich **Einkäufe** eingeführt.
-   Bestellungen können mit Lieferant, Datum, Bestellnummer und Notizen
    erfasst werden.
-   Mehrere Materialpositionen pro Einkauf.
-   Menge, Preis und Lagerort je Position.
-   Warenzugänge aktualisieren den Materialbestand.
-   Einkaufsinformationen fließen in die Materialhistorie ein.
-   Navigation um den Einkaufsbereich erweitert.

------------------------------------------------------------------------

## 🔢 v1.10 -- Mengen & Preise

### v1.10.1

#### ✨ Neu

-   Erweiterte Mengen- und Preislogik für Warenzugänge.
-   Gebinde, Gesamtpreise und Einheitspreise können differenzierter
    verarbeitet werden.
-   Einheitsschrittweiten berücksichtigen unterschiedliche
    Materialeinheiten.

#### 🔎 Prüfung

-   Lokale Prüfung hinterlegter Bezugslinks auf formal gültige
    Webadressen ergänzt.

------------------------------------------------------------------------

### v1.10.0

#### ✨ Neu

-   Mengenlogik für unterschiedliche Einheiten erweitert.
-   Grundlage für Gebinde- und Einkaufspreisberechnungen geschaffen.

------------------------------------------------------------------------

## 🗃️ v1.9 -- Lagerstruktur & Bezugsquellen

### v1.9.0

#### ✨ Neu

-   Materialien können mehrere **Bezugsquellen** besitzen.
-   Eine Bezugsquelle kann als bevorzugt markiert werden.
-   Lieferanteninformationen, Artikelnummern, Preise und Links können
    strukturiert zugeordnet werden.
-   Lagerorte können hierarchisch organisiert werden.
-   Bestände und Materialwerte berücksichtigen die erweiterte
    Lagerstruktur.

------------------------------------------------------------------------

## 💾 v1.7 -- Medien & lokale Datenhaltung

### v1.7.6

#### 🐛 Behoben

-   Bildspeicherung grundlegend stabilisiert.
-   Originalbilder werden nur bei Bedarf geladen.
-   Große Bildbestände belasten den Arbeitsspeicher deutlich weniger.
-   Medien werden zuverlässiger gemeinsam mit Materialdaten gespeichert.

------------------------------------------------------------------------

### v1.7.2

#### 🔄 Verbessert

-   Export und Datensicherung an die erweiterte lokale Datenhaltung
    angepasst.

------------------------------------------------------------------------

### v1.7.0

#### ✨ Neu

-   Lokale Datenhaltung und Medienverwaltung weiter ausgebaut.
-   Bestehende Daten aus älteren Versionen können in die neue
    Speicherung übernommen werden.
-   Werkzeuge für Sicherung und Wiederherstellung erweitert.

------------------------------------------------------------------------

## ⚙️ v1.6 -- Stammdatenverwaltung

### v1.6.0

#### ✨ Neu

-   Einstellungen zu einer echten **Stammdatenverwaltung** ausgebaut.
-   Zentrale Verwaltung für:
    -   Kategorien
    -   Lieferanten
    -   Lagerorte
    -   Farben
    -   Einheiten
-   Stammdaten können gesucht und bearbeitet werden.
-   Verknüpfte Materialien bleiben bei Änderungen referenziert.
-   Grundlage für spätere Umbenennung, Zusammenführung und strukturierte
    Referenzen geschaffen.

------------------------------------------------------------------------

## 🌱 v1.2 -- Ausbau der Materialverwaltung

### v1.2.0

#### ✨ Neu

-   Materialverwaltung funktional erweitert.
-   Übersichten und Materialdialoge stärker miteinander verzahnt.
-   Grundlage für die späteren Lager-, Lieferanten- und
    Stammdatenfunktionen geschaffen.

------------------------------------------------------------------------

## 🧩 v1.1 -- Referenzen & Datenmodell

### v1.1.0

#### ✨ Neu

-   Materialdaten stärker auf wiederverwendbare Referenzen umgestellt.
-   Kategorien und weitere Stammdaten können konsistenter mit
    Materialien verknüpft werden.
-   Neue Werte können direkt während der Materialbearbeitung ergänzt
    werden.
-   Import älterer Datenbestände wurde an das erweiterte Modell
    angepasst.

------------------------------------------------------------------------

## 🌿 v0.9 -- Grundversion

### v0.9.0

#### ✨ Grundlage

-   Erste nutzbare Version von LilyStudio.
-   Browserbasierte Materialverwaltung.
-   Materialien mit grundlegenden Informationen wie:
    -   Name
    -   Kategorie
    -   Farbe
    -   Größe
    -   Einheit
    -   Bestand
    -   Meldebestand
    -   Lagerort
    -   Lieferant
    -   Einkaufspreis
    -   Bezugslink
    -   Artikelnummer
    -   Notizen
-   Materialbilder und Hauptbild.
-   Materialübersicht mit Karten.
-   Filterung und Sortierung.
-   Kennzeichnung niedriger Bestände.
-   Lokale Sicherung der LilyStudio-Daten.

------------------------------------------------------------------------

## 📌 Versionsübersicht

  -----------------------------------------------------------------------
  Bereich                             Schwerpunkt
  ----------------------------------- -----------------------------------
  **v0.9 -- v1.7**                    Materialverwaltung, Stammdaten &
                                      lokale Datenhaltung

  **v1.9 -- v1.12**                   Lager, Bezugsquellen, Einkauf &
                                      Teilstücke

  **v1.13 -- v1.15**                  Produkte, Kalkulation, Auswertungen
                                      & Chargen

  **v1.16 -- v1.17**                  Bestandsbewegungen & Verbrauch

  **v1.18**                           Bedienkomfort & Massenbearbeitung

  **v1.19**                           Hierarchische Kategorien &
                                      Navigation

  **v1.20**                           Nachbestellmanagement
  -----------------------------------------------------------------------

------------------------------------------------------------------------

> **Hinweis:** LilyStudio befindet sich in aktiver Entwicklung.
> Funktionen und Benutzeroberfläche werden kontinuierlich anhand der
> praktischen Nutzung weiterentwickelt.
