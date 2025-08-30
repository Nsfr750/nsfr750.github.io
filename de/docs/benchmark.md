---
lang: de
lang-niv: fonto
lang-ref: 023-jbk
layout: doc
order: 14 # Optional: für die Menüreihenfolge
title: 'benchmark'
---

[![Lizenz: GPL v3](https://img.shields.io/badge/Lizenz-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Code-Style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Ein modernes Python-Benchmark-Tool, das mit PySide6 entwickelt wurde und eine benutzerfreundliche Oberfläche zum Ausführen und Analysieren von Pystone- und anderen Benchmark-Tests bietet.

## 📥 Installation

### Voraussetzungen

- Python 3.9 oder höher
- Windows oder Linux

### Schnellstart

1. Repository klonen:

   ```bash
   git clone https://github.com/Nsfr750/benchmark.git
   cd benchmark
   ```

2. Virtuelle Umgebung erstellen und aktivieren:

   ```bash
   python -m venv venv
   .\venv\Scripts\activate  # Windows
   source venv/bin/activate  # Linux/Mac
   ```

3. Abhängigkeiten installieren:

   ```bash
   pip install -r requirements.txt
   ```

4. Anwendung starten:

   ```bash
   python main.py
   ```

## ✨ Funktionen

- **Moderne Benutzeroberfläche**: Saubere, reaktionsschnelle Oberfläche mit PySide6
- **Umfassendes Benchmarking**:
  - Anpassbare Testdauer
  - Echtzeit-Fortschrittsverfolgung
  - Detaillierte Ergebnisse mit Statistiken
  - Vergleich mit historischen Daten
- **Protokollierung**:
  - Detaillierte Betriebsprotokolle
  - Filterung von Protokollen nach Schweregrad
  - Protokolldatei-Rotation
- **Mehrsprachige Unterstützung**:
  - Englisch (en)
  - Italienisch (it)
- **Barrierefreiheit**:
  - Tastenkombinationen
  - Modus mit hohem Kontrast
  - Anpassbare Textgröße

## ⌨️ Tastenkombinationen

- `Strg+L`: Anwendungsprotokolle anzeigen
- `F1`: Hilfe anzeigen
- `Esc`: Dialoge schließen
- `Strg+Q`: Anwendung beenden

## 📊 Verwendung

1. Legen Sie die Anzahl der Iterationen für den Benchmark fest
2. Klicken Sie auf "Benchmark starten"
3. Verfolgen Sie den Fortschritt in Echtzeit
4. Sehen Sie sich detaillierte Ergebnisse und Statistiken an
5. Greifen Sie für die Fehlerbehebung auf Protokolle zu

## 📂 Projektstruktur

```
benchmark/
├── .github/                            # GitHub Actions
│   ├── workflows/                      # GitHub Actions-Workflows
│   │   └── ci-cd.yml                   # CI/CD-Pipeline
│   ├── issues/                         # GitHub-Issues
│   |   └── templates/                  # GitHub-Issue-Vorlagen
│   └── FUNDING.yml                     # Förderdatei
├── assets/                             # Asset-Dateien
├── config/                             # Konfigurationsdateien
│   ├── config.json                     # Konfigurationsdatei
│   └── updates.json                    # Update-Cache
├── docs/                               # Dokumentation
│   ├── images/                         # Dokumentationsbilder
│   ├── pdf/                            # PDF-Dokumentation
│   └── USER_GUIDE.md                   # Benutzerhandbuch
├── lang/                               # Sprachdateien
│   ├── en.json                         # Englische Sprachdatei
│   └── it.json                         # Italienische Sprachdatei
├── logs/                               # Protokolldateien
├── script/                             # Quellcode
│   ├── __init__.py                     # Paketinitialisierung
│   ├── about.py                        # Info-Dialog
│   ├── benchmark_history.py            # Benchmark-Verlauf
│   ├── benchmark_tests.py              # Benchmark-Tests
│   ├── CLI_pystone.py                  # Pystone-Benchmark (CLI)
│   ├── config_manager.py               # Konfigurationsmanager
│   ├── export_results.py               # Ergebnisexport
│   ├── hardware_monitor.py             # Hardware-Monitor
│   ├── help.py                         # Hilfe-Dialog
│   ├── history_dialog.py               # Verlaufsdialog
│   ├── lang_mgr.py                     # Sprachmanager
│   ├── logger.py                       # Protokollierungskonfiguration
│   ├── menu.py                         # Menüleistenfunktionalität
│   ├── settings.py                     # Einstellungsdialog
│   ├── sponsor.py                      # Sponsor-Dialog
│   ├── system_info.py                  # Systeminformationen
│   ├── test_menu.py                    # Testmenü
│   ├── theme_manager.py                # Design-Manager
│   ├── updates.py                      # Update-System
│   ├── version.py                      # Versionssystem
│   ├── view_log.py                     # Protokollanzeige
│   └── visualization.py                # Benchmark-Visualisierung
├── tests/                              # Testdateien
│   ├── test_benchmark.py               # Benchmark-Test
│   ├── test_hardware_monitor.py        # Hardware-Monitor-Test
│   ├── test_monitor_manual.py          # Manueller Monitor-Test
│   ├── test_monitor.py                 # Monitor-Test
│   └── TEST_README.md                  # Test-README
├── .gitignore                          # Git-Ignore-Datei
├── CHANGELOG.md                        # Änderungsprotokoll
├── CONTRIBUTING.md                     # Beitragsrichtlinien
├── LICENSE                             # GPLv3-Lizenzdatei
├── main.py                             # Hauptanwendung
├── README.md                           # Diese Datei
├── requirements.txt                    # Anforderungen
└── TO_DO.md                            # Aufgabenliste
```
