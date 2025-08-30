---
lang: de
lang-niv: fonto
lang-ref: 020-jbk
layout: doc
order: 11
title: 'PySnoop'
---

# PySnoop

[![Lizenz: GPL v3](https://img.shields.io/badge/Lizenz-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![Code-Stil: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Eine moderne Python-Anwendung zum Lesen, Schreiben und Analysieren von Magnetstreifenkartendaten. Dieses Projekt ist eine Fortführung des ursprünglichen StripeSnoop-Projekts, neu aufgebaut mit modernem Python und einer benutzerfreundlichen Oberfläche.

## ✨ Funktionen

- **Kartenlesen**: Lesen von Magnetstreifenkarten mit kompatiblen Lesegeräten
- **Datenbankverwaltung**: Sichere Speicherung und Verwaltung von Kartendaten
- **Mehrere Formate**: Export/Import von Kartendaten in verschiedenen Formaten
- **Moderne GUI**: Benutzerfreundliche Oberfläche mit Themenunterstützung
- **Plattformübergreifend**: Läuft unter Windows, macOS und Linux
- **Eigenständige Ausführbare Datei**: Als einzelne ausführbare Datei für einfache Verteilung
- **Debug-Builds**: Spezielle Debug-Konfiguration zur Fehlerbehebung
- **Sicherheit**: Sichere Speicherung sensibler Kartendaten
- **Validierung**: Integrierte Kartennummernvalidierung (C10/Luhn)
- **Dokumentation**: Umfassende Dokumentation und Beispiele

## 🚀 Installation

### Voraussetzungen

- Python 3.7 oder höher
- pip (Python-Paketmanager)
- Git (optional, für die Entwicklung)

### Schnellstart

1. Repository klonen:

   ```bash
   git clone https://github.com/Nsfr750/PySnoop.git
   cd PySnoop
   ```

2. Virtuelle Umgebung erstellen und aktivieren:

   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Abhängigkeiten installieren:

   ```bash
   pip install -r requirements.txt
   ```

## 🏗️ Anwendung erstellen

PySnoop kann mit Nuitka in eine eigenständige ausführbare Datei umgewandelt werden. Wir bieten zwei Build-Skripte an:

### Debug-Build

```bash
.\snoop_debug.bat
```

Erstellt eine Debug-Version der Anwendung mit aktiviertem Konsolenfenster zur Fehlerbehebung.

### Release-Build

```bash
.\snoop.bat
```

Erstellt eine optimierte Release-Version der Anwendung.

### Build-Ausgaben

- Debug-Build: `build\PySnoop_debug.exe`
- Release-Build: `build\PySnoop.exe`

## 🛠️ Entwicklung
   ```bash
   pip install -r requirements.txt
   ```

## 💻 Verwendung

### GUI-Modus (Empfohlen)

```bash
python pysnoop_gui.py
```

### Befehlszeilenschnittstelle

```bash
python pysnoop.py [Optionen]
```

### Verfügbare Optionen

```bash
-h, --help      Hilfe anzeigen
-v, --verbose   Ausführliche Ausgabe aktivieren
--version       Versionsinformationen anzeigen
```

## 🔌 Unterstützte Geräte

- MSR605 Magnetstreifenkartenleser/-schreiber
- Andere HID-kompatible Kartenleser (experimentell)

## 📚 Dokumentation

Detaillierte Dokumentation, einschließlich API-Referenz und Anwendungsbeispiele, finden Sie in der [Dokumentation](https://nsfr750.github.io/PySnoop/ "PySnoop-Dokumentation").

## 🤝 Mitwirken

Mitwirkung ist willkommen! Bitte lesen Sie unsere [Richtlinien für Beiträge](CONTRIBUTING.md), um zu beginnen.

## 📄 Lizenz

Dieses Projekt ist unter der GPLv3-Lizenz lizenziert - siehe die Datei [LICENSE](LICENSE) für Details.

## 🙏 Unterstützung

Wenn Sie dieses Projekt nützlich finden, erwägen Sie eine Unterstützung der Entwicklung:

[![Über PayPal spenden](https://img.shields.io/badge/Spenden-PayPal-blue.svg)](https://paypal.me/3dmega)
[![Werden Sie ein Förderer](https://img.shields.io/badge/Unterstützen-Patreon-orange.svg)](https://www.patreon.com/Nsfr750)

## 📧 Kontakt

Bei Fragen oder Unterstützung öffnen Sie bitte ein Issue oder kontaktieren Sie [Nsfr750](mailto:nsfr750@yandex.com).

## Danksagung

- Basierend auf dem ursprünglichen StripeSnoop-Projekt (http://stripesnoop.sourceforge.net)

## Mitwirken

Beiträge sind willkommen! Bitte zögern Sie nicht, einen Pull Request zu senden.
