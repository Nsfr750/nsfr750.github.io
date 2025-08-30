---
lang: de
lang-niv: fonto
lang-ref: 010-jbk
layout: doc
order: 1
title: '3D Filament Manager'
---

# 3D Filament Manager

![3D Filament Manager](assets/logo.png)

Eine Desktop-Anwendung zur Verwaltung Ihres 3D-Druckfilamentbestands. Behalten Sie Materialien, Farben, Verbrauch, Kosten und Slicer-Einstellungen an einem Ort im Überblick.

## ✨ Funktionen

* **🌐 Mehrsprachige Unterstützung**: Verfügbar auf Englisch und Italienisch
* **🎨 Moderne Benutzeroberfläche**: Übersichtliches Design mit Emoji-Symbolen und Designunterstützung (Hell-/Dunkelmodus)
* **📊 Umfassende Filamentverwaltung**:
  * Speichern Sie detaillierte Filamentinformationen (Marke, Material, Farbe, Durchmesser usw.)
  * Verfolgen Sie den Filamentverbrauch und die verbleibende Menge
  * Berechnen Sie Materialkosten
  * Preisverfolgung und -verlauf
  * Interaktive Preisanlyse mit Visualisierungen
  * Anbieterpreisvergleich
* **⚙️ Slicer-Integration**:
  * Speichern und Verwalten von Slicer-Profilen (Cura, PrusaSlicer, eQuidiSlicer)
  * Benutzerdefinierte Druckprofile für verschiedene Drucker
* **🔍 Erweiterte Suche & Filterung**:
  * Suche nach beliebigen Filamenteigenschaften
  * Sortierung nach beliebiger Spalte
  * Filterung nach Materialtyp, Farbe oder benutzerdefinierten Tags
* **📂 Import/Export**:
  * Sichern und Wiederherstellen Ihrer Filamentbibliothek
  * Profile mit anderen teilen
  * Unterstützung für Massenimport/-export
* **🔒 Datensicherheit**:
  * Einstellungen werden im Verzeichnis `config/` gespeichert
  * Keine Internetverbindung erforderlich
  * Lokale Datenspeicherung

## 🚀 Anforderungen

* Python 3.8+
* Erforderliche Pakete (werden automatisch installiert):
  * `lxml` - Schnelle XML-Verarbeitung
  * `pillow` - Bildverarbeitung für Symbole
  * `matplotlib` - Datenvisualisierung für die Preisanlyse

## 🛠️ Installation

### Voraussetzungen

* Python 3.8 oder höher
* Git (optional, für die Entwicklung)

### Installationsschritte

1. **Repository klonen** (oder als ZIP herunterladen):

   ```bash
   git clone https://github.com/Nsfr750/3D_Filament_Manager.git
   cd 3D_Filament_Manager
   ```

2. **Virtuelle Umgebung erstellen und aktivieren** (empfohlen):

   ```bash
   # Unter Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # Unter macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Abhängigkeiten installieren**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Anwendung starten**:

   ```bash
   python main.py
   ```

### Datenspeicherung

* Filamentprofile werden im Verzeichnis `fdm/` gespeichert
* Anwendungseinstellungen werden im Verzeichnis `config/` gespeichert
* Protokolle werden im Verzeichnis `logs/` geschrieben

## 🤝 Mitwirken

Wir freuen uns über Beiträge! So können Sie helfen:

* Melden Sie Fehler, indem Sie ein [Issue](https://github.com/Nsfr750/3D_Filament_Manager/issues) öffnen
* Schlagen Sie neue Funktionen oder Verbesserungen vor
* Reichen Sie Pull-Requests mit Codeänderungen ein
* Helfen Sie bei der Verbesserung der Dokumentation
* Übersetzen Sie die Anwendung in neue Sprachen

### Entwicklungsumgebung

1. Forken Sie das Repository
2. Erstellen Sie einen Feature-Branch (`git checkout -b feature/tolle-funktion`)
3. Nehmen Sie Ihre Änderungen vor (`git commit -m 'Füge tolle Funktion hinzu'`)
4. Übertragen Sie die Änderungen in das Repository (`git push origin feature/tolle-funktion`)
5. Erstellen Sie einen Pull-Request

### Code-Stil

* Bitte halten Sie sich an die [PEP 8](https://www.python.org/dev/peps/pep-0008/)-Richtlinien
* Verwenden Sie Typ-Hinweise für bessere Code-Klarheit
* Schreiben Sie Docstrings für alle öffentlichen Funktionen und Klassen

## 📜 Lizenz

Dieses Projekt steht unter der **GNU General Public License v3.0**. Weitere Informationen finden Sie in der [LIZENZ](LICENSE)-Datei.

## 🙏 Unterstützung

Wenn Sie dieses Projekt nützlich finden, erwägen Sie bitte eine Unterstützung der Entwicklung:

* ⭐ Vergeben Sie einen Stern für das Repository
* 🐛 Melden Sie Probleme
* 💡 Schlagen Sie neue Funktionen vor
* 💰 [Unterstützen Sie das Projekt auf GitHub](https://github.com/sponsors/Nsfr750)

## 📞 Kontakt

* GitHub: [@Nsfr750](https://github.com/Nsfr750)
* E-Mail: nsfr750@yandex.com

---

### Unterstützen Sie den Entwickler

Wenn Sie diese Anwendung nützlich finden, erwägen Sie bitte eine Unterstützung des Entwicklers:

* **PayPal**: [https://paypal.me/3dmega](https://paypal.me/3dmega)
* **GitHub**: [https://github.com/Nsfr750](https://github.com/Nsfr750)
