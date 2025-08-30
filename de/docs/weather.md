---
lang: de
lang-niv: fonto
lang-ref: 022-jbk
layout: doc
order: 13
title: 'Wetter'
---

# Wetter-App Dokumentation (v1.6.0)

Willkommen zur Dokumentation der Wetter-App! Diese Anwendung bietet Echtzeit-Wetterinformationen und Vorhersagen von mehreren Wetterdatenanbietern.

## Funktionen

- 🌦️ Aktuelle Wetterbedingungen mit detaillierten Messwerten
- 📅 7-Tage-Wettervorhersage mit stündlicher Aufschlüsselung
- 📖 Integrierter Markdown-Dokumentationsbetrachter
- 📊 Anwendungsprotokollbetrachter für Diagnosen
- 🌍 Mehrere Wetterdatenanbieter
- 🌐 Mehrsprachige Unterstützung
- ⭐ Favorisierte Orte mit erweitertem Verlauf
- ⚙️ Anpassbare Einstellungen und Designs

## Aktuelle Aktualisierungen

Eine detaillierte Liste der Änderungen finden Sie in der Datei [CHANGELOG.md](CHANGELOG.md).

## Erste Schritte

1. [Installationsanleitung](installation.md) - So installieren und richten Sie die Anwendung ein
2. [Benutzerhandbuch](usage.md) - So verwenden Sie die Anwendung
3. [Konfiguration](configuration.md) - So konfigurieren Sie die Anwendung

## Fortgeschrittene Themen

- [Wetteranbieter](providers.md) - Informationen zu unterstützten Wetterdatenanbietern
- [Übersetzungen](translations.md) - So fügen Sie Übersetzungen hinzu oder ändern sie
- [Entwicklungsleitfaden](development.md) - So tragen Sie zum Projekt bei
- [Fehlerbehebung](troubleshooting.md) - Häufige Probleme und Lösungen

## Unterstützung

Bei Unterstützungsanfragen öffnen Sie bitte ein Issue in unserem [GitHub-Repository](https://github.com/Nsfr750/weather).

## Lizenz

Dieses Projekt ist unter der GPLv3-Lizenz lizenziert - siehe die [LIZENZ](https://github.com/Nsfr750/weather/blob/main/LICENSE) für Details.

# Benutzerhandbuch

## Erste Schritte

1. **Starten der Anwendung**
   - Doppelklicken Sie auf das Anwendungssymbol oder führen Sie sie über die Befehlszeile aus
   - Das Hauptfenster öffnet sich mit dem Wetter am Standardstandort
   - Beim ersten Start werden Sie durch die Ersteinrichtung geführt

2. **Nach einem Ort suchen**
   - Geben Sie einen Städtenamen in das Suchfeld ein
   - Drücken Sie die Eingabetaste oder klicken Sie auf die Suchschaltfläche (🔍)
   - Fügen Sie für genauere Ergebnisse den Ländercode hinzu (z.B. "Berlin, DE")
   - Klicken Sie mit der rechten Maustaste auf die Karte, um einen Ort auszuwählen

## Hauptoberfläche

### Wetteranzeige

- **Aktuelles Wetter**: Zeigt Temperatur, Bedingungen und zusätzliche Details
  - Tippen Sie auf eine beliebige Maßeinheit, um zwischen Einheiten umzuschalten (z.B. °C/°F, km/h/Meilen pro Stunde)
  - Fahren Sie mit der Maus über Symbole, um weitere Informationen anzuzeigen

- **7-Tage-Vorhersage**: Zeigt die Wettervorhersage für die nächsten 7 Tage
  - Klicken Sie auf einen Tag, um stündliche Vorhersagen anzuzeigen
  - Farbkodierte Niederschlagswahrscheinlichkeit
  - Enthält Temperaturbereiche und Wetterbedingungen für jeden Tag

- **Wetterdetails**: Enthält:
  - Gefühlte Temperatur
  - Luftfeuchtigkeit und Taupunkt
  - Windgeschwindigkeit und -richtung
  - Luftdruck und Sichtweite
  - UV-Index und Luftqualität
  - Sonnenauf- und -untergangszeiten

### Navigation

- **Suchleiste**: Finden Sie das Wetter für jeden Ort
  - Letzte Suchanfragen werden automatisch gespeichert
  - Suche nach Städtenamen, Postleitzahlen oder Koordinaten

- **Design-Umschalter**: Wechseln Sie zwischen hellem, dunklem oder Systemdesign

- **Menüleiste**: Zugriff auf zusätzliche Funktionen und Einstellungen
  - Datei: Neues Fenster, Einstellungen, Beenden
  - Ansicht: UI-Elemente ein-/ausblenden, Daten aktualisieren, Wetterkarten & Radar
  - Favoriten: Gespeicherte Orte verwalten
  - Hilfe: Dokumentationsbetrachter, Protokollbetrachter, Info, Nach Updates suchen

## Wetterkarten & Radar

Die Funktion Wetterkarten & Radar bietet interaktive Visualisierungen von Wettermustern und -bedingungen.

### Aufrufen der Wetterkarten

1. Klicken Sie in der Menüleiste auf **Ansicht**
2. Wählen Sie **Wetterkarten & Radar**
3. Der Wetterkarten-Dialog öffnet sich mit mehreren Registerkarten

### Funktionen

#### Radar-Registerkarte
- **Kartentyp**: Wechseln Sie zwischen verschiedenen Grundkarten (OpenStreetMap, OpenTopoMap, Stamen Terrain)
- **Ebene**: Schalten Sie zwischen Radar- und Satellitenüberlagerungen um
- **Suche**: Finden Sie Orte nach Namen oder Koordinaten

#### Temperatur-Registerkarte
- Zeigen Sie Temperaturschwankungen in verschiedenen Regionen an
- Schalten Sie zwischen Celsius und Fahrenheit um
- Passen Sie die Deckkraft der Temperaturüberlagerung an

#### Niederschlags-Registerkarte
- Sehen Sie aktuelle und vorhergesagte Niederschläge
- Schalten Sie zwischen verschiedenen Niederschlagsebenen um
- Zeigen Sie Regen, Schnee und andere Niederschlagsarten an

#### Wind-Registerkarte
- Visualisieren Sie Windgeschwindigkeit und -richtung
- Schalten Sie zwischen Windfahnen oder Strömungslinien um
- Stellen Sie die Windgeschwindigkeitseinheiten ein (km/h, m/s, mph, Knoten)

### Verwendung der Karte
- **Zoomen**: Verwenden Sie das Mausrad oder die +/- Schaltflächen
- **Verschieben**: Klicken und ziehen Sie die Karte
- **Suchen**: Geben Sie einen Ort in das Suchfeld ein und drücken Sie die Eingabetaste
- **Ebenen**: Schalten Sie verschiedene Wetterebenen mit den Steuerelementen um
- **Vollbild**: Klicken Sie auf die Vollbildschaltfläche für eine größere Ansicht

### Tipps
- Die Karte zentriert sich automatisch auf Ihren aktuellen Standort, wenn die Standortdienste aktiviert sind
- Klicken Sie auf die Karte, um detaillierte Wetterinformationen für diesen Ort zu erhalten
- Verwenden Sie die Zeitachsensteuerung, um Vorhersagedaten für verschiedene Zeiten anzuzeigen
- Klicken Sie mit der rechten Maustaste auf die Karte, um eine Markierung zu setzen oder Koordinaten abzurufen

## Funktionen

### Favoriten

- **Zu Favoriten hinzufügen**: Klicken Sie auf den Stern (☆), um einen Ort zu speichern

- **Favoriten anzeigen**: Greifen Sie auf gespeicherte Orte über das Favoriten-Menü zu
  - Sortieren Sie Favoriten per Drag & Drop
  - Rechtsklick für Schnellaktionen

- **Favoriten synchronisieren**: Aktivieren Sie die Cloud-Synchronisierung in den Einstellungen

- **Aus Favoriten entfernen**: Klicken Sie auf den ausgefüllten Stern (★) zum Entfernen

### Einstellungen

1. Klicken Sie auf das Zahnradsymbol (⚙️) oder gehen Sie zu Menü > Einstellungen
2. Konfigurieren Sie Optionen wie:
   - **Allgemein**: Sprache, Design, Einheiten
   - **Wetter**: Anbietereinstellungen, Aktualisierungsintervall
   - **Anzeige**: Layout, Animationen, Schriftgröße
   - **Benachrichtigungen**: Wetterwarnungen, Regenwarnungen
   - **Erweitert**: Cache, Protokollierung, Entwickleroptionen
3. Klicken Sie auf "Speichern", um die Änderungen zu übernehmen

### Befehlszeilenschnittstelle

```bash
# Grundlegende Verwendung
weather-app [Ort] [Optionen]

# Beispiele
weather-app "Berlin, DE"
weather-app --provider openweathermap --units metric
weather-app --config ~/.config/weather/config.ini

# Optionen
  -h, --help            Hilfenachricht anzeigen und beenden
  -v, --version         Versionsinformationen anzeigen
  -c, --config DATEI    Konfigurationsdatei angeben
  -d, --debug           Debug-Modus aktivieren
  --provider ANBIETER   Wetteranbieter festlegen
  --units {metric,imperial}
                        Einheitensystem festlegen
  --lang SPRACHE        Sprachcode festlegen
  --theme {hell,dunkel,system}
                        Farbdesign festlegen
  --no-gui              Im Konsolenmodus ausführen
```

## Tastenkombinationen

### Globale Tastenkombinationen

| Tastenkombination | Aktion |
|-------------------|--------|
| `Strg + F` | Fokus auf die Suchleiste setzen |
| `Strg + ,` | Einstellungen öffnen |
| `Strg + Q` | Anwendung beenden |
| `F1` | Hilfe anzeigen |
| `Esc` | Dialoge schließen oder Suche zurücksetzen |
| `F5` | Wetterdaten aktualisieren |
| `Strg + R` | Alle Daten aktualisieren |
| `Strg + W` | Aktuelles Fenster schließen |
| `Strg + N` | Neues Fenster |

### Navigations-Tastenkombinationen

| Tastenkombination | Aktion |
|-------------------|--------|
| `Strg + Tab` | Zwischen Orten wechseln |
| `Strg + F` | Favoriten ein-/ausblenden |
| `Strg + L` | Ortsliste ein-/ausblenden |
| `Strg + M` | Kartenansicht ein-/ausblenden |

## Tipps & Tricks

- **Rechtsklick** auf eine Wetterkarte für Schnellaktionen
- **Doppelklicken** Sie auf die Temperatur, um zwischen Celsius und Fahrenheit zu wechseln
- **Mittlere Maustaste** auf der Karte, um einen benutzerdefinierten Ort festzulegen
- Verwenden Sie das **Mausrad** in der Vorhersage, um durch die Stunden zu scrollen
- **Ziehen und Ablegen** zum Neusortieren von Favoriten
- **Heften** Sie das Fenster an, um es über anderen Anwendungen zu behalten
- Verwenden Sie das **Systemtray-Symbol** für schnellen Zugriff

### Dokumentationsbetrachter

- Greifen Sie über das Hilfemenü auf die integrierte Markdown-Dokumentation zu
- Durchsuchen Sie die umfassende Dokumentation
- Nutzen Sie die Suchfunktion, um bestimmte Themen zu finden
- Zoomen Sie hinein/heraus für bessere Lesbarkeit
- Inhaltsverzeichnis für einfache Navigation

### Protokollbetrachter

- Zeigen Sie Anwendungsprotokolle über das Hilfemenü an
- Filtern Sie Protokolle nach Ebene (Debug, Info, Warnung, Fehler)
- Durchsuchen Sie die Protokollmeldungen
- Kopieren Sie Protokolle zur Fehlerbehebung in die Zwischenablage

### Wetterkarten
- Greifen Sie über das Ansichtsmenü auf Wetterkarten zu
- Interaktive Karte mit mehreren Ebenen:
  - Temperatur
  - Niederschlag
  - Windgeschwindigkeit
  - Bewölkung
- Bewegen Sie sich und zoomen Sie, um verschiedene Regionen zu erkunden
- Klicken Sie auf die Karte, um Wetterinformationen für diesen Ort zu erhalten

## Fehlerbehebung

Wenn Sie auf Probleme stoßen:
1. Überprüfen Sie Ihre Internetverbindung
2. Überprüfen Sie Ihre API-Schlüssel in den Einstellungen
3. Versuchen Sie, zu einem anderen Wetteranbieter zu wechseln
4. Überprüfen Sie die Anwendungsprotokolle auf Fehler
5. Starten Sie die Anwendung neu
6. Setzen Sie die Einstellungen bei Bedarf zurück

Zusätzliche Hilfe finden Sie in unserem [GitHub-Repository](https://github.com/Nsfr750/weather) oder im [Fehlerbehebungsleitfaden](troubleshooting.md).

## Feedback

Wir freuen uns über Ihr Feedback! Teilen Sie uns bitte mit:
- Welche Funktionen Sie sich wünschen
- Auf welche Fehler Sie stoßen
- Wie Ihre Erfahrung mit der Anwendung ist

Sie können Feedback über die Anwendung (Hilfe > Feedback senden) oder auf unserer [GitHub Issues](https://github.com/Nsfr750/weather/issues) Seite einreichen.

# Fehlerbehebungsleitfaden

Dieser Leitfaden hilft Ihnen, häufige Probleme zu beheben, die bei der Verwendung der Wetter-App auftreten können.

## Inhaltsverzeichnis
- [Häufige Probleme](#häufige-probleme)
- [Protokolldateien](#protokolldateien)
- [Debugging](#debugging)
- [Leistungsprobleme](#leistungsprobleme)
- [Häufig gestellte Fragen](#häufig-gestellte-fragen)
- [Hilfe erhalten](#hilfe-erhalten)

## Häufige Probleme

### 1. Die Anwendung startet nicht

**Symptome**:
- Die Anwendung stürzt sofort nach dem Start ab
- Sie sehen eine Fehlermeldung über fehlende Abhängigkeiten
- Das Anwendungsfenster wird nicht angezeigt

**Lösungen**:
1. **Systemanforderungen überprüfen**:
   - Stellen Sie sicher, dass Python 3.10 oder höher installiert ist
   - Überprüfen Sie, ob alle Systemabhängigkeiten installiert sind
   - Überprüfen Sie den Festplattenspeicher und die Berechtigungen

2. **Abhängigkeiten neu installieren**:
   ```bash
   # Aktivieren Sie zuerst Ihre virtuelle Umgebung
   pip install --upgrade -r requirements.txt
   ```

3. **Auf Konflikte mit anderer Software prüfen**:
   - Deaktivieren Sie vorübergehend Antivirenprogramm/Firewall
   - Schließen Sie andere Anwendungen, die in Konflikt stehen könnten

4. **Konfiguration zurücksetzen**:
   ```bash
   # Sichern Sie zuerst Ihre Konfiguration
   mv ~/.config/WeatherApp/config.ini ~/.config/WeatherApp/config.ini.bak
   ```

### 2. Keine Wetterdaten werden angezeigt

**Symptome**:
- Die App öffnet sich, zeigt aber "Keine Daten verfügbar" an
- Die Wetterinformationen werden nicht aktualisiert
- Der Standort kann nicht gefunden werden

**Lösungen**:
1. **Internetverbindung überprüfen**:
   - Stellen Sie sicher, dass Ihr Gerät mit dem Internet verbunden ist
   - Versuchen Sie, eine Website in Ihrem Browser zu öffnen

2. **API-Schlüssel überprüfen**:
   - Überprüfen Sie, ob Ihr API-Schlüssel gültig und nicht abgelaufen ist
   - Stellen Sie sicher, dass der API-Schlüssel die richtigen Berechtigungen hat
   - Versuchen Sie, den API-Schlüssel neu zu generieren

3. **Anbieterstatus**:
   - Überprüfen Sie, ob der Wetterdienst Ausfälle hat
   - Versuchen Sie, zu einem anderen Wetteranbieter zu wechseln

4. **Standortdienste**:
   - Stellen Sie sicher, dass die Standortdienste aktiviert sind
   - Versuchen Sie, den Standort manuell einzugeben

### 3. Hohe CPU- oder Speichernutzung

**Symptome**:
- Die Anwendung wird langsam oder reagiert nicht mehr
- Der Lüfter Ihres Computers läuft auf Hochtouren
- Andere Anwendungen werden langsam

**Lösungen**:
1. **Aktualisierungsintervall erhöhen**:
   - Erhöhen Sie das Aktualisierungsintervall in Einstellungen > Wetter
   - Deaktivieren Sie automatische Standortaktualisierungen, wenn nicht benötigt

2. **Animationen deaktivieren**:
   - Gehen Sie zu Einstellungen > Anzeige
   - Schalten Sie "Animationen aktivieren" aus

3. **Cache leeren**:
   ```bash
   # Linux/macOS
   rm -rf ~/.cache/WeatherApp
   
   # Windows
   rmdir /s /q %LOCALAPPDATA%\WeatherApp\Cache
   ```

4. **Auf Speicherlecks prüfen**:
   - Überwachen Sie die Speichernutzung im Task-Manager
   - Melden Sie anhaltende Speicherzunahmen

## Protokolldateien

Protokolldateien enthalten detaillierte Informationen zu Anwendungsereignissen und -fehlern. Sie sind für die Fehlerbehebung unerlässlich.

### Protokollorte

- **Linux/macOS**: `~/.local/share/WeatherApp/logs/`
- **Windows**: `%APPDATA%\WeatherApp\logs\`
- **macOS**: `~/Library/Logs/WeatherApp/`

### Protokollebenen

- **DEBUG**: Detaillierte Informationen zur Fehlersuche
- **INFO**: Allgemeine Anwendungsereignisse
- **WARNUNG**: Möglicherweise problematische Situationen
- **FEHLER**: Fehler, die die Anwendung möglicherweise weiterlaufen lassen
- **KRITISCH**: Schwere Fehler, die zum Absturz der Anwendung führen

### Protokolle anzeigen

1. **Aus der Anwendung**:
   - Gehen Sie zu Hilfe > Protokolle anzeigen
   - Filtern Sie nach Protokollebene
   - Suchen Sie nach bestimmten Begriffen

2. **Über die Befehlszeile**:
   ```bash
   # Linux/macOS
   tail -f ~/.local/share/WeatherApp/logs/app.log
   
   # Windows
   Get-Content -Path "$env:APPDATA\WeatherApp\logs\app.log" -Wait
   ```

## Häufig gestellte Fragen

### Wie wechsle ich zwischen metrischen/imperialen Einheiten?

1. Gehen Sie zu Einstellungen > Allgemein
2. Wählen Sie Ihr bevorzugtes Einheitensystem
3. Klicken Sie auf "Speichern"

### Wie melde ich einen Fehler?

1. Überprüfen Sie zuerst, ob der Fehler nicht bereits gemeldet wurde
2. Sammeln Sie folgende Informationen:
   - Version der Anwendung
   - Betriebssystem und Version
   - Schritte zur Reproduktion des Fehlers
   - Genauer Fehlertext
   - Relevante Protokolldateien
3. Erstellen Sie ein neues Issue auf [GitHub](https://github.com/Nsfr750/weather/issues)

## Hilfe erhalten

Wenn Sie keine Lösung für Ihr Problem finden:

1. **Dokumentation durchsuchen**:
   - [Benutzerhandbuch](usage.md)
   - [Konfiguration](configuration.md)
   - [API-Dokumentation](api.md)

2. **Bestehende Probleme durchsuchen**:
   - [GitHub Issues](https://github.com/Nsfr750/weather/issues)
   - [Häufig gestellte Fragen](faq.md)

3. **Hilfe anfordern**:
   - Erstellen Sie ein neues Issue auf GitHub
   - Fügen Sie so viele Details wie möglich bei
   - Hängen Sie bei Bedarf Protokolldateien an

## Übersetzung

Die Anwendung unterstützt mehrere Sprachen. So fügen Sie eine neue Sprache hinzu:

1. Erstellen Sie eine neue Übersetzungsdatei im Ordner `translations/`
2. Fügen Sie Übersetzungen für alle Zeichenfolgen in der Datei `translations/en.json` hinzu
3. Fügen Sie die Sprache zum Sprachmenü hinzu, indem Sie diese Schlüssel einfügen:
   - `language_menu`: Der Menütitel (z.B. "Sprache")
   - `language_tip`: QuickInfo-Text für das Sprachmenü (z.B. "Anwendungssprache auswählen")

Beispiel für Deutsch (`de.json`):
```json
{
  "language_menu": "Sprache",
  "language_tip": "Anwendungssprache auswählen",
  "settings": "Einstellungen",
  "weather": "Wetter",
  "forecast": "Vorhersage",
  "map": "Karte",
  "favorites": "Favoriten",
  "help": "Hilfe"
}
```
