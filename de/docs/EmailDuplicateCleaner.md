---
lang: de
lang-niv: fonto
lang-ref: 013-jbk
layout: doc
order: 3
title: 'E-Mail-Duplikatbereiniger'
---

# 📧 E-Mail-Duplikatbereiniger

Ein umfassendes Python-Tool zum Scannen, Identifizieren und Entfernen doppelter E-Mails über mehrere E-Mail-Clients hinweg. Mit Web-, Desktop- und Befehlszeilenschnittstelle.

## 🚀 Version

**Aktuelle Version:**
[![GitHub-Version](https://img.shields.io/badge/version-v2.5.2-green)](https://github.com/Nsfr750/EmailDuplicateCleaner)
[![Dokumentation](https://img.shields.io/badge/dokumentation-verfügbar-brightgreen)](https://github.com/Nsfr750/EmailDuplicateCleaner/blob/master/README.md)
[![Python-Versionen](https://img.shields.io/badge/python-3.8%20|%203.9%20|%203.10%20|%203.11%20|%203.12-blue)](https://www.python.org/)
[![Lizenz: GPL v3](https://img.shields.io/badge/Lizenz-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![PyPI](https://img.shields.io/pypi/v/email-duplicate-cleaner)](https://pypi.org/project/email-duplicate-cleaner/)
[![Spenden](https://img.shields.io/badge/Spenden-PayPal-green.svg)](https://paypal.me/3dmega)
[![Unterstützung](https://img.shields.io/badge/Unterstützung-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750)

## ✨ Neu in Version 2.5.2

- 🚀 Aktualisierung auf Version 2.5.2
- 🐛 Fehlerbehebung bei der Versionsnummern-Anzeige im Info-Dialog
- 📚 Dokumentation aktualisiert, um die neuesten Änderungen widerzuspiegeln

## ✨ Neu in Version 2.5.1

- 🐛 Behobener QAction-Importfehler in der PySide6-Oberfläche
- 🌐 Vollständige englische Übersetzungen hinzugefügt
- 📄 GPL-3.0-Lizenzdatei eingefügt
- 🔄 Verbesserte Fehlerbehandlung bei der GUI-Initialisierung
- ⬆️ Abhängigkeiten für bessere Stabilität aktualisiert

## ✨ Funktionen

### 🔍 Duplikaterkennung

- Mehrere Erkennungskriterien:
  - Streng: Umfassender Vergleich
  - Nur Inhalt: Analyse des Nachrichtentexts
  - Kopfzeilen: Metadatenbasierte Übereinstimmung
  - Betreff+Absender: Fokussierte Identifizierung

### 📊 E-Mail-Analyse

- Erweiterte E-Mail-Analysen:
  - Absenderanalyse: Wichtige Absender und Domains identifizieren
  - Zeitliche Analyse: E-Mail-Muster über die Zeit visualisieren
  - Anhangsanalyse: Dateitypen, -größen und -häufigkeiten
  - Themenanalyse: Konversationsverläufe anzeigen und verwalten
  - Duplikatanalyse: Detaillierte Einblicke in die Duplikaterkennung
  - Exportierbare Berichte in mehreren Formaten (Text, HTML, JSON)

### 🖥️ Multi-Schnittstellen-Unterstützung

- **Web-Oberfläche** - Modernes, responsives Design mit Dunkel-/Hellmodus
- **Desktop-GUI** - Native Desktop-Erfahrung mit PySide6
- **Befehlszeilenschnittstelle** - Leistungsstarke Automatisierungs- und Skriptunterstützung

### 🌓 Verbessertes Benutzererlebnis

- Moderne Weboberfläche mit Dunkel-/Hellmodus
- Interaktive Vorschau mit Echtzeitaktualisierungen
- Umfangreiches Hilfesystem
- Debug-Modus mit detaillierter Protokollierung
- Demo-Modus zum Testen und Lernen

### 🔒 E-Mail-Client-Kompatibilität

Unterstützt:

- Mozilla Thunderbird
- Apple Mail
- Microsoft Outlook
- Generische mbox/maildir-Formate

### 🏗️ Technische Highlights

- Moderne Weboberfläche mit Flask
- Datenbankverwaltung mit SQLAlchemy
- Umfangreiches Hilfesystem mit dynamischen Inhalten
- Modulare Architektur mit klarer Aufgabentrennung
- Plattformübergreifende Kompatibilität
- Umfangreiche Fehlerbehandlung und Protokollierung

## 🛠️ Voraussetzungen

- Python 3.8+
- pip
- Unterstützte Betriebssysteme: Windows, macOS, Linux

## 🚀 Schnellstart

### 💰 Unterstützen Sie dieses Projekt

Wenn Sie dieses Tool nützlich finden, erwägen Sie bitte eine Unterstützung der Entwicklung:

- [![Spenden](https://img.shields.io/badge/Spenden-PayPal-green.svg)](https://paypal.me/3dmega) Über PayPal unterstützen
- [![Unterstützung](https://img.shields.io/badge/Unterstützung-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750) Werden Sie ein Unterstützer
- :money_with_wings: **Monero (XMR)**: 
  ```
  47Jc6MC47WJVFhiQFYwHyBNQP5BEsjUPG6tc8R37FwcTY8K5Y3LvFzveSXoGiaDQSxDrnCUBJ5WBj6Fgmsfix8VPD4w3gXF
  ```

## 📦 Installation

1.  Repository klonen:

    ```bash
    git clone https://github.com/Nsfr750/EmailDuplicateCleaner.git
    cd EmailDuplicateCleaner
    ```

2.  Abhängigkeiten installieren:

    ```bash
    pip install -r requirements.txt
    ```

### Anwendung starten

#### Weboberfläche

```bash
python app.py
```

Verfügbar unter `http://localhost:5000`

#### Desktop-Oberfläche

```bash
python email_cleaner_gui.py
```

#### Befehlszeilen-Demo

```bash
python email_duplicate_cleaner.py --demo
```

## 🤝 Mitwirken

Interessiert an einer Mitarbeit? Lesen Sie unsere [Richtlinien für Beiträge](CONTRIBUTING.md)!

## 📄 Lizenz

Dieses Projekt steht unter der MIT-Lizenz.

## 🐛 Probleme

Einen Fehler gefunden? [Erstellen Sie ein Ticket](https://github.com/Nsfr750/EmailDuplicateCleaner/issues)

## 📊 Erkennungsmethoden

- `strict`: Nachrichten-ID + Datum + Von + Betreff + Inhalt
- `content`: Nur Inhalt
- `headers`: Nachrichten-ID + Datum + Von + Betreff
- `subject-sender`: Nur Betreff- und Absenderfelder

## Sicherheitsfunktionen

- Behält immer mindestens eine Kopie jeder E-Mail
- Behält standardmäßig die älteste E-Mail
- Originale E-Mails können aus dem Papierkorb wiederhergestellt werden
- Demo-Modus für sicheres Testen

## Projektstruktur

- `email_cleaner_web.py`: Weboberfläche
- `email_cleaner_gui.py`: Desktop-Oberfläche
- `email_duplicate_cleaner.py`: Kernfunktionalität und CLI
- `static/`: Web-Assets (CSS, JS)
- `templates/`: HTML-Vorlagen

## Arbeitsabläufe

- Demo-Modus: Läuft mit Test-E-Mails
- Hilfe: Zeigt Nutzungsinformationen an
- GUI-Modus: Startet die grafische Oberfläche
- Web-Modus: Startet den Webserver

## GUI-Struktur

- **GUI (`email_cleaner_gui.py`)** : Eine benutzerfreundliche grafische Oberfläche, die mit Tkinter erstellt wurde. Sie bietet eine intuitive Möglichkeit, E-Mail-Clients auszuwählen, Ordner zu durchsuchen und Duplikate zu verwalten.
- **CLI (`email_cleaner_cli.py`)** : Eine Befehlszeilenschnittstelle für Benutzer, die lieber im Terminal arbeiten.
- **Web (`app.py`)** : Eine webbasierte Oberfläche, die mit Flask erstellt wurde und von jedem Browser aus zugänglich ist.

### Hilfsmodule (`struttura/`)

Das Verzeichnis `struttura/` enthält alle Hilfsmodule, die die grafische Oberfläche unterstützen, wie Dialogfenster und das Menü.

- **`menu.py`** : Verwaltet die Erstellung und Funktionalität der Hauptmenüleiste und hält die Haupt-GUI-Datei sauber und auf ihr Kernlayout fokussiert.
- **`about.py`**, **`help.py`**, **`sponsor.py`** : Definieren die Dialogfenster `Über`, `Hilfe` und `Unterstützung`, wobei jedes in seiner eigenen Klasse gekapselt ist.
- **`log_viewer.py`** : Ein einfacher Log-Viewer zur Anzeige von Anwendungsprotokollen.
