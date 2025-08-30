---
lang: fr
lang-niv: fonto
lang-ref: 020-jbk
layout: doc
order: 11
title: 'PySnoop'
---

# PySnoop

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Une application Python moderne pour lire, écrire et analyser les données de cartes à bande magnétique. Ce projet est une continuation du projet StripeSnoop original, reconstruit avec Python moderne et une interface conviviale.

## ✨ Fonctionnalités

- **Lecture de cartes** : Lire les cartes à bande magnétique à l'aide de lecteurs compatibles
- **Gestion de base de données** : Stocker et gérer les données de cartes en toute sécurité
- **Multi-formats** : Exporter/Importer les données de cartes dans divers formats
- **Interface graphique moderne** : Interface utilisateur conviviale avec support des thèmes
- **Multi-plateforme** : Fonctionne sous Windows, macOS et Linux
- **Exécutable autonome** : Construction en un seul fichier exécutable pour une distribution facile
- **Versions de débogage** : Configuration spéciale de débogage pour le dépannage
- **Sécurité** : Stockage sécurisé pour les données de cartes sensibles
- **Validation** : Validation intégrée des numéros de carte (C10/Luhn)
- **Documentation** : Documentation complète et exemples

## 🚀 Installation

### Prérequis

- Python 3.7 ou supérieur
- pip (gestionnaire de paquets Python)
- Git (optionnel, pour le développement)

### Démarrage rapide

1. Clonez le dépôt :

   ```bash
   git clone https://github.com/Nsfr750/PySnoop.git
   cd PySnoop
   ```

2. Créez et activez un environnement virtuel :

   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Installez les dépendances :

   ```bash
   pip install -r requirements.txt
   ```

## 🏗️ Construction de l'application

PySnoop peut être compilé en un exécutable autonome en utilisant Nuitka. Nous fournissons deux scripts de construction :

### Version de débogage

```bash
.\snoop_debug.bat
```

Ceci crée une version de débogage de l'application avec la fenêtre de console activée pour le dépannage.

### Version de production

```bash
.\snoop.bat
```

Ceci crée une version optimisée de l'application.

### Sorties de construction

- Version de débogage : `build\PySnoop_debug.exe`
- Version de production : `build\PySnoop.exe`

## 🛠️ Développement
   ```bash
   pip install -r requirements.txt
   ```

## 💻 Utilisation

### Mode graphique (recommandé)

```bash
python pysnoop_gui.py
```

### Interface en ligne de commande

```bash
python pysnoop.py [options]
```

### Options disponibles

```bash
-h, --help      Afficher le message d'aide et quitter
-v, --verbose   Activer la sortie détaillée
--version       Afficher les informations de version
```

## 🔌 Périphériques pris en charge

- Lecteur/Écrivain de cartes à bande magnétique MSR605
- Autres lecteurs de cartes compatibles HID (expérimental)

## 📚 Documentation

Pour une documentation détaillée, y compris la référence de l'API et des exemples d'utilisation, veuillez visiter la [documentation](https://nsfr750.github.io/PySnoop/ "Documentation PySnoop").

## 🤝 Contribution

Les contributions sont les bienvenues ! Veuillez lire nos [lignes directrices de contribution](CONTRIBUTING.md) pour commencer.

## 📄 Licence

Ce projet est sous licence GPLv3 - voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 🙏 Soutien

Si vous trouvez ce projet utile, envisagez de soutenir son développement :

[![Faire un don via PayPal](https://img.shields.io/badge/Don-PayPal-blue.svg)](https://paypal.me/3dmega)
[![Devenir un Mécène](https://img.shields.io/badge/Soutien-Patreon-orange.svg)](https://www.patreon.com/Nsfr750)

## 📧 Contact

Pour des questions ou du support, veuillez ouvrir un problème ou contacter [Nsfr750](mailto:nsfr750@yandex.com).

## Crédits

- Basé sur le projet StripeSnoop original (http://stripesnoop.sourceforge.net)

## Contribution

Les contributions sont les bienvenues ! N'hésitez pas à soumettre une demande d'extraction (Pull Request).
