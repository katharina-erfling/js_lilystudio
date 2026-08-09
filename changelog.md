# 📝 LilyStudio -- Changelog

Alle wichtigen Änderungen und Entwicklungsschritte von **LilyStudio**.

> LilyStudio wird iterativ anhand realer Arbeitsabläufe
> weiterentwickelt.\
> Der Changelog dokumentiert Funktionen, Verbesserungen und
> Fehlerbehebungen, ohne interne Implementierungsdetails offenzulegen.

------------------------------------------------------------------------
## v1.33.3

### 🔄 Verbessert
- Der Schnellbestand auf den Materialkarten reagiert jetzt unmittelbar auf Plus- und Minus-Klicks.
- Schnelle Bestandsänderungen werden beim Speichern gebündelt, sodass die Oberfläche nicht mehr verzögert reagiert und Klicks scheinbar „nachholt“.
- Beim Anlegen eines neuen Materials wird keine Kategorie mehr automatisch vorausgewählt.

### 🐛 Behoben
- Mehrfaches Klicken auf die Bestandsbuttons konnte durch die verzögerte Rückmeldung unbeabsichtigt zu größeren Bestandsänderungen führen.

## v1.33.2

### 🐛 Behoben
- Die Dashboard-Zähler „Ohne Shop-Link“ und „Ohne Preis“ verwenden jetzt dieselbe Datenqualitätslogik wie die zugehörigen Materialfilter.
- Ausnahmen wie „Unbekannte Herkunft“ werden dadurch sowohl beim Zählen als auch beim Anzeigen der Treffer identisch berücksichtigt.
- Die angezeigte Anzahl stimmt damit wieder mit den tatsächlich geöffneten Materialien überein.

## v1.33.1

### ✨ Neu
- Bei mehreren Materialseiten gibt es jetzt zusätzlich oberhalb der Materialkarten eine kompakte Paginierung.
- Die obere Navigation zeigt dezent die aktuelle Seite und ermöglicht direktes Vor- und Zurückblättern, ohne erst bis ans Ende der Übersicht scrollen zu müssen.

### 🔄 Verbessert
- Die ausführliche Paginierung am Seitenende bleibt unverändert bestehen; die neue obere Variante ist bewusst platzsparender gestaltet.

## v1.33.0

### 🐛 Behoben
- Die rote Nullbestands-Umrandung wird jetzt dem tatsächlich sichtbaren Material zugeordnet.
- Materialien mit vorhandenem Bestand konnten nach Seitenwechseln oder Filterungen noch fälschlicherweise wie 0-Bestand markiert werden.
- Nullbestands-Markierung und Prioritätsdarstellung sind damit wieder sauber voneinander getrennt.

## v1.32.9

### 🐛 Behoben
- Bestands- und Prioritätsmarkierungen werden jetzt dem tatsächlich sichtbaren Material zugeordnet.
- Materialien mit vorhandenem Bestand konnten fälschlicherweise als Nullbestand rot hervorgehoben werden.
- Die Ursache war eine unterschiedliche Paginierung zwischen Materialkarten und nachträglichen Statusmarkierungen.
- Niedrige und sehr niedrige Nachbestellprioritäten behalten ihre bewusst zurückhaltende Darstellung.

## v1.32.8

### 🐛 Behoben
- Die Materialkarten verwenden jetzt wieder dieselbe Paginierung wie die Trefferliste.
- Bei größeren Kategorien wurden zuvor auf jeder Seite erneut die ersten Materialien dargestellt.
- Dadurch wirkte es beispielsweise so, als würde „Alle Beschläge“ nur Doppelstegschnallen enthalten, obwohl weitere Unterkategorien bereits korrekt gefiltert wurden.
- Seitenwechsel zeigen nun tatsächlich die Materialien der jeweiligen Seite.

### v1.32.3

#### 🐛 Behoben
- Schnelländerung des Materialbestands auf den Karten war verschwunden.
- Materialien mit Lieferant „Unbekannte Herkunft“ wurden fälschlich unter „Ohne Preis“ aufgeführt.

#### 🔄 Verbessert
- Bestand kann wieder direkt in der Materialübersicht über − / + geändert werden.
- Einkaufspreis startet bei neuen Materialien leer statt mit `0`.
- Regulärer Preis startet ebenfalls leer statt mit `0`.
- Gespeicherte `0`-Preise werden im Eingabefeld leer dargestellt.
- „Ohne Preis“ berücksichtigt nur Materialien, bei denen tatsächlich ein Preis erwartet wird.

### v1.32.2

#### 🐛 Behoben
- Datenqualitätsfilter wurden vom finalen Materialkarten-Renderer ignoriert.
- Dadurch konnten Trefferzahl und angezeigte Materialkarten voneinander abweichen.
- „Ohne Lieferant“ zeigt jetzt ausschließlich Materialien ohne Lieferant.
- „Ohne Preis“ berücksichtigt den tatsächlich aktuellen Einkaufspreis aus der bevorzugten Bezugsquelle.
- Filterchip, Trefferzahl und Kartenansicht verwenden nun dieselbe Filterlogik.

### v1.32.1

#### 🐛 Behoben
- Standardsortierung war durch einen JavaScript-Fehler praktisch deaktiviert.
- Materialkarten wurden unterhalb der Nachbestellliste erneut eingeblendet.
- Drilldowns „ohne Lieferant“ und „ohne Preis“ zeigten fälschlich den gesamten Materialbestand.
- Datenqualitäts-Drilldowns wurden auf die vorhandene Filterlogik vereinheitlicht.

#### 🔄 Sortierung
- Kategorie
- Name
- Material
- Farbe
- Größe
- Form
- Artikelnummer

## v1.32.0

### ✨ Neu
- Neues Materialfeld „Bruchlast“ im oberen Materialstamm.
- Bruchlast wird dauerhaft gespeichert und in Sicherungen berücksichtigt.
- Bruchlast kann über die Materialsuche gefunden werden.

### 🔄 Verbessert
- Standardsortierung innerhalb einer Kategorie: Name → Material → Farbe → Größe.
- Materialien mit gleichem Namen werden dadurch sinnvoll nach Materialart gruppiert.
- Bruchlast wird bei vorhandener Angabe kompakt in den Material-Metadaten angezeigt.

### 🐛 Behoben
- Materialbilder konnten nach dem Speichern mehrfach kurz flackern.
- Mehrere unmittelbar aufeinanderfolgende Render-Vorgänge beim Speichern werden jetzt zu einem finalen Render zusammengefasst.

### v1.31.7

#### 🐛 Behoben
- Nachbestellprioritäten wurden auf Materialkarten teilweise weiterhin wie normale Nachbestellungen dargestellt.
- Ältere Karten-Renderer konnten die Prioritätsdarstellung nachträglich überschreiben.

#### 🔄 Verbessert
- Priorität wird jetzt direkt beim Erzeugen jeder Materialkarte berücksichtigt.
- „Niedrig“ und „Sehr niedrig“ erhalten einen deutlich ruhigeren Status-Tag.
- Abweichende Prioritäten werden direkt im Tag benannt.

### v1.31.6

#### 🔄 Verbessert
- Nachbestellprioritäten werden jetzt auch auf den Materialkarten berücksichtigt.
- „Niedrig“ und „Sehr niedrig“ werden auf der Materialübersicht bewusst zurückhaltender dargestellt.
- Der Nachbestell-Tag zeigt bei abweichender Priorität zusätzlich die Prioritätsstufe an.
- Normale Priorität behält den kompakten Tag „Nachbestellen“.

### v1.31.5

#### 🐛 Behoben
- Die Nachbestellpriorität wurde beim Speichern eines Materials teilweise nicht dauerhaft übernommen.
- Status, Priorität und Nachbestellnotiz werden jetzt gemeinsam nach Abschluss der gesamten Material-Speicherkette abgesichert.
- Prioritätsänderungen direkt in der Nachbestellliste werden zusätzlich unmittelbar persistent gespeichert.

### v1.31.4

#### 🔄 Verbessert
- Nachbestellungen mit Priorität „Niedrig“ werden optisch zurückhaltender dargestellt.
- „Sehr niedrige“ Prioritäten sind noch stärker entschärft und wirken weniger dringlich.
- Beim Hover werden auch niedrige Prioritäten wieder vollständig hervorgehoben.

#### 💾 Datensicherung
- Mehrere Sicherungen am selben Tag erhalten automatisch fortlaufende Dateinamen.
- Erste Sicherung: `...-2026-08-09.json`
- Weitere Sicherungen: `...-2026-08-09-1.json`, `...-2.json` usw.
- Der Tageszähler bleibt auch nach einem Neuladen erhalten.

### v1.31.1

#### ✨ Neu
- Bestandsfelder unterstützen Mausrad-Eingaben.
- Mausrad-Steuerung funktioniert in Einzelmaterial, Sammelbearbeitung und Tabellenbearbeitung.
- Bestandswerte werden nur verändert, wenn das jeweilige Eingabefeld aktiv fokussiert ist.

#### 🐛 Behoben
- Der Status „Nicht nachbestellen“ wurde auf Materialkarten nicht mehr angezeigt.
- Status-Badges für „Zurückgestellt“ und „Nicht mehr verfügbar“ werden ebenfalls wieder dargestellt.

#### 🔄 Verbessert
- Nachbestellstatus und tatsächlicher Meldebestand werden auf Materialkarten wieder eindeutig unterschieden.

## v1.31.0

### 🌳 Kategorien & Meldebestand
- Meldebestände werden entlang der Hauptkategorie-Hierarchie vererbt.
- Unterkategorien übernehmen standardmäßig den Meldebestand ihrer übergeordneten Kategorie.
- Für Unterkategorien kann bewusst ein abweichender eigener Meldebestand festgelegt werden.
- Meldebestände werden niemals addiert.
- Individuelle Meldebestände am Material überschreiben weiterhin den Kategorie-Standard.
- In den Stammdaten wird angezeigt, von welcher Kategorie ein Meldebestand übernommen wird.

### 🔄 Schnellfilter
- Die bisherige Chip-Liste für sämtliche Unterkategorien wurde entfernt.
- Pro Hauptbereich bleibt nur noch „Alle <Hauptkategorie>“ direkt sichtbar.
- Unterkategorien werden über einen kompakten Dropdown-Picker geöffnet.
- Der Picker ist durchsuchbar und bei langen Kategoriehierarchien scrollbar.
- Eine ausgewählte Unterkategorie erscheint als einzelner aktiver Filter-Chip.
- Der aktive Unterkategorie-Filter kann direkt über × entfernt werden.

### v1.30.6

#### 🐛 Behoben
- Die Auswahlcheckboxen der Mehrfachauswahl verschwanden nach dem Rendern der Materialkarten.
- Die Mehrfachauswahl wird jetzt nach dem endgültigen Kartenaufbau zuverlässig wieder eingeblendet.

#### ✨ Neu
- Mehrere Kategorien können jetzt auch in der Sammelbearbeitung zugewiesen werden.
- Die Sammelbearbeitung verwendet einen hierarchischen Kategorie-Picker mit Checkboxen.
- Kategorien können dort durchsucht und direkt neu angelegt werden.
- Die Tabellenbearbeitung unterstützt ebenfalls Mehrfachkategorien pro Material.
- Kategorieauswahl in der Tabellenansicht ist als kompakter aufklappbarer Picker in die Tabellenzelle integriert.
- Auch aus der Tabellenbearbeitung können neue Kategorien angelegt werden.

#### 🔄 Verbessert
- Kategoriehierarchien werden in beiden Massenbearbeitungen vollständig angezeigt.
- Lange Kategorielisten sind scrollbar.
- Mehrfachkategorien bleiben mit der bisherigen primären Kategorie kompatibel.

### v1.30.5

#### 🔄 Verbessert
- Der Kategorie-Filter auf der Materialübersicht ist jetzt kontextabhängig.
- Innerhalb einer Hauptkategorie werden nur deren Unterkategorien angeboten.
- „Alle Kategorien“ bleibt ausschließlich im globalen Modus „Alle Materialien“ verfügbar.
- Breadcrumb und Kategorie-Filter bleiben dadurch logisch miteinander synchron.
- Beim Wechsel zwischen Hauptkategorien werden alte Kategorie-Filter automatisch zurückgesetzt.
- Verschachtelte Kategorien werden kompakt eingerückt angezeigt.

#### 🐛 Behoben
- Materialien konnten trotz Navigation innerhalb einer Hauptkategorie über den Filter in einen völlig anderen Kategoriebaum wechseln.
- Der Materialzähler bzw. Leerzustand konnte dadurch fälschlich `0 Materialien` anzeigen.

### v1.30.4

#### 🐛 Behoben
- Kategorien konnten intern vorhanden sein, aber in den Stammdaten vollständig ausgeblendet werden.
- Dadurch meldete LilyStudio beim Anlegen einer Kategorie „existiert bereits“, obwohl der Eintrag nicht auffindbar war.
- Die Dublettenprüfung bei Kategorien berücksichtigte die Kategoriehierarchie nicht korrekt.

#### 🌳 Kategorien
- Inaktive Kategorien bleiben in den Stammdaten sichtbar und werden als „inaktiv“ gekennzeichnet.
- Verwaiste Kategorien werden ebenfalls angezeigt und entsprechend markiert.
- Dubletten werden nur noch innerhalb derselben übergeordneten Kategorie geprüft.
- Ein vorhandener inaktiver/verwaister Eintrag kann beim Speichern automatisch reaktiviert werden.

### v1.30.3

#### 🐛 Behoben
- Neue Kategorien konnten im Materialdialog eingegeben werden, wurden aber nicht zuverlässig erstellt bzw. gespeichert.
- Der Quick-Create-Handler wurde vollständig ersetzt.

#### 🔄 Verbessert
- Neue Kategorien werden sofort persistent gespeichert.
- Die neue Kategorie wird direkt im Material ausgewählt.
- Kategoriebaum, Filter und Stammdaten werden unmittelbar aktualisiert.
- Enter im Kategorien-Namensfeld legt die Kategorie direkt an.

### v1.30.2

#### 🐛 Behoben
- Kategorie-Drag-&-Drop startete trotz sichtbarem Drag-Griff nicht zuverlässig.
- Das native HTML5-Drag-&-Drop wurde für die Kategorieverwaltung vollständig ersetzt.

#### 🔄 Verbessert
- Kategorien werden jetzt per Pointer-/Maus-Drag verschoben.
- Beim Ziehen wird eine sichtbare Vorschau der Kategorie mitgeführt.
- Unterkategorie- und Hauptkategorie-Zielbereiche werden während des Ziehens hervorgehoben.

### v1.30.1

#### 🐛 Behoben
- Kategorien in den Stammdaten zeigten zwar einen Drag-Cursor, ließen sich aber nicht tatsächlich ziehen.
- Der Drag-Start wurde jetzt direkt an den dafür vorgesehenen Griff gebunden.
- Unterordnen und Zurückziehen auf die Hauptkategorie verwenden nun denselben stabilen Drag-Pfad.

## v1.30.0

### 🐛 Behoben
- Escape reagierte nach längerer Nutzung teilweise erst nach mehreren Tastendrücken.
- Mehrere alte Escape-Handler konnten gleichzeitig aktiv sein.
- Kategorie-Drag-&-Drop erlaubte das Herausziehen, aber nicht zuverlässig das Unterordnen.
- Der separate „Nach oben“-Button blieb im Materialdialog trotz vorheriger Entfernung sichtbar.
- Der reguläre Preis der bevorzugten Bezugsquelle ging nach Neuladen teilweise verloren.
- Der Bereich „Neue Kategorie anlegen“ lief im Materialdialog seitlich aus dem Popup.

### 🌳 Kategorien
- Kategorie-Drag-&-Drop vollständig neu aufgebaut.
- Die komplette Kategoriezeile kann gezogen werden.
- Während des Ziehens erscheint unter jeder Kategorie eine große Zielzone:
  `↳ Als Unterkategorie ablegen`
- Kategorien können über eine eigene Dropzone wieder zu Hauptkategorien gemacht werden.
- Der Quick-Create-Bereich im Materialdialog verwendet jetzt ein vertikales, kompaktes Layout.

### 💾 Stabilität
- Regulärpreis, Verfügbarkeitsstatus, Aktionsende und Aktionsnotiz werden direkt an der bevorzugten Bezugsquelle gespeichert.
- Gebindepreis und Gebindeinhalt werden ebenfalls dauerhaft mitgesichert.
- Der gespeicherte Materialdatensatz wird nach dem Speichern nochmals persistent abgesichert.

### ⌨️ Bedienung
- Es gibt nur noch einen zentralen globalen Escape-Handler.
- Ein Escape-Tastendruck schließt offene Hilfs-Popups und anschließend den obersten Dialog zuverlässig.

## v1.29.0

### ✨ Neu
- Browser- und Mausnavigation über Zurück/Vorwärts wird unterstützt.
- Kategorie-Icon-Picker um zahlreiche weitere voreingestellte Symbole erweitert.
- Eigene Emojis und kurze Zeichen bleiben weiterhin als individuelle Kategorie-Icons möglich.

### 🌳 Kategorien
- Drag & Drop in den Kategorie-Stammdaten wurde überarbeitet.
- Beim Ziehen erscheint an jeder Kategorie eine eindeutige Dropzone „Als Unterkategorie hier hinein“.
- Kategorien können zuverlässig anderen Kategorien untergeordnet werden.
- Das Zurückziehen auf die Ebene der Hauptkategorien bleibt möglich.
- Der Bereich zum direkten Anlegen neuer Kategorien im Materialdialog wurde übersichtlicher gestaltet.
- Name und übergeordnete Kategorie erhalten mehr Platz; der Anlegen-Button ist kompakter.

### 🐛 Behoben
- Regulärpreise wurden beim erneuten Öffnen eines Materials teilweise auf `0` zurückgesetzt.
- Nullbestand wurde auch bei Materialien hervorgehoben, die bewusst nicht nachbestellt werden sollen.
- Kategorien konnten per Drag & Drop zwar aus einer Hierarchie herausgezogen, aber nicht zuverlässig einer anderen Kategorie untergeordnet werden.

### 🔄 Verbessert
- Nullbestand wird nicht hervorgehoben bei:
  - Nicht nachbestellen
  - Zurückgestellt
  - Nicht verfügbar
  - Ausverkauft
  - Nicht mehr verfügbar
- Der separate „Nach oben“-Button im Material-Bearbeitungsdialog wurde entfernt.
- Der globale Seiten-Button bleibt für lange LilyStudio-Seiten erhalten.

## v1.28.0

### ✨ Neu
- Kategorien können einem Material per Checkbox mehrfach zugewiesen werden.
- Kategorien im Materialdialog werden hierarchisch und scrollbar dargestellt.
- Neue Kategorien können direkt beim Anlegen eines Materials erstellt werden.
- Beim Erstellen einer Kategorie kann sofort die übergeordnete Kategorie gewählt werden.
- Neue Kategorien sind anschließend unmittelbar auswählbar.
- Lieferanten können direkt aus dem Materialdialog neu angelegt werden.
- Durchsuchbarer Icon-Picker für Kategorie-Stammdaten ergänzt.
- Eigene Emojis und kurze Zeichen können weiterhin frei als Kategorie-Icon eingegeben werden.
- Betroffene Materialien unter Auswertungen → Nachbestellungen können nach Spalten sortiert werden.

### 🌳 Kategorien
- Mehrfachzuordnung von Kategorien zu Materialien ergänzt.
- Bestehende Hauptkategorie bleibt aus Kompatibilitätsgründen erhalten.
- Kategorie-Dropdowns zeigen die vollständige Hierarchie.
- Verschachtelte Kategorien werden mit vollständigem Pfad dargestellt.
- Stammdaten-Kategorien erhalten einen überarbeiteten Drag-&-Drop-Modus.
- Kategorien können vor oder nach anderen Kategorien einsortiert werden.
- Kategorien können per Drag & Drop zu Unterkategorien gemacht werden.
- Kategorien können wieder auf die oberste Ebene verschoben werden.
- Material-Schnellfilter berücksichtigen auch Mehrfachkategorien und tiefere Hierarchieebenen.

### 🔄 Verbessert
- Escape behandelt offene Picker, Vorschläge, Comboboxen und Dialoge jetzt unmittelbar und in eindeutiger Reihenfolge.
- Materialnamen in Nachbestelllisten bleiben optisch zurückhaltend.
- Kategorie-Auswahl im Materialdialog bleibt auch bei vielen Kategorien kompakt und scrollbar.
- Nachbestell-Auswertung zeigt Materialien weiterhin mit Bild und eindeutigen Merkmalen.

### 🛠️ Stammdaten
- Kategorie-Icons werden zentral in den Stammdaten gepflegt.
- Der Icon-Picker bietet eine größere durchsuchbare Auswahl für Material-, Werkzeug-, Versand-, Farb- und weitere Kategorien.

## v1.27.0

### ✨ Neu
- Globaler „Nach oben“-Button für lange LilyStudio-Seiten.
- Eigener „Nach oben“-Button für den Materialdialog.
- Mehrstufige Kategoriehierarchien werden vollständig unterstützt.
- Kategorien können in den Stammdaten per Drag & Drop verschoben und untergeordnet werden.
- Kategorien können beliebig tief verschachtelt werden, z. B.:
  - Beschläge
    - Verschlüsse
      - Doppelstegschnalle
- Alle Unterebenen stehen in der Materialansicht als Schnellfilter zur Verfügung.
- Einkaufspreise können wahlweise als Einzelpreis oder Gebindepreis erfasst werden.
- Bei Gebindepreisen wird der Einzelpreis automatisch aus Preis und Gebindeinhalt berechnet.

### 🔄 Verbessert
- Der Auswertungsreiter heißt wieder „Nachbestellungen“.
- „Betroffene Materialien“ in der Nachbestell-Auswertung orientieren sich jetzt optisch an der eigentlichen Nachbestellliste.
- Materialien werden dort mit Bild, Kategoriepfad, Materialmerkmalen und Lieferant eindeutig identifizierbar dargestellt.
- Materialnamen sind in Nachbestelllisten nicht mehr unnötig fett hervorgehoben.
- Kategorie-Schnellfilter berücksichtigen auch tiefer verschachtelte Ebenen.
- Kategoriepfade werden in den Stammdaten verständlicher dargestellt.

### 🧱 Stammdaten
- Übergeordnete Kategorien können weiterhin direkt beim Bearbeiten gewählt werden.
- Drag & Drop auf eine Kategorie verschiebt einen Eintrag innerhalb der Ebene.
- „↳ hinein“ ordnet eine Kategorie als Unterkategorie ein.
- Eine eigene Hauptkategorie-Dropzone verschiebt Kategorien wieder auf die oberste Ebene.

### v1.26.2

#### 🐛 Behoben
- „Datensicherung“ und „Sicherung laden“ wurden auf der eigentlichen Materialien-Startseite mit den Kategorie-Kacheln nicht angezeigt.

#### 🔄 Verbessert
- Sicherungsfunktionen sind jetzt sowohl auf der Materialien-Startseite als auch in der Materialliste direkt im jeweiligen Seitenkopf erreichbar.
- Die vorhandenen Sicherungsfunktionen werden abhängig von der aktuellen Materialansicht automatisch an die passende Stelle verschoben.


### v1.26.1

#### 🐛 Behoben
- Unpassender Punkt bei Materialien mit Bestand `0` entfernt.
- Auswahl des Werts `0` im Einkaufspreisfeld reagiert jetzt direkt auf Klick/Fokus.
- Escape schließt Vorschläge, Auswahlfelder und Materialdialog ohne unnötige Verzögerung.
- „Nach oben“-Button im Materialdialog erneut stabilisiert.

#### ✨ Neu
- Scrollposition der Materialübersicht wird beim Öffnen eines Artikels gemerkt und nach Schließen oder Speichern wiederhergestellt.

#### 🔄 Verbessert
- Datensicherung und „Sicherung laden“ werden direkt im Kopf der Materialübersicht angezeigt.
- Auswertungsbereich „Nachbestellungen“ heißt jetzt „Nachbestellliste“.
- Betroffene Materialien in der Nachbestell-Auswertung werden kompakter und eindeutiger dargestellt.
- Nullbestand bleibt optisch hervorgehoben, ohne zusätzliche Symbolmarkierung.

## v1.26.0

### ✨ Neu
- Materialien mit Bestand `0` werden in der Übersicht deutlich hervorgehoben.
- Shop-Links können direkt über einen kleinen Öffnen-Button neben dem Eingabefeld aufgerufen werden.
- Datensicherung und „Sicherung laden“ sind direkt im Kopf der Materialübersicht erreichbar.

### 🔄 Verbessert
- Einkaufspreis, Verfügbarkeitsstatus, Regulärpreis, Aktionsende und Aktionsnotiz wurden zu einem gemeinsamen Bereich „Einkauf & Verfügbarkeit“ zusammengeführt.
- Beim Klick in ein Einkaufspreisfeld mit Wert `0` wird die Null automatisch markiert und kann direkt überschrieben werden.
- Der „Nach oben“-Button ist im Materialdialog dauerhaft sichtbar und nicht mehr von Scroll-Schwellen oder Sichtbarkeitsberechnungen abhängig.

### 🎨 Oberfläche
- Nullbestand wird in Materialkarten dezent, aber eindeutig hervorgehoben.
- Sicherungsfunktionen sind im normalen Material-Workflow leichter erreichbar.

### v1.25.15

#### 🐛 Behoben
- Lagerort wurde trotz mehrfacher vorheriger Korrekturen weiterhin durch eine ältere interne Validierung erzwungen.
- Lagerort wurde nun direkt aus der ursprünglichen Referenzprüfung entfernt und ist tatsächlich optional.
- Der „Nach oben“-Button wurde angezeigt, reagierte aber wegen mehrerer übereinanderliegender Click-Handler nicht zuverlässig.

#### 🧹 Bereinigt
- Mehrere widersprüchliche Zwischen-Patches für Lagerort und „Nach oben“ wurden entfernt.
- Der „Nach oben“-Button verwendet jetzt nur noch einen eindeutigen Click- und Scroll-Handler.

### v1.25.14

#### 🐛 Behoben
- Lagerort wurde trotz optionalem Feld weiterhin durch die interne Referenzprüfung erzwungen.
- Ein vollständig leerer Lagerort wird jetzt korrekt als gültiger Zustand behandelt.
- Nur tatsächlich eingegebene Lagerorte müssen aus den Stammdaten ausgewählt sein.

### v1.25.11

#### 🔄 Verbessert
- Der „Nach oben“-Button wird nicht mehr über eine feste Scrollschwelle gesteuert.
- Er erscheint jetzt automatisch, sobald der obere Kopfbereich des Materialdialogs nicht mehr sichtbar ist.
- Beim Zurückscrollen zum Anfang verschwindet der Button wieder.

### v1.25.10

#### 🐛 Behoben
- Lagerort war in der Materialanlage versehentlich zum Pflichtfeld geworden.
- Materialien können wieder ohne zugewiesenen Lagerort angelegt und bearbeitet werden.

### v1.25.9

#### 🐛 Behoben
- Der Materialdialog konnte horizontal über den sichtbaren Bereich hinauslaufen.
- Dadurch wurden Felder auf der rechten Seite abgeschnitten und eine horizontale Scrollleiste eingeblendet.
- Der „Nach oben“-Button erschien im Materialdialog zu spät bzw. teilweise gar nicht sichtbar.

#### 🔄 Verbessert
- Der Materialdialog scrollt nur noch vertikal.
- Formularbereiche und Spalten passen sich zuverlässig an die verfügbare Dialogbreite an.
- Der „Nach oben“-Button erscheint bereits nach kurzem Scrollen.
- Der Button wird bei geöffnetem Materialdialog direkt innerhalb der modalen Dialogebene dargestellt.

## v1.25.8

### 🛡️ Datensicherheit
- Vollsicherungen wurden auf ein selbstprüfendes, portables Sicherungsformat umgestellt.
- Originalbilder werden vollständig in die Sicherungsdatei eingebettet.
- Temporäre `blob:`-Referenzen gelten nicht mehr als gültige Bildsicherung.
- Für jedes Bild werden Größe und SHA-256-Prüfsumme im Medien-Manifest gespeichert.
- Eine Sicherung wird abgebrochen, wenn ein hinterlegtes Originalbild nicht gelesen werden kann.
- Neue Vollsicherungen werden vor dem Import auf Vollständigkeit und Bildintegrität geprüft.
- Nach dem Import wird zusätzlich kontrolliert, ob alle Bilder erfolgreich im lokalen Bildspeicher gespeichert wurden.
- Ältere Sicherungen bleiben kompatibel; bei fehlenden eingebetteten Bildern erfolgt eine Warnung.

### 🐛 Behoben
- Originalbilder wurden nach einem Neustart im Material-Bearbeitungsdialog teilweise nicht mehr angezeigt, obwohl die Kartenansicht noch ein Vorschaubild besaß.
- Der „Nach oben“-Button war bei geöffneten modalen Dialogen durch die Browser-Dialogebene nicht sichtbar.
- Die Bestellhistorie erhielt trotz vieler Einträge nicht zuverlässig einen eigenen Scrollbereich.
- Enter- und Escape-Behandlung konnte auch auf nicht tatsächlich geöffnete Comboboxen reagieren.

### 🔄 Verbessert
- Originalbilder werden beim Öffnen eines Materials direkt aus dem lokalen Bildspeicher nachgeladen.
- Materialdialoge besitzen einen definierten Scrollbereich.
- Der dezente „Nach oben“-Button erscheint nach längerem Scrollen auch innerhalb des Materialdialogs.
- Historie und Bestellhistorie werden ab mehr als sechs Einträgen kompakt scrollbar.
- Neue Breiten werden weiterhin kategoriebasiert verwaltet und wieder über den LilyStudio-Vervollständigungsdialog ergänzt.
- Neu angelegte Material-Stammdaten werden direkt normalisiert und ausgewählt.

### v1.25.4

#### 🐛 Behoben
- Produktkarten reagierten seit v1.25.0 nicht mehr zuverlässig auf Klicks.
- Die fehlerhafte Produkt-Regression wurde durch einen Neuaufbau auf Basis der stabilen v1.24.0 entfernt.
- Enter bei Namensvorschlägen löst nicht mehr versehentlich das Speichern des Materials aus.

#### 🔄 Verbessert
- Die Änderungen aus v1.25 wurden neu isoliert umgesetzt, ohne in die Produktlogik einzugreifen.
- Breitenvorschläge in der Materialanlage werden kategoriebasiert verwaltet.
- Escape schließt Vorschläge, Auswahlfelder oder den aktuell offenen Dialog.

### v1.25.3

#### 🐛 Behoben
- Produktkarten reagierten teilweise überhaupt nicht auf Klicks.
- Der Produktdialog war zu stark von mehreren älteren Öffnungs- und Renderpfaden abhängig.

#### 🔄 Verbessert
- Produktkarten verwenden jetzt eine zentrale und robuste Klicksteuerung.
- Der Produktdialog öffnet sofort und lädt Stückliste, Varianten und Kalkulation anschließend getrennt.
- Fehler in einzelnen Produktbereichen verhindern nicht mehr das Öffnen des gesamten Produkts.

  
### v1.25.2

#### 🐛 Behoben
- Produktkarten konnten trotz des vorherigen Regression-Fixes weiterhin nicht zuverlässig geöffnet werden.
- Unvollständige ältere Produkt- oder Materialart-Daten konnten den gesamten Öffnungsvorgang abbrechen.

#### 🔄 Verbessert
- Der Produktdialog wird jetzt robuster gegen unvollständige Bestandsdaten geladen.
- Produktvarianten, Stückliste und Kalkulation werden voneinander isolierter initialisiert.
- Produktkarten werden nach dem Rendern zuverlässig mit dem aktuellen Öffnen-Handler verbunden.

### v1.25.1

#### 🐛 Behoben
- Produkte ließen sich nach dem Update auf v1.25.0 nicht mehr öffnen.
- Die neue kategoriebasierte Breitenlogik griff versehentlich auch außerhalb der Materialanlage.
- Materialbezogene Auswahl- und Vorschlagslogik ist jetzt strikt auf den Materialdialog begrenzt.

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
