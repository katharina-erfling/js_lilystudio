# 🌿 LilyStudio

> **Materialverwaltung, Einkauf, Produktion und Kalkulation für Maker und kleine kreative Unternehmen.**

LilyStudio ist eine browserbasierte All-in-One-Anwendung zur Verwaltung von **Materialien, Beständen, Einkäufen, Produkten und Produktionsabläufen**.

Das Projekt ist aus dem praktischen Bedarf entstanden, Materialverwaltung und kreative Produktion übersichtlich miteinander zu verbinden – ohne die Komplexität klassischer Warenwirtschaftssysteme.

---

## ✨ Features

### 📦 Materialverwaltung

Materialien werden nicht nur als einfacher Lagerbestand geführt, sondern können umfangreich beschrieben und organisiert werden.

- 🗂️ Kategorien & Unterkategorien
- 🧵 Materialarten
- 🎨 Farben
- 📏 Maße, Breiten & Formen
- 📍 Lagerorte
- 🔢 Artikelnummern
- 🖼️ mehrere Bilder & Hauptbild
- 📝 Notizen
- 📦 Bestand & Meldebestand
- 💰 Einkaufspreise
- 🚚 Lieferanten & Bezugsquellen

Durch **verschachtelbare Kategorien** lassen sich auch größere Materialbestände übersichtlich strukturieren.

---

### 🔎 Finden statt Suchen

LilyStudio ist darauf ausgelegt, auch bei vielen hundert oder tausend Materialien übersichtlich zu bleiben.

> **Kategorie-Kacheln** ermöglichen den schnellen Einstieg in die oberste Kategorieebene.

Unterkategorien können anschließend als **Shortcuts für die Filterung** verwendet werden, ohne sich durch mehrere Ebenen klicken zu müssen.

Zusätzlich stehen verschiedene **Filter- und Sortiermöglichkeiten** zur Verfügung.

---

### ✏️ Mehrfachbearbeitung

Viele Materialien ändern, ohne jeden Datensatz einzeln öffnen zu müssen.

LilyStudio bietet dafür zwei unterschiedliche Arbeitsweisen:

| Modus | Funktion |
|---|---|
| **Sammelbearbeitung** | Einen Wert gleichzeitig auf mehrere Materialien anwenden |
| **Tabellenbearbeitung** | Mehrere Materialien gemeinsam anzeigen und individuell bearbeiten |

Auch größere zusammenhängende Materialbereiche können komfortabel ausgewählt werden.

---

## 🛒 Nachbestellmanagement

Ein niedriger Bestand bedeutet nicht automatisch, dass ein Material sofort bestellt werden muss.

Deshalb besitzt LilyStudio ein eigenes **Nachbestellmanagement**.

### Mögliche Zustände

- 🔄 **Automatisch** – Nachbestellung anhand des Meldebestands
- ⏸️ **Zurückgestellt** – momentan bewusst nicht bestellen
- 🚫 **Nicht nachbestellen** – Material soll nicht erneut beschafft werden
- ❌ **Nicht verfügbar** – Material kann nicht mehr bestellt werden

Dadurch verschwinden bewusst nicht bestellte Materialien nicht einfach aus dem Blick.

---

### 📋 Nachbestellplanung

Offene Nachbestellungen besitzen eine eigene Arbeitsansicht.

Dort stehen unter anderem zur Verfügung:

- 🖼️ Materialvorschau
- 🧵 Material & Kategorie
- 🚚 Lieferant
- 📦 Bestand / Meldebestand
- 🚦 mehrstufige Priorität
- 📝 individuelle Bestellnotizen
- 🔎 Filter
- 🗂️ Gruppierungen
- ↕️ sortierbare Tabellenspalten
- 🖱️ Drag & Drop zur manuellen Priorisierung
- 📄 eigene Seitennavigation für größere Bestelllisten

Die Nachbestellliste ist damit nicht nur eine Warnanzeige, sondern dient als **aktive Einkaufsplanung**.

---

## 🚚 Einkauf & Bezugsquellen

Materialien können mit ihren bevorzugten Lieferanten und Bezugsquellen verbunden werden.

Dabei lassen sich unter anderem Informationen zu

- Lieferant
- Artikelnummer
- Einkaufspreis
- Bezugsquelle
- Bestellungen

hinterlegen und miteinander verknüpfen.

Eine **Bestell- und Bestandshistorie** macht vergangene Bewegungen nachvollziehbar.

---

## 🏭 Produkte & Produktion

LilyStudio endet nicht beim Materiallager.

Die Anwendung verbindet die Materialverwaltung mit den daraus entstehenden Produkten und Produktionsabläufen.

```text
Material
   ↓
Einkauf
   ↓
Bestand
   ↓
Produkt
   ↓
Produktion
   ↓
Kalkulation
```

Die einzelnen Bereiche bleiben dabei eigenständig, greifen aber auf eine gemeinsame Materialbasis zurück.

---

## 🧮 Kalkulation

Materialpreise und weitere Kosten können für die Kalkulation eigener Produkte genutzt werden.

Ziel ist es, nicht nur zu wissen:

> **„Was habe ich auf Lager?“**

sondern auch:

> **„Was kostet mich das Produkt tatsächlich?“**

Damit entwickelt sich LilyStudio von einer reinen Inventarverwaltung zu einer Arbeitsumgebung für den gesamten Herstellungsprozess.

---

## 🎯 Warum LilyStudio?

Viele bestehende Systeme sind für kleine kreative Unternehmen entweder

- zu umfangreich,
- zu unflexibel,
- auf klassische Handelsunternehmen ausgelegt
- oder mit laufenden Kosten verbunden.

LilyStudio verfolgt deshalb einen anderen Ansatz:

> ### Eine übersichtliche und flexibel erweiterbare Arbeitsumgebung, die sich an den tatsächlichen Abläufen kleiner Produktions- und Kreativbetriebe orientiert.

Neue Funktionen entstehen dabei nicht nur anhand eines theoretischen Feature-Katalogs, sondern vor allem aus **konkreten Anforderungen im täglichen Einsatz**.

---

## 🛠️ Tech Stack

| Technologie | Einsatz |
|---|---|
| **HTML5** | Struktur & Benutzeroberfläche |
| **CSS3** | Layout, Responsive Design & UI |
| **Vanilla JavaScript** | Anwendungslogik |
| **Browser APIs** | lokale Datenhaltung & Interaktionen |
| **Drag & Drop API** | Sortierung & Priorisierung |

### Ohne Frontend-Framework

LilyStudio wird bewusst ohne React, Vue, Angular oder vergleichbare Frontend-Frameworks entwickelt.

```text
HTML  •  CSS  •  Vanilla JavaScript
```

---

## 🚧 Entwicklungsstand

> 🟢 **Aktive Entwicklung**

LilyStudio wird kontinuierlich erweitert und im praktischen Einsatz getestet.

Der Fokus liegt aktuell insbesondere auf:

- Materialverwaltung
- großen Materialbeständen
- Einkaufs- & Nachbestellmanagement
- Produkten
- Produktion
- Kalkulation
- komfortabler Massenbearbeitung
- übersichtlichen Workflows

Änderungen und neue Funktionen werden im **Changelog** dokumentiert.

---

## 🗺️ Roadmap

LilyStudio soll schrittweise um weitere Funktionen ergänzt werden.

```text
✓ Materialverwaltung
✓ Stammdaten
✓ Kategorien & Unterkategorien
✓ Bestandsverwaltung
✓ Einkauf
✓ Nachbestellmanagement
✓ Mehrfachbearbeitung

↻ Produkte
↻ Produktion
↻ Kalkulation
↻ Auswertungen
↻ weitere Workflow-Optimierungen
```

> Die Roadmap entwickelt sich gemeinsam mit den Anforderungen aus der praktischen Nutzung weiter.

---

## 🔒 Quellcode

Dieses Repository dient derzeit in erster Linie der **Dokumentation und Präsentation von LilyStudio und seiner Entwicklung**.

Der vollständige Quellcode ist **nicht öffentlich verfügbar**.

Veröffentlicht werden unter anderem:

- 📖 Projektdokumentation
- 📋 Features
- 📝 Changelog / Patch Notes
- 🖼️ ausgewählte Screenshots
- 🗺️ Entwicklungsfortschritt

Interne Implementierungsdetails und die vollständige Anwendungslogik bleiben privat.

---

## 📌 Projektstatus

**🌿 LilyStudio**  
`Active Development` · `HTML5` · `CSS3` · `Vanilla JavaScript`

---

*LilyStudio is an independent software project in active development.*
