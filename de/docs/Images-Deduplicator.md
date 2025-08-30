---
lang: de
lang-niv: fonto
lang-ref: 014-jbk
layout: page
title: 'Bild-Duplikaterkennung'
---

# Bild-Duplikaterkennung

Die Bild-Duplikaterkennung ist eine leistungsstarke Python-Anwendung zur effizienten Verwaltung und Entfernung doppelter Bilder. Mit der Wand-Bibliothek (ImageMagick) für die Bildverarbeitung bietet dieses Tool fortschrittliche visuelle Vergleichstechniken zur genauen Identifizierung und Verwaltung doppelter Bilder.

## Hauptmerkmale

- **Fortgeschrittene Bildverarbeitung**: Nutzt Wand/ImageMagick für optimale Unterstützung verschiedener Bildformate
- **Visuelle Duplikaterkennung**: Perzeptuelles Hashing zur Identifizierung visuell ähnlicher Bilder
- **Umfassende Formatunterstützung**: Unterstützt alle gängigen Bildformate inklusive JPEG, PNG, WEBP, PSD und mehr
- **Intuitive Benutzeroberfläche**: Benutzerfreundliche grafische Oberfläche mit Hell-/Dunkelmodus
- **Mehrsprachige Unterstützung**: Integrierte Internationalisierung mit Englisch und Italienisch
- **Stapelverarbeitung**: Effiziente Verarbeitung Tausender Bilder
- **Vorschau & Vergleich**: Gegenüberstellung von Bildern vor der Bearbeitung
- **Sichere Operationen**: Verschieben in den Papierkorb anstatt sofortiges Löschen
- **Detaillierte Protokollierung**: Umfassende Aufzeichnung aller Aktionen

## Systemanforderungen

- **Python**: 3.8 oder höher (empfohlen: 3.10+)
- **ImageMagick**: Erforderlich für die Bildverarbeitung mit Wand
  - Windows: Installation über [ImageMagick Windows](https://imagemagick.org/script/download.php#windows)
  - macOS: `brew install imagemagick`
  - Linux: `sudo apt-get install libmagickwand-dev`
- **Arbeitsspeicher**: Mindestens 4 GB, empfohlen 8 GB+ für große Bildersammlungen
- **Speicherplatz**: Ausreichend Platz für die zu verarbeitenden Bilder + temporäre Dateien
- **Betriebssysteme**:
  - Windows 10/11
  - macOS 10.15+
  - Linux mit X11/Wayland

## Warum Wand/ImageMagick?

Die Bild-Duplikaterkennung verwendet Wand (eine Python-Schnittstelle zu ImageMagick) aus folgenden Gründen:

- Bessere Unterstützung verschiedener Formate, einschließlich PSD, GIF und BMP
- Verbessertes Speichermanagement für große Bilder
- Konsistenteres Verhalten über verschiedene Plattformen hinweg
- Erweiterte Bildbearbeitungsmöglichkeiten
- Aktive Wartung und Sicherheitsupdates

## Verwendung

### Hauptoberfläche

Die Anwendung bietet eine moderne, benutzerfreundliche Oberfläche mit folgenden Hauptkomponenten:

1. **Menüleiste**: Zugriff auf alle Anwendungsfunktionen und -einstellungen
2. **Werkzeugleiste**: Schnellzugriff auf häufig verwendete Funktionen
3. **Ordner-Navigator**: Durchsuchen und Auswählen von Verzeichnissen zum Scannen
4. **Vorschaufenster**: Gegenüberstellung von Bildern
5. **Ergebnisbereich**: Anzeige gefundener Duplikate mit Ähnlichkeitswerten
6. **Statusleiste**: Fortschrittsanzeige und Systeminformationen

### Grundlegender Arbeitsablauf

1. **Quellordner auswählen**
   - Klicken Sie auf "Ordner öffnen" oder nutzen Sie `Datei > Ordner öffnen`
   - Die Anwendung sucht nach unterstützten Bildformaten
   - Unterstützte Formate: JPEG, PNG, WEBP, PSD, BMP, GIF und mehr (über Wand/ImageMagick)

2. **Sucheinstellungen anpassen**
   - Ähnlichkeitsschwelle anpassen (Standard: 90%)
   - Minimale Bildgröße festlegen
   - Zu vergleichende Bildeigenschaften auswählen (Größe, Datum, Inhalts-Hash)

3. **Suche starten**
   - Klicken Sie auf "Suche starten", um mit der Duplikaterkennung zu beginnen
   - Der Fortschritt wird in der Statusleiste angezeigt
   - Suche kann jederzeit pausiert oder gestoppt werden

4. **Ergebnisse überprüfen**
   - Duplikatgruppen werden mit Vorschaubildern angezeigt
   - Sortierung nach Dateigröße, Datum oder Ähnlichkeitswert möglich
   - Nutzen Sie die Gegenüberstellungsfunktion zur Überprüfung

5. **Duplikate verwalten**
   - Bilder zum Behalten oder Löschen auswählen
   - Duplikate in den Papierkorb verschieben (wiederherstellbar) oder endgültig löschen
   - Ergebnisse nach CSV/JSON exportieren

### Erweiterte Funktionen

#### Stapelverarbeitung

- Mehrere Ordner nacheinander verarbeiten
- Suchprofile speichern und laden
- Automatische Suche planen

#### Intelligente Auswahl

- Automatische Auswahl nach Kriterien (älteste, kleinste, etc.)
- Beibehaltung der höchsten Auflösung
- Bilder mit bestimmten Namensmustern erhalten

#### Bildvergleichswerkzeuge

- Gegenüberstellungs- und Überlagerungsmodus
- Synchronisiertes Zoomen und Bewegen
- Histogramm- und EXIF-Datenvergleich

#### Benutzerdefinierte Filter

- Filter nach Bildabmessungen
- Filter nach Erstellungs-/Änderungsdatum
- Filter nach Bildformat oder Farbprofil

#### Wand/ImageMagick-Integration

- Erweterte Formatunterstützung
- Bessere Handhabung von Farbprofilen und Metadaten
- Unterstützung für RAW-Formate (wenn in ImageMagick aktiviert)

### Tastenkombinationen

| Tastenkombination | Aktion                          |
|------------------|---------------------------------|
| `Strg+O`        | Ordner öffnen                   |
| `Strg+F`        | Neue Suche starten              |
| `Leertaste`     | Aktuelles Bild auswählen/abwählen |
| `Entf`          | Auswahl in den Papierkorb verschieben |
| `Strg+Z`        | Letzte Aktion rückgängig machen |
| `F5`            | Ansicht aktualisieren           |

## Leistungsoptimierung

### Für große Sammlungen

- Nutzen Sie den "Schnellvergleich" für die erste Filterung
- Erhöhen Sie die Mindestdateigröße, um Vorschaubilder zu überspringen
- Planen Sie die Suche für große Sammlungen außerhalb der Hauptnutzungszeiten

### Speicherverwaltung

- Schließen Sie speicherintensive Anwendungen
- Passen Sie ggf. die Ressourcenbegrenzungen von ImageMagick an (siehe Installation)
- Verarbeiten Sie Bilder in kleineren Stapeln

### Speicherplatzbedarf

- Stellen Sie ausreichend freien Speicherplatz für temporäre Dateien sicher
- Verarbeiten Sie Bilder nach Möglichkeit direkt vom Quelllaufwerk
- Nutzen Sie eine schnelle SSD für bessere Leistung

## Fehlerbehebung

### Langsame Leistung

- Überprüfen Sie die ImageMagick-Richtlinieneinstellungen (siehe Installation)
- Reduzieren Sie die Anzahl gleichzeitiger Operationen
- Deaktivieren Sie die Echtzeitvorschau für große Sammlungen

### Fehlende Bilder

- Überprüfen Sie, ob das Bildformat von ImageMagick unterstützt wird
- Überprüfen Sie die Dateiberechtigungen
- Suchen Sie nach Fehlermeldungen im Protokoll

### Unerwartete Ergebnisse

- Passen Sie die Ähnlichkeitsschwelle an
- Überprüfen Sie, ob die Filter zu restriktiv sind
- Stellen Sie sicher, dass die Bildmetadaten korrekt gelesen werden

## Konfiguration

### Hauptoptionen

#### Vergleichsgenauigkeit

- **Genauigkeitsstufe (1-100)**:
  - Niedrigere Werte finden mehr Duplikate
  - Höhere Werte finden nur nahezu identische Duplikate

#### Mindestgrößen

- **Bilder kleiner als ignorieren**:
  - Minimale Breite (Pixel)
  - Minimale Höhe (Pixel)
  - Minimale Größe (KB)

#### Unterstützte Formate

- **Erlaubte Erweiterungen**:
  - .jpg, .jpeg
  - .png
  - .gif
  - .bmp
  - .webp

#### Ausgeschlossene Ordner

- **Liste der zu ignorierenden Ordner**:
  - Systemordner
