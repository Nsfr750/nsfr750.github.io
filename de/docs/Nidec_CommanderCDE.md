---
lang: de
lang-niv: fonto
lang-ref: 017-jbk
layout: doc
order: 7
title: 'Nidec CommanderCDE'
---

# Nidec CommanderCDE

Eine umfassende Python-GUI-Anwendung zur Steuerung und Überwachung von Nidec Commander CDE-Antrieben über Modbus RTU.

## ✨ Funktionen

- **Mehrsprachige Unterstützung**: Vollständige Oberfläche auf Englisch und Italienisch mit dynamischem Sprachwechsel
- **Mehrfachmodell-Unterstützung**: Kompatibel mit den Antriebsmodellen CDE400, CDE550, CDE750 und CDE1100S
- **Antriebssteuerung**:
  - Verbindung zu Nidec Commander CDE-Antrieben über RS-485/Modbus RTU
  - Steuerung von Motordrehzahl und -richtung
  - Start/Stopp des Antriebs
  - Echtzeitüberwachung des Antriebszustands und der Diagnose
  - Fehlererkennung und Rücksetzfunktion
  - Parameter-Sicherung und -Wiederherstellung
- **Benutzeroberfläche**:
  - Moderne, auf Registerkarten basierende Oberfläche mit intuitiven Steuerelementen
  - Umfassendes Dashboard mit Echtzeit-Metriken
  - Statusleiste mit Verbindungs- und Antriebsstatus
  - Reaktionsfähiges Design mit Unterstützung für Dunkel-/Hellmodus
  - Anpassbare Oberflächenelemente
- **Datenverwaltung**:
  - Echtzeitüberwachung und Protokollierung von Antriebsparametern
  - Datenexport nach CSV/Excel
  - Grafische Darstellung von Parameterverläufen
  - Konfigurierbare Protokollierungsintervalle
- **Diagnose**:
  - Umfassende Parameterüberwachung
  - Fehlerverlauf und -protokollierung
  - Systemstatusanzeigen
  - Echtzeit-Leistungsmetriken

## 🆕 Neu in Version 0.0.4

### Neue Funktionen
- Unterstützung für mehrere Nidec-Antriebsmodelle (CDE400, CDE550, CDE750, CDE1100S) hinzugefügt
- Vollständige Übersetzungen für alle Oberflächenelemente ins Italienische
- Verbessertes Hilfesystem mit detaillierter Dokumentation
- Blaues Design für bessere Lesbarkeit in den Hilfeseiten

### Verbesserungen
- Aktualisierte Benutzeroberfläche für ein besseres Nutzererlebnis
- Verbesserte Fehlermeldungen und Protokollierung
- Optimierte Leistung für die Echtzeitüberwachung
- Behobene Kompatibilitätsprobleme mit PyQt6
- Korrigierter Sprachwechsel in Hilfedialogen

## 🚀 Systemanforderungen

- Python 3.8 oder höher
- PyQt6 >= 6.6.1
- pyserial >= 3.5
- pymodbus >= 3.5.4
- PyQt6-QScintilla >= 2.14.1
- python-dotenv >= 1.0.0

## 🛠 Installation & Einrichtung

1. Repository klonen:

   ```bash
   git clone https://github.com/Nsfr750/nidec-commandercde.git
   cd nidec-commandercde
   ```

2. Virtuelle Umgebung erstellen und aktivieren (empfohlen):

   ```bash
   python -m venv venv
   # Unter Windows:
   .\venv\Scripts\activate
   # Unter Unix oder MacOS:
   # source venv/bin/activate
   ```

3. Erforderliche Pakete installieren:

   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Grundlegende Verwendung

1. Schließen Sie Ihren Nidec Commander CDE-Antrieb über einen RS-485-Adapter an Ihren Computer an
2. Starten Sie die Anwendung:

   ```bash
   python main.py
   ```

3. Wählen Sie den entsprechenden COM-Port und die Baudrate
4. Klicken Sie auf 'Verbinden', um die Kommunikation mit dem Antrieb herzustellen
5. Verwenden Sie die Benutzeroberfläche, um den Antrieb zu steuern und zu überwachen

## Verbindungseinstellungen

- Baudrate: 9600
- Datenbits: 8
- Parität: Gerade
- Stoppbits: 1
- Modbus-Adresse: 1 (Standard, kann in den Antriebsparametern geändert werden)

## Wichtige Hinweise

- Diese Software wird ohne jegliche Gewährleistung bereitgestellt
- Stellen Sie beim Arbeiten mit Motorantrieben immer geeignete elektrische Verbindungen und Sicherheitsmaßnahmen sicher
- Die Standard-Registeradressen basieren auf typischen Nidec-Antriebskonfigurationen, müssen aber möglicherweise an Ihr spezifisches Modell angepasst werden
- Weitere Informationen zu Parametern und Registeradressen finden Sie im Nidec CDE 400 Commander-Handbuch
