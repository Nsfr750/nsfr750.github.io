---
lang: de
lang-niv: fonto
lang-ref: 019-jbk
layout: doc
order: 9
title: 'PDF Finder'
---

# PDF-Duplikatfinder

[![Lizenz: GPL v3](https://img.shields.io/badge/Lizenz-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Code-Stil: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Ein leistungsstarkes Werkzeug zum Finden und Verwalten doppelter PDF-Dateien auf Ihrem Computer. Der PDF-Duplikatfinder hilft Ihnen, doppelte PDF-Dokumente zu identifizieren und zu entfernen, um Speicherplatz zu sparen und Ihre Dateien effizienter zu organisieren.

## ✨ Funktionen

- 🔍 **Intelligenter PDF-Vergleich**: Finden Sie doppelte PDFs basierend auf dem Inhalt, nicht nur nach Dateinamen oder -größen
- 📝 **Textbasierter Vergleich**: Identifizieren Sie Duplikate auch bei geringfügigen visuellen Unterschieden durch fortschrittliche Textanalyse
- 👁 **Integrierter PDF-Viewer**: Betrachten Sie PDFs direkt in der Anwendung
- 📋 **Zweigeteilte Benutzeroberfläche**: Zeigen Sie sowohl die Dateiliste als auch Duplikatgruppen in separaten Tabs an
- 🎯 **Erweiterte Filterung**: Filtern Sie nach Dateigröße, Änderungsdatum und Namensmustern
- 🚀 **Schnelles Scannen**: Optimierte Algorithmen für schnelles Scannen großer PDF-Sammlungen
- 🎨 **Intuitive Benutzeroberfläche**: Übersichtliche und benutzerfreundliche Oberfläche mit Unterstützung für Hell/Dunkel-Designs
- 🔄 **Stapelverarbeitung**: Verarbeiten Sie mehrere Dateien oder ganze Ordner auf einmal
- 📊 **Detaillierte Analyse**: Zeigen Sie Dateidetails, Vorschauen und Vergleichsergebnisse an
- 🛠 **Erweiterte Werkzeuge**: Mehrere Auswahlmodi, Filter- und Sortieroptionen
- 🌍 **Mehrsprachige Unterstützung**: In mehreren Sprachen verfügbar
- 📊 **Fortschrittsverfolgung**: Echtzeit-Fortschrittsbalken für Dateiverarbeitungsvorgänge
- ⏱ **Zuletzt geöffnet**: Schneller Zugriff auf zuletzt geöffnete Dateien mit Kontextmenüoptionen

## 📦 Installation

### Voraussetzungen

- Python 3.8 oder höher
- pip (Python-Paketmanager)
- Optionale Backends für das PDF-Rendering (automatischer Fallback bei Fehlschlagen):
  - PyMuPDF (fitz) — Standard und in den Anforderungen enthalten
  - Ghostscript (für Wand) — Installieren Sie Ghostscript und legen Sie den ausführbaren Pfad in den Einstellungen fest

Siehe [VORAUSSETZUNGEN.md](VORAUSSETZUNGEN.md) für plattformspezifische Einrichtung.

### Installation aus dem Quellcode

1. Klonen Sie das Repository:

   ```bash
   git clone https://github.com/Nsfr750/PDF_finder.git
   cd PDF_finder
   ```

2. Erstellen und aktivieren Sie eine virtuelle Umgebung (empfohlen):

   ```bash
   python -m venv venv
   .\venv\Scripts\activate  # Windows
   source venv/bin/activate  # Linux/Mac
   ```

3. Installieren Sie die erforderlichen Abhängigkeiten:

   ```bash
   pip install -r requirements.txt
   ```

## Verwendung

1. Starten Sie die Anwendung:

   ```bash
   python main.py
   ```

2. Klicken Sie auf "Ordner durchsuchen", um ein Verzeichnis für die Suche nach doppelten PDFs auszuwählen.

3. Überprüfen Sie die Ergebnisse im Hauptfenster. Nach Abschluss eines Scans wird die Dateiliste automatisch mit den gescannten PDFs und Duplikatgruppen gefüllt.

4. Verwenden Sie die Werkzeuge zum Verwalten von Duplikaten:
   - Markieren Sie zu behaltende Dateien
   - Löschen Sie unerwünschte Duplikate
   - Zeigen Sie Vorschauen der Dateien an, bevor Sie Aktionen durchführen

## Wichtige Funktionen im Detail

### Intelligenter PDF-Vergleich

- Vergleicht PDF-Inhalte mit fortschrittlichen Hash-Algorithmen
- Erkennt ähnliche Dokumente auch bei unterschiedlichen Dateinamen oder Metadaten
- Konfigurierbarer Ähnlichkeitsschwellenwert für optimale Ergebnisse

### Leistungsoptimierungen

- Multithread-Scanning für schnelleres Verarbeiten
- Speichereffiziente Handhabung großer PDF-Dateien
- Fortschrittsverfolgung und Abbruchmöglichkeit

### Benutzererfahrung

- Moderne, reaktionsschnelle Oberfläche
- Anpassbare Ansichtsoptionen
- Umfassende Tastenkombinationen
- Detaillierte Dateiinformationen und Vorschauen
- Symbolleiste mit verbessertem Abstand und besserer Lesbarkeit
- Das Einstellungsfenster enthält eine Schaltfläche "Backends testen", um die Verfügbarkeit von PyMuPDF und Ghostscript zu überprüfen

### PDF-Backends und Fallback

- Wählen Sie Ihr bevorzugtes Backend in Einstellungen → PDF-Rendering
- Verwenden Sie "Backends testen", um zu überprüfen, ob Ghostscript korrekt konfiguriert ist
- Wenn das ausgewählte Backend fehlschlägt, wechselt die Anwendung automatisch zu einem verfügbaren Backend und zeigt eine Warnung in der Statusleiste an (lokalisiert)

## Versionsverlauf

Siehe [CHANGELOG.md](CHANGELOG.md) für eine vollständige Liste der Änderungen in jeder Version.

## Mitwirken

Beiträge sind willkommen! Bitte lesen Sie unsere [Beitragsrichtlinien](CONTRIBUTING.md) für Details, wie Sie zu diesem Projekt beitragen können.

## 📄 Lizenz

Dieses Projekt ist unter der GNU General Public License v3.0 lizenziert - siehe [LIZENZ](LIZENZ) für Details.

## 🙏 Danksagungen

- Vielen Dank an alle Mitwirkenden, die zur Verbesserung des PDF-Duplikatfinders beigetragen haben
- Mit ❤️ erstellt mit Python und PyQt6

## 🐞 Bekannte Probleme

- Die Sprachauswahl funktioniert nicht

---

📅 **Letzte Aktualisierung**: August 2025  
🐍 **Python-Version**: 3.8+  
📜 **Lizenz**: GPL-3.0
