---
lang: de
lang-niv: fonto
lang-ref: 016-jbk
layout: doc
order: 6
title: 'NFC'
---

# 🚀 NFC Lese-/Schreibanwendung

[![Lizenz: GPL v3](https://img.shields.io/badge/Lizenz-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Code-Stil: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Eine leistungsstarke PySide6-basierte Anwendung zum Lesen von und Schreiben auf verschiedene NFC-Typen mit erweiterten Funktionen und einer benutzerfreundlichen Oberfläche.

## Installation

### Voraussetzungen

- Python 3.9 oder höher
- NFC-Lesegerät (ACR122U, ACR1252U usw.)

### Schnellstart

1. Repository klonen:

   ```bash
   git clone https://github.com/Nsfr750/NFC.git
   cd NFC
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

Detaillierte Installationsanweisungen finden Sie in [PREREQUISITES.md](PREREQUISITES.md).

## Funktionen

- **Mehrfach-Tag-Unterstützung**: Umfassende Unterstützung verschiedener NFC-Tag-Typen:
  - NTAG (NTAG213, NTAG215, NTAG216)
  - MIFARE Classic (1K, 4K)
  - MIFARE Ultralight
  - FeliCa (Sony)
  - ISO 14443 Typ A/B Karten

- **Vollständige Tag-Unterstützung**: [Unterstützte Operationen anzeigen](docs/supported_operations.md) für alle Tag-Typen

- **NDEF-Operationen**:
  - Lesen und Schreiben von NDEF-Datensätzen
  - Erstellen und Verwalten mehrerer NDEF-Datensätze
  - Unterstützung verschiedener NDEF-Datensatztypen (Text, URI, Smart Poster usw.)
  - Hex-Ansicht zur Inspektion von Rohdaten

- **Tag-Verwaltung**:
  - Tag-Informationen lesen (UID, Speicherlayout, Fähigkeiten)
  - Daten mit Validierung auf Tags schreiben
  - Tags gegen unbefugtes Beschreiben sperren
  - Tags für die NDEF-Nutzung formatieren

- **Benutzeroberfläche**:
  - Modernes, ansprechendes Design mit sphinx_rtd_theme
  - Unterstützung für Hell-/Dunkel-/Systemdesign
  - Echtzeit-Tag-Erkennung und Statusaktualisierungen
  - Detailliertes Tag-Informationsfeld
  - Protokollanzeige mit Filteroptionen
  - Umfassende Dokumentation auf Englisch und Italienisch

- **Sicherheitsfunktionen**:
  - 🔒 Passwortschutz für sensible Vorgänge
  - 🔑 Sicheres Passwort-Hashing mit PBKDF2
  - 🔄 Funktion zum Ändern des Passworts
  - ⚙️ Option zum Aktivieren/Deaktivieren des Passwortschutzes
  - 🔐 Geschützte Vorgänge umfassen Tag-Tools, Datenbank und Klonen

- **Erweiterte Funktionen**:
  - Tag-Emulationsmodus (experimentell)
  - Stapelverarbeitung für mehrere Tags
  - Ausführung benutzerdefinierter Befehle
  - Protokollierungssystem mit mehreren Detaillierungsstufen
  - API-Dokumentation für Entwickler
  - Fehlerbehebungsleitfaden für häufige Probleme
  - Richtlinien für Open-Source-Beiträge

## 🚀 Systemanforderungen

- Python 3.8 oder höher
- Unterstütztes NFC-Lesegerät:
  - ACR122U
  - PN532 (über USB/UART)
  - PC/SC-kompatible Lesegeräte
- Windows 10/11 oder Linux mit PC/SC-Unterstützung
- Erforderliche Python-Pakete (siehe `requirements.txt`)

## 📖 Dokumentation

Umfassende Dokumentation ist auf Englisch und Italienisch verfügbar, einschließlich:

- Benutzerhandbuch
- API-Referenz
- Fehlerbehebungsleitfaden
- Häufig gestellte Fragen
- Richtlinien für Beiträge

So erstellen Sie die Dokumentation lokal:

```bash
# Dokumentationsvoraussetzungen installieren
pip install -r requirements-docs.txt

# Englische Dokumentation erstellen
cd docs/ENG
make html

# Deutsche Dokumentation erstellen
cd ../DEU
make html
```

Die Dokumentation wird im Verzeichnis `_build/html` jedes Sprachordners verfügbar sein.

## 📦 Installation

1. Dieses Repository klonen:

   ```bash
   git clone https://github.com/Nsfr750/NFC.git
   cd NFC
   ```

2. Virtuelle Umgebung erstellen und aktivieren (empfohlen):

   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate

   # Linux/macOS
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Erforderliche Pakete installieren:

   ```bash
   pip install -r requirements.txt
   ```

4. (Optional) PC/SC-Treiber installieren, falls noch nicht geschehen:
   - Windows: [CCID-Treiber](https://ccid.apdu.fr/) installieren
   - Linux: Pakete `pcscd` und `libpcsclite-dev` installieren

5. Anwendung starten:

   ```bash
   python main.py
   ```

## 🚀 Verwendung

### Grundlegende Vorgänge

1. **NFC-Lesegerät anschließen**
   - Die Anwendung erkennt unterstützte Geräte automatisch
   - Der Verbindungsstatus wird in der Statusleiste angezeigt

2. **Tag lesen**
   - Halten Sie einen NFC-Tag in die Nähe des Lesegeräts
   - Die Tag-Informationen werden im Hauptfenster angezeigt
   - Detaillierte Speicherbelegung im Hex-Editor anzeigen

3. **Auf ein Tag schreiben**
   - Navigieren Sie zum Tab "Schreiben"
   - Wählen Sie den Datensatztyp (Text, URI usw.)
   - Geben Sie Ihren Inhalt ein und klicken Sie auf "Auf Tag schreiben"

4. **Tag sperren**
   - Verwenden Sie die Schaltfläche "Sperren", um weitere Schreibvorgänge zu verhindern
   - Einige Tags unterstützen dauerhaftes Sperren (Vorsicht!)

### 🛠️ Erweiterte Funktionen

- **Tag-Emulation**: Emulieren Sie einen NFC-Tag (experimentell)
- **Stapelverarbeitung**: Verarbeiten Sie mehrere Tags gleichzeitig
- **Benutzerdefinierte Skripte**: Führen Sie benutzerdefinierte Befehle auf Tags aus
- **Erweiterte Protokollierung**: Detaillierte Protokolle zur Fehlersuche anzeigen

## 🤝 Mitwirken

Beiträge sind willkommen! Bitte lesen Sie unsere [Beitragsrichtlinien](CONTRIBUTING.md) für weitere Details.

## 📄 Lizenz

Dieses Projekt steht unter der GPL-3.0-Lizenz - siehe [LICENSE](LICENSE) für Details.

## 📞 Unterstützung

Bei Problemen und Fragen öffnen Sie bitte ein [Issue](https://github.com/Nsfr750/NFC/issues) auf GitHub.
