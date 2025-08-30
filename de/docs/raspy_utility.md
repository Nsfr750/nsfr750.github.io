---
lang: de
lang-niv: font
lang-ref: 021-jbk
layout: doc
order: 12
title: 'RasPY Utility'
---

# RasPY Utility

<div align="center">
  <img src="../images/logo.png" alt="RasPY Utility Logo" width="50%">
</div>

## Willkommen zur RasPY Utility Dokumentation

RasPY Utility ist eine umfassende Anwendung zur Steuerung und Überwachung von Raspberry Pi GPIO-Pins über eine intuitive grafische Oberfläche oder REST-API.

## Inhaltsverzeichnis

### Einführung
- [Installation](installazione.md)
- [Anleitung](guida.md)

### Entwicklung
- [Entwicklung](sviluppo.md)
- [API](api.md)
- [GUI](gui.md)
- [Beispiele](esempi.md)

### Zusätzliche Ressourcen
- [Änderungsprotokoll](changelog.md)
- [FAQ](faq.md)

### Community
- [Mitwirken](contribuire.md)
- [Danksagungen](ringraziamenti.md)

## Hauptmerkmale

### ✅ **Moderne grafische Oberfläche**
- Dunkles/Helles Design
- Mehrsprachige Unterstützung
- Echtzeit-Überwachung der Pin-Status
- System-Tray-Integration

### 🔌 **Vollständige GPIO-Unterstützung**
- Digitale Ein-/Ausgabe-Pin-Steuerung
- Integrierter Simulator für die Entwicklung
- Automatische Hardware-Erkennung
- Unterstützung für Remote-GPIO

### 🌐 **Web-Oberfläche**
- Integrierter Webserver
- Reaktionsfähiges Design für Mobilgeräte/Desktop
- Echtzeit-Aktualisierungen
- Integrierte API-Dokumentation

## Schnellstart

1. [Installation](installazione.md) - So installieren und konfigurieren Sie RasPY Utility
2. [Anleitung](guida.md) - Benutzerhandbuch für die Anwendung
3. [API](api.md) - API-Dokumentation für Entwickler
4. [Entwicklung](sviluppo.md) - Entwicklungs- und Beitragsanleitung

## Benutzerhandbuch

### Grafische Oberfläche

Die grafische Oberfläche von RasPY 4 Utility ist intuitiv und einfach zu bedienen.

#### Hauptmenü

- **Datei**: Allgemeine Anwendungssteuerungen
- **GPIO**: GPIO-Pin- und Simulatorverwaltung
- **Ansicht**: Anpassung der Benutzeroberfläche
- **Hilfe**: Dokumentation und Informationen

#### GPIO-Steuerung

1. Öffnen Sie das GPIO-Steuerungsfenster über das Menü
2. Wählen Sie den zu steuernden Pin aus
3. Verwenden Sie die Schaltflächen, um die Pins umzuschalten
4. Überwachen Sie den Status in Echtzeit

#### GPIO-Simulator
Mit dem Simulator können Sie Code ohne physische Hardware testen:

1. Starten Sie den Simulator über das GPIO-Menü
2. Verwenden Sie die Oberfläche, um Ein-/Ausgaben zu simulieren
3. Änderungen werden in Echtzeit übernommen

### Protokollierung und Fehlerbehebung
Die Anwendung protokolliert wichtige Ereignisse in der Datei `logs/app.log`. Verwenden Sie den integrierten Protokollbetrachter, um:

- Nachrichten nach Ebene filtern (INFO, WARNUNG, FEHLER)
- Nach bestimmten Nachrichten suchen
- Protokolle zur Analyse exportieren

### Tastenkombinationen

- **Strg+Q**: Anwendung beenden
- **F1**: Hilfe anzeigen
- **Strg+L**: Protokollbetrachter öffnen
- **F5**: Benutzeroberfläche aktualisieren

## API-Referenz

### Überblick

Die RasPY 4 Utility REST-API ermöglicht die Steuerung von GPIO-Pins über HTTP-Anfragen.
Alle Antworten erfolgen im JSON-Format.

### Verfügbare Endpunkte

#### `GET /api/gpio`

Gibt den Status aller konfigurierten GPIO-Pins zurück.

**Beispielantwort:**

```json
{
  "17": {"state": 0, "mode": "out", "description": "Rote LED"},
  "18": {"state": 1, "mode": "in", "description": "Taster"}
}
```

#### `GET /api/gpio/<int:pin>`

Gibt den Status eines bestimmten Pins zurück.

**Parameter:**
- `pin`: GPIO-Pin-Nummer

**Statuscodes:**
- 200: Vorgang erfolgreich
- 404: Pin nicht gefunden

**Beispielantwort:**

```json
{
  "state": 0,
  "mode": "out",
  "description": "Rote LED"
}
```

#### `POST /api/gpio/<int:pin>/on`

Schaltet den angegebenen Pin ein.

**Parameter:**
- `pin`: GPIO-Pin-Nummer

**Statuscodes:**
- 200: Vorgang erfolgreich
- 400: Ungültiger oder nicht beschreibbarer Pin

#### `POST /api/gpio/<int:pin>/off`

Schaltet den angegebenen Pin aus.

**Parameter:**
- `pin`: GPIO-Pin-Nummer

**Statuscodes:**
- 200: Vorgang erfolgreich
- 400: Ungültiger oder nicht beschreibbarer Pin

## Anwendungsbeispiele

### GPIO-Steuerung mit Python

```python
import requests

BASE_URL = "http://localhost:5000/api/gpio"

# Status aller Pins abrufen
response = requests.get(f"{BASE_URL}")
print("Aktueller Status:", response.json())

# Pin 17 einschalten
response = requests.post(f"{BASE_URL}/17/on")
print("Antwort beim Einschalten:", response.status_code)
```

## Nützliche Ressourcen

- [Offizielle Raspberry Pi-Website](https://www.raspberrypi.org/)
- [Python-Dokumentation](https://www.python.org/)
- [GPIO-Pinbelegung](https://pinout.xyz/)
