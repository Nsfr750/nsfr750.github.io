---
lang: de
lang-niv: font
lang-ref: 012-jbk
layout: doc
order: 2
title: 'CDE550-Sim'
---

# Nidec Commander CDE 550 Simulator

[![Python Version](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Lizenz: GPL v3](https://img.shields.io/badge/Lizenz-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Version](https://img.shields.io/badge/version-0.0.2-green.svg)](CHANGELOG.md)

Software-Simulator für den Nidec Commander CDE 550 Wechselrichter mit grafischer Benutzeroberfläche, entwickelt in Python mit PyQt6.

## Neu in Version 0.0.2

- **Vollständige Lokalisierung** der Benutzeroberfläche auf Italienisch
- **Verbesserte Alarmverwaltung** mit reduzierten Fehlalarmen
- **Leistungsoptimierungen** beim Starten und bei Lastschwankungen
- **Aktualisierte Dokumentation** mit detaillierter Änderungshistorie

## Funktionen

- Realistische Simulation des Verhaltens des Nidec Commander CDE 550 Wechselrichters
- Intuitive grafische Benutzeroberfläche mit PyQt6, vollständig auf Italienisch lokalisiert
- Serielle Kommunikation über pyserial
- Unterstützung der wichtigsten Steuerbefehle
- Simulation von Fehlern und Alarme mit erweiterter Verwaltung
- Echtzeit-Überwachung von Parametern
- Protokollierung von Ereignissen und Fehlern

## Voraussetzungen

- Python 3.8 oder höher
- Pip (Python-Paketmanager)
- Python virtuelle Umgebung (empfohlen)

## Installation

1. Repository klonen:
   ```bash
   git clone https://github.com/Nsfr750/CDE550-sim.git
   cd CDE550-sim
   ```

2. Virtuelle Umgebung erstellen und aktivieren (optional, aber empfohlen):
   ```bash
   # Unter Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # Unter macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Abhängigkeiten installieren:
   ```bash
   pip install -r requirements.txt
   ```

## Verwendung

1. Starten Sie den Simulator:
   ```bash
   python main.py
   ```

2. Die grafische Benutzeroberfläche zeigt:
   - Status des Wechselrichters
   - Betriebsparameter
   - Ereignisprotokoll
   - Simulationssteuerungen

3. Für die serielle Verbindung:
   - Gehen Sie zu Verbindung -> Verbinden
   - Wählen Sie den gewünschten COM-Port aus
   - Stellen Sie die Kommunikationsgeschwindigkeit (Baudrate) ein
   - Klicken Sie auf "Verbinden"

## Unterstützte serielle Befehle

| Befehl | Beschreibung | Beispiel |
|--------|--------------|----------|
| `RUN` | Startet den Wechselrichter | `RUN` |
| `STOP` | Stoppt den Wechselrichter | `STOP` |
| `RST` | Setzt Alarme zurück | `RST` |
| `FREQ <Wert>` | Stellt die Frequenz (Hz) ein | `FREQ 50.0` |
| `DIR <1\|-1>` | Stellt die Richtung ein | `DIR 1` (vorwärts) |
| `STATUS` | Zeigt den vollständigen Status an | `STATUS` |
| `HELP` | Zeigt die Befehlsliste an | `HELP` |

## Projektstruktur

```
CDE550-sim/
├── main.py              # Einstiegspunkt der Anwendung
├── inverter_sim.py      # Wechselrichter-Simulationslogik
├── serial_handler.py    # Handhabung der seriellen Kommunikation
├── script/              # Benutzeroberfläche und Hilfedateien
│   ├── help.py          # Hilfefenster
│   ├── serial_dialog.py # Serielles Verbindungsfenster
│   └── version.py       # Versionsverwaltung
├── requirements.txt     # Projektabhängigkeiten
├── README.md            # Hauptdokumentation
└── CHANGELOG.md         # Änderungsprotokoll
```

## Mitwirken

Beiträge sind willkommen! Um Verbesserungen vorzuschlagen:

1. Forken Sie das Projekt
2. Erstellen Sie einen Feature-Branch (`git checkout -b feature/TolleFunktion`)
3. Committen Sie Ihre Änderungen (`git commit -m 'Füge tolle Funktion hinzu'`)
4. Übertragen Sie die Änderungen in das Repository (`git push origin feature/TolleFunktion`)
5. Erstellen Sie einen Pull-Request

## Lizenz

Veröffentlicht unter der GPL-3.0-Lizenz. Siehe `LIZENZ` für weitere Informationen.

## Kontakt

- Autor: Nsfr750
- E-Mail: [nsfr750@yandex.com]
- Repository: https://github.com/Nsfr750/CDE550-sim

---

<div align="center">
  <sub>Entwickelt mit ❤️ von Nsfr750</sub>
</div>
