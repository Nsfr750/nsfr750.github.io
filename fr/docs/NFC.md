---
lang: fr
lang-niv: fonto
lang-ref: 016-jbk
layout: doc
order: 6
title: 'NFC'
---

# 🚀 Application de Lecture/Écriture NFC

[![Licence : GPL v3](https://img.shields.io/badge/Licence-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Style de code : black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Une application puissante basée sur PySide6 pour lire et écrire sur divers types d'étiquettes NFC avec des fonctionnalités avancées et une interface utilisateur intuitive.

## Installation

### Prérequis

- Python 3.9 ou supérieur
- Lecteur NFC matériel (ACR122U, ACR1252U, etc.)

### Démarrage Rapide

1. Clonez le dépôt :

   ```bash
   git clone https://github.com/Nsfr750/NFC.git
   cd NFC
   ```

2. Créez et activez un environnement virtuel :

   ```bash
   python -m venv venv
   .\venv\Scripts\activate  # Windows
   source venv/bin/activate  # Linux/Mac
   ```

3. Installez les dépendances :

   ```bash
   pip install -r requirements.txt
   ```

4. Lancez l'application :

   ```bash
   python main.py
   ```

Pour des instructions d'installation détaillées, consultez [PREREQUIS.md](PREREQUIS.md).

## Fonctionnalités

- **Support Multi-étiquettes** : Prise en charge complète de divers types d'étiquettes NFC, notamment :
  - NTAG (NTAG213, NTAG215, NTAG216)
  - MIFARE Classic (1K, 4K)
  - MIFARE Ultralight
  - FeliCa (Sony)
  - Cartes ISO 14443 Type A/B

- **Support Complet des Étiquettes** : [Voir les opérations prises en charge](docs/supported_operations.md) pour tous les types d'étiquettes

- **Opérations NDEF** :
  - Lecture et écriture d'enregistrements NDEF
  - Création et gestion de plusieurs enregistrements NDEF
  - Prise en charge de divers types d'enregistrements NDEF (Texte, URI, Smart Poster, etc.)
  - Vue hexadécimale pour l'inspection des données brutes

- **Gestion des Étiquettes** :
  - Lecture des informations de l'étiquette (UID, structure de la mémoire, capacités)
  - Écriture de données sur les étiquettes avec validation
  - Verrouillage des étiquettes pour empêcher les écritures non autorisées
  - Formatage des étiquettes pour une utilisation NDEF

- **Interface Utilisateur** :
  - Conception moderne et réactive avec sphinx_rtd_theme
  - Prise en charge des thèmes clair/sombre/système
  - Détection en temps réel des étiquettes et mises à jour d'état
  - Panneau d'informations détaillées sur les étiquettes
  - Visionneuse de journaux avec options de filtrage
  - Documentation complète en anglais et en italien

- **Fonctionnalités de Sécurité** :
  - 🔒 Protection par mot de passe pour les opérations sensibles
  - 🔑 Hachage sécurisé des mots de passe avec PBKDF2
  - 🔄 Fonctionnalité de changement de mot de passe
  - ⚙️ Option pour activer/désactiver la protection par mot de passe
  - 🔐 Opérations protégées incluant les Outils d'Étiquette, la Base de Données et le Clonage

- **Fonctionnalités Avancées** :
  - Mode d'émulation d'étiquette (expérimental)
  - Opérations par lots pour le traitement de plusieurs étiquettes
  - Exécution de commandes personnalisées
  - Système de journalisation avec plusieurs niveaux de verbosité
  - Documentation API pour les développeurs
  - Guide de dépannage pour les problèmes courants
  - Lignes directrices pour la contribution en open source

## 🚀 Configuration Requise

- Python 3.8 ou supérieur
- Lecteur/Écriveur NFC pris en charge :
  - ACR122U
  - PN532 (via USB/UART)
  - Lecteurs compatibles PC/SC
- Windows 10/11 ou Linux avec support PC/SC
- Paquets Python requis (voir `requirements.txt`)

## 📖 Documentation

Une documentation complète est disponible en anglais et en italien, comprenant :

- Guide de l'utilisateur
- Référence API
- Guide de dépannage
- FAQ
- Lignes directrices pour la contribution

Pour générer la documentation localement :

```bash
# Installer les prérequis de documentation
pip install -r requirements-docs.txt

# Générer la documentation anglaise
cd docs/ENG
make html

# Générer la documentation italienne
cd ../FRA
make html
```

La documentation sera disponible dans le répertoire `_build/html` de chaque dossier de langue.

## 📦 Installation

1. Clonez ce dépôt :

   ```bash
   git clone https://github.com/Nsfr750/NFC.git
   cd NFC
   ```

2. Créez et activez un environnement virtuel (recommandé) :

   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate

   # Linux/macOS
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Installez les paquets requis :

   ```bash
   pip install -r requirements.txt
   ```

4. (Facultatif) Installez les pilotes PC/SC s'ils ne sont pas déjà installés :
   - Windows : Installez les [pilotes CCID](https://ccid.apdu.fr/)
   - Linux : Installez les paquets `pcscd` et `libpcsclite-dev`

5. Lancez l'application :

   ```bash
   python main.py
   ```

## 🚀 Utilisation

### Opérations de Base

1. **Connectez votre lecteur NFC**
   - L'application détectera automatiquement les appareils pris en charge
   - L'état de la connexion est affiché dans la barre d'état

2. **Lisez une étiquette**
   - Placez une étiquette NFC près du lecteur
   - Les informations de l'étiquette s'afficheront dans la fenêtre principale
   - Consultez la structure détaillée de la mémoire dans l'éditeur hexadécimal

3. **Écrivez sur une étiquette**
   - Accédez à l'onglet "Écrire"
   - Sélectionnez le type d'enregistrement (Texte, URI, etc.)
   - Entrez votre contenu et cliquez sur "Écrire sur l'étiquette"

4. **Verrouillez une étiquette**
   - Utilisez le bouton "Verrouiller" pour empêcher d'autres écritures
   - Certaines étiquettes prennent en charge le verrouillage permanent (à utiliser avec précaution !)

### 🛠️ Fonctionnalités Avancées

- **Émulation d'étiquette** : Émulez une étiquette NFC (expérimental)
- **Opérations par lots** : Traitez plusieurs étiquettes en une seule fois
- **Scripts personnalisés** : Exécutez des commandes personnalisées sur les étiquettes
- **Journalisation avancée** : Consultez les journaux détaillés pour le débogage

## 🤝 Contribution

Les contributions sont les bienvenues ! Veuillez lire nos [lignes directrices de contribution](CONTRIBUTING.md) pour plus de détails.

## 📄 Licence

Ce projet est sous licence GPL-3.0 - voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 📞 Support

Pour les problèmes et les questions, veuillez ouvrir un [problème](https://github.com/Nsfr750/NFC/issues) sur GitHub.
