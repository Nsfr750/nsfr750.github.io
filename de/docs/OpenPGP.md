---
lang: de
lang-niv: fonto
lang-ref: 018-jbk
layout: page
title: 'OpenPGP'
---

# OpenPGP GUI App Dokumentation

Willkommen zur offiziellen Dokumentation der **OpenPGP GUI App**.

## Übersicht
Diese Anwendung bietet eine moderne, benutzerfreundliche Oberfläche zur Verwaltung von OpenPGP-Schlüsseln, Verschlüsselung, Entschlüsselung, Nachrichtensignierung, -überprüfung und SSL-Zertifikatsgenerierung. Alle kryptografischen Vorgänge werden lokal ausgeführt, um maximale Privatsphäre zu gewährleisten.

# Funktionen

- Moderne Benutzeroberfläche mit ttkbootstrap (Superhero-Design)
- OpenPGP-Schlüsselpaare generieren, laden und exportieren
- Schlüsselname, E-Mail, Passphrase festlegen und Fingerabdruck anzeigen
- Nachrichten verschlüsseln und entschlüsseln
- Nachrichten signieren und überprüfen (abgetrennte Signaturen)
- Öffentlichen Schlüssel im ASCII-armierten Format (.asc) exportieren
- Visuelle Darstellung des Schlüsselfingerabdrucks zur Sicherheitsüberprüfung
- SSL-Zertifikate mit benutzerdefiniertem CN generieren
- Alle Felder mit einem Klick zurücksetzen
- **Zentralisiertes Protokollsystem** (Info, Warnung, Fehler, unbehandelte Ausnahmen)
- **Protokollanzeige mit Echtzeitfilterung** (ALLE, INFO, WARNUNG, FEHLER)
- Verwendung von `log_info`, `log_warning`, `log_error` für benutzerdefinierte Protokolleinträge
- Automatische Erfassung und Anzeige von Tracebacks in der Protokollanzeige
- Dynamische Menüleiste mit Dialogen zu Über, Hilfe, Protokollanzeige, Sponsor, Version
- Semantische Versionsverwaltung und Versionsinformationen
- Modulare Struktur (`struttura`, `gui` usw.)
- Einfache Erweiterbarkeit und Anpassung (über ttkbootstrap)

# Erste Schritte

## Voraussetzungen
- Python 3.9 oder höher
- PySide6 (in den Anforderungen enthalten)
- pgpy (in den Anforderungen enthalten)
- cryptography (in den Anforderungen enthalten)
- pyperclip (in den Anforderungen enthalten)

> **Hinweis**: Die Anwendung wurde von Tkinter/ttkbootstrap auf PySide6 migriert, um eine modernere und wartbarere Benutzeroberfläche zu bieten.

## Installation
1. Klonen oder laden Sie dieses Repository herunter.
2. (Optional) Erstellen Sie eine virtuelle Umgebung:
   ```
   python -m venv venv
   venv\Scripts\activate
   ```
3. Installieren Sie die Abhängigkeiten:
   ```
   pip install -r requirements.txt
   ```

## Ausführen der Anwendung
Führen Sie im Stammverzeichnis des Projekts aus:
```
python main.py
```

Falls Sie Importfehler erhalten, stellen Sie sicher, dass Sie das Skript aus dem Stammverzeichnis und nicht aus einem Unterordner ausführen.

# Benutzerhandbuch

## Übersicht des Hauptfensters
- Geben Sie Ihren Namen, Ihre E-Mail und Ihre Passphrase für die Schlüsselgenerierung ein.
- Wählen Sie den Algorithmus (derzeit RSA; weitere folgen in Kürze).
- Verwenden Sie die Schaltflächen zum Generieren, Laden oder Exportieren von Schlüsseln.
- Der Fingerabdruck des geladenen/generierten Schlüssels wird zur Überprüfung angezeigt.
- Verwenden Sie das Textfeld, um Nachrichten zum Verschlüsseln, Entschlüsseln, Signieren oder Überprüfen einzugeben.
- Exportieren Sie Ihren öffentlichen Schlüssel, um ihn sicher zu teilen.
- Generieren Sie SSL-Zertifikate über die grafische Oberfläche.
- Verwenden Sie die Schaltfläche 'Zurücksetzen', um alle Felder zu leeren.

## Menüleiste
- **Datei**: Öffentlichen Schlüssel exportieren, Beenden
- **Protokoll**: Protokoll anzeigen (mit Filtern für ALLE, INFO, WARNUNG, FEHLER)
- **Hilfe**: Hilfe, Über, Sponsor

## Protokollierung und Protokollanzeige
- Alle Informationen, Warnungen, Fehler und unbehandelten Ausnahmen werden automatisch protokolliert.
- Verwenden Sie `log_info(msg)`, `log_warning(msg)`, `log_error(msg)` in Ihren Skripten für benutzerdefinierte Protokolleinträge.
- Die Protokollanzeige (Protokoll > Protokoll anzeigen) ermöglicht das Filtern und Anzeigen von Protokollen nach Ebene.
- Falls die Protokolldatei fehlt, wird der letzte Laufzeit-Fehlerbericht angezeigt (falls verfügbar).

## Tipps
- Alle kryptografischen Vorgänge erfolgen lokal (keine Cloud).
- Verwenden Sie für optimale Sicherheit starke Passphrasen.
- Das Protokollfenster bietet Rückmeldungen und Fehlerdetails.

# Erweiterte Nutzung

## Exportieren öffentlicher Schlüssel
- Verwenden Sie die Schaltfläche 'Öffentlichen Schlüssel exportieren' oder den entsprechenden Menüpunkt, um Ihren öffentlichen Schlüssel im ASCII-armierten Format (.asc) zu speichern.

## Überprüfen des Fingerabdrucks
- Überprüfen Sie den Fingerabdruck immer, bevor Sie Ihren öffentlichen Schlüssel teilen, um zusätzliche Sicherheit zu gewährleisten.

## SSL-Zertifikatsgenerierung
- Geben Sie den gewünschten Common Name (CN) in das Namensfeld ein.
- Klicken Sie auf die Schaltfläche 'SSL-Zertifikat generieren', um ein selbstsigniertes Zertifikat zu erstellen.

## Erweitern der Anwendung
- Sie können weitere Algorithmen (z.B. ECC, Ed25519) unterstützen, indem Sie die Schlüsselgenerierungslogik in `main_window.py` erweitern.
- Die Benutzeroberfläche verwendet ttkbootstrap für einfache Anpassung und Themenverwaltung.

## Protokollierung und Fehlerbehebung
- Alle Aktionen, Warnungen, Fehler und unbehandelten Ausnahmen werden in `traceback.log` protokolliert.
- Verwenden Sie `log_info`, `log_warning`, `log_error` für benutzerdefinierte Protokolleinträge in Ihrem Code.
- Die Protokollanzeige unterstützt die Filterung nach ALLE, INFO, WARNUNG, FEHLER.
- Unbehandelte Ausnahmen werden automatisch protokolliert und in der Protokollanzeige angezeigt (mit Fehlerbericht).

## Fehlerbehebung
- Bei Importfehlern stellen Sie sicher, dass Sie das Skript aus dem Stammverzeichnis des Projekts ausführen.
- Bei Problemen mit Abhängigkeiten überprüfen Sie `requirements.txt` oder installieren Sie die erforderlichen Pakete neu.

# Entwicklerhandbuch

Willkommen, Entwickler! Dieses Handbuch enthält die wesentlichen Informationen zur Mitarbeit an der OpenPGP GUI App und deren Erweiterung.

---

## Projektstruktur
- `main.py` — Einstiegspunkt, startet das Hauptfenster.
- `gui/` — Alle Benutzeroberflächenkomponenten (Hauptfenster, Widgets, Dialoge).
- `struttura/` — Kernlogik, Dialoge, Hilfsfunktionen, Versionsverwaltung, Hilfe/Über usw.
- `docs/` — Dokumentation.
- `requirements.txt` — Python-Abhängigkeiten.

## Wichtige Technologien
- **Python 3.x**
- **Tkinter** — GUI-Framework (mit ttkbootstrap für das Design)
- **pgpy** — OpenPGP-Verschlüsselung
- **cryptography** — SSL-Zertifikatsgenerierung
- **Pillow** — (optional) für Symbole

## Wie Sie mitwirken können
1. Forken und klonen Sie das Repository.
2. Erstellen Sie eine virtuelle Umgebung und installieren Sie die Abhängigkeiten.
3. Halten Sie sich an PEP8 und behalten Sie eine modulare Codebasis bei.
4. Dokumentieren Sie neue Funktionen und aktualisieren Sie `CHANGELOG.md`.
5. Fügen Sie nach Möglichkeit Tests hinzu oder aktualisieren Sie sie.
6. Öffnen Sie einen Pull-Request mit einer klaren Beschreibung.

## Hinzufügen von Funktionen
- Um neue Algorithmen (z.B. ECC, Ed25519) hinzuzufügen, erweitern Sie die Schlüsselgenerierungslogik in `main_window.py`.
- Für neue Benutzeroberflächenkomponenten fügen Sie Widgets in `gui/` hinzu und trennen Sie die Logik von der Benutzeroberfläche.
- Verwenden Sie `ttkbootstrap`-Stile für ein einheitliches Erscheinungsbild.

## Tests
- Fügen Sie Tests für neue Funktionen und Fehlerbehebungen hinzu.
- Manuelles Testen: Führen Sie `python main.py` aus und nutzen Sie alle GUI-Funktionen.
- (Optional) Integrieren Sie CI/CD für automatisierte Tests.

## Codestil
- Halten Sie sich an PEP8.
- Verwenden Sie Docstrings für öffentliche Funktionen/Klassen.
- Trennen Sie Benutzeroberfläche und Logik so weit wie möglich.

## Protokollierung und Fehlerbehebung
- Verwenden Sie `log_info(msg)`, `log_warning(msg)`, `log_error(msg)` überall im Code für benutzerdefinierte Protokolleinträge.
- Alle Protokolle werden in `traceback.log` gespeichert und in der Protokollanzeige angezeigt.
- Die Protokollanzeige unterstützt die Filterung nach ALLE, INFO, WARNUNG, FEHLER.
- Unbehandelte Ausnahmen werden automatisch protokolliert und in der Protokollanzeige angezeigt (mit Fehlerbericht).

## Unterstützung und Fragen
- Öffnen Sie bei Fehlern oder Funktionswünschen ein Issue auf GitHub.
- Weitere Informationen zu Kontakt und Beiträgen finden Sie in `README.md`.

---

## Fortgeschrittene Themen

### API-Referenz

Die Anwendung ist modular aufgebaut: Die Kernlogik befindet sich in `struttura/`, die Benutzeroberfläche in `gui/`.

**Wichtige Klassen und Funktionen:**
- `MainWindow` (`gui/main_window.py`): Hauptlogik der Benutzeroberfläche und Ereignisbehandlung.
- `gen_key`, `export_pubkey`, `clear_fields` usw.: Methoden für kryptografische Vorgänge.
- `Help`, `About`, `LogViewer` usw.: Dialoge und Hilfsfunktionen in `struttura/`.
- `get_version()` (`struttura/version.py`): Gibt die aktuelle Versionszeichenfolge zurück.

Weitere Informationen finden Sie in den Dokumentationszeichenfolgen im Code und in `docs/user_guide.md` für den Nutzungsablauf.

### Erweiterungsbeispiele

#### Hinzufügen eines neuen Schlüsselalgorithmus
1. Suchen Sie in `gui/main_window.py` nach der Auswahlliste für Algorithmen.
2. Fügen Sie Ihren neuen Algorithmus (z.B. ECC, Ed25519) zu den Dropdown-Optionen hinzu.
3. Implementieren Sie die Behandlung des neuen Algorithmus in der Schlüsselgenerierungslogik mit `pgpy`.
4. Testen Sie gründlich und aktualisieren Sie die Dokumentation.

#### Hinzufügen eines benutzerdefinierten Widgets
1. Erstellen Sie Ihr Widget in `gui/widgets.py` oder einer neuen Datei.
2. Importieren und verwenden Sie es im Hauptfenster oder einem Dialog.
