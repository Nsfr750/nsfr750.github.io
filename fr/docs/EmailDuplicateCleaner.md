---
lang: fr
lang-niv: fonto
lang-ref: 013-jbk
layout: doc
order: 3
title: 'Nettoyeur de Doublons d\'Emails'
---

# 📧 Nettoyeur de Doublons d'Emails

Un outil Python complet conçu pour analyser, identifier et supprimer les emails en double sur plusieurs clients de messagerie. Avec des interfaces web, bureau et ligne de commande.

## 🚀 Version

**Version actuelle :**
[![Version GitHub](https://img.shields.io/badge/version-v2.5.2-green)](https://github.com/Nsfr750/EmailDuplicateCleaner)
[![Documentation](https://img.shields.io/badge/docs-disponible-brightgreen)](https://github.com/Nsfr750/EmailDuplicateCleaner/blob/master/README.md)
[![Versions Python](https://img.shields.io/badge/python-3.8%20|%203.9%20|%203.10%20|%203.11%20|%203.12-blue)](https://www.python.org/)
[![Licence : GPL v3](https://img.shields.io/badge/Licence-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![PyPI](https://img.shields.io/pypi/v/email-duplicate-cleaner)](https://pypi.org/project/email-duplicate-cleaner/)
[![Faire un don](https://img.shields.io/badge/Don-PayPal-green.svg)](https://paypal.me/3dmega)
[![Soutien](https://img.shields.io/badge/Soutien-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750)

## ✨ Nouveautés de la version 2.5.2

- 🚀 Mise à jour vers la version 2.5.2
- 🐛 Correction de l'affichage du numéro de version dans la fenêtre À propos
- 📚 Mise à jour de la documentation pour refléter les derniers changements

## ✨ Nouveautés de la version 2.5.1

- 🐛 Correction d'une erreur d'importation QAction dans l'interface graphique PySide6
- 🌐 Ajout des traductions complètes en anglais
- 📄 Inclusion du fichier de licence GPL-3.0
- 🔄 Amélioration de la gestion des erreurs lors de l'initialisation de l'interface graphique
- ⬆️ Mise à jour des dépendances pour une meilleure stabilité

## ✨ Fonctionnalités

### 🔍 Détection des doublons

- Plusieurs critères de détection :
  - Strict : Comparaison complète
  - Contenu uniquement : Analyse du corps du message
  - En-têtes : Correspondance basée sur les métadonnées
  - Objet+Expéditeur : Identification ciblée

### 📊 Analyse des emails

- Analyses avancées des emails :
  - Analyse des expéditeurs : Identifier les principaux expéditeurs et domaines
  - Analyse chronologique : Visualiser les modèles d'emails dans le temps
  - Analyse des pièces jointes : Types de fichiers, tailles et fréquences
  - Analyse des fils de discussion : Voir et gérer les conversations
  - Analyse des doublons : Informations détaillées sur la détection des doublons
  - Rapports exportables dans plusieurs formats (Texte, HTML, JSON)

### 🖥️ Prise en charge multi-interfaces

- **Interface Web** - Design moderne et réactif avec mode clair/sombre
- **Interface Bureau** - Expérience de bureau native avec PySide6
- **Interface Ligne de Commande** - Prise en charge puissante de l'automatisation et des scripts

### 🌓 Expérience utilisateur améliorée

- Interface web moderne avec mode clair/sombre
- Aperçu interactif avec mises à jour en temps réel
- Système d'aide complet
- Mode débogage avec journalisation détaillée
- Mode démo pour les tests et l'apprentissage

### 🔒 Compatibilité avec les clients de messagerie

Prend en charge :

- Mozilla Thunderbird
- Apple Mail
- Microsoft Outlook
- Formats mbox/maildir génériques

### 🏗️ Points forts techniques

- Interface web moderne construite avec Flask
- Gestion de base de données avec SQLAlchemy
- Système d'aide complet avec contenu dynamique
- Architecture modulaire avec séparation claire des préoccupations
- Compatibilité multiplateforme
- Gestion étendue des erreurs et journalisation

## 🛠️ Prérequis

- Python 3.8+
- pip
- Systèmes d'exploitation pris en charge : Windows, macOS, Linux

## 🚀 Démarrage rapide

### 💰 Soutenir ce projet

Si vous trouvez cet outil utile, envisagez de soutenir son développement :

- [![Faire un don](https://img.shields.io/badge/Don-PayPal-green.svg)](https://paypal.me/3dmega) Soutien via PayPal
- [![Soutien](https://img.shields.io/badge/Soutien-Patreon-ff69b4.svg)](https://www.patreon.com/Nsfr750) Devenir un Mécène
- :money_with_wings: **Monero (XMR)**: 
  ```
  47Jc6MC47WJVFhiQFYwHyBNQP5BEsjUPG6tc8R37FwcTY8K5Y3LvFzveSXoGiaDQSxDrnCUBJ5WBj6Fgmsfix8VPD4w3gXF
  ```

## 📦 Installation

1.  Clonez le dépôt :

    ```bash
    git clone https://github.com/Nsfr750/EmailDuplicateCleaner.git
    cd EmailDuplicateCleaner
    ```

2.  Installez les dépendances :

    ```bash
    pip install -r requirements.txt
    ```

### Exécution de l'application

#### Interface Web

```bash
python app.py
```

Accédez à `http://localhost:5000`

#### Interface Bureau

```bash
python email_cleaner_gui.py
```

#### Démo en Ligne de Commande

```bash
python email_duplicate_cleaner.py --demo
```

## 🤝 Contribution

Intéressé(e) à contribuer ? Consultez notre [Guide de Contribution](CONTRIBUTING.md) !

## 📄 Licence

Ce projet est sous licence MIT.

## 🐛 Problèmes

Vous avez trouvé un bug ? [Ouvrez un ticket](https://github.com/Nsfr750/EmailDuplicateCleaner/issues)

## 📊 Méthodes de détection

- `strict` : ID du message + Date + De + Objet + Contenu
- `content` : Contenu uniquement
- `headers` : ID du message + Date + De + Objet
- `subject-sender` : Champs Objet + De uniquement

## Fonctionnalités de sécurité

- Conserve toujours au moins une copie de chaque email
- Conserve l'email le plus ancien par défaut
- Les emails originaux sont récupérables depuis la corbeille
- Mode démo pour des tests en toute sécurité

## Structure du projet

- `email_cleaner_web.py` : Interface web
- `email_cleaner_gui.py` : Interface graphique de bureau
- `email_duplicate_cleaner.py` : Fonctionnalités principales et CLI
- `static/` : Ressources web (CSS, JS)
- `templates/` : Modèles HTML

## Flux de travail

- Mode Démo : Fonctionne avec des emails de test
- Aide : Affiche les informations d'utilisation
- Mode GUI : Lance l'interface graphique
- Mode Web : Démarre le serveur web

## Structure de l'interface graphique

- **Interface Graphique (`email_cleaner_gui.py`)** : Une interface utilisateur conviviale construite avec Tkinter. Elle offre un moyen intuitif de sélectionner les clients de messagerie, d'analyser les dossiers et de gérer les doublons.
- **Ligne de Commande (`email_cleaner_cli.py`)** : Une interface en ligne de commande pour les utilisateurs qui préfèrent travailler dans le terminal.
- **Web (`app.py`)** : Une interface web basée sur Flask, accessible depuis n'importe quel navigateur.

### Modules Auxiliaires (`struttura/`)

Le répertoire `struttura/` contient tous les modules auxiliaires qui prennent en charge l'interface graphique, tels que les fenêtres de dialogue et le menu.

- **`menu.py`** : Gère la création et la fonctionnalité de la barre de menu principale, maintenant le fichier d'interface graphique principal propre et concentré sur sa mise en page principale.
- **`about.py`**, **`help.py`**, **`sponsor.py`** : Définissent respectivement les fenêtres de dialogue `À propos`, `Aide` et `Soutien`, chacune encapsulée dans sa propre classe.
- **`log_viewer.py`** : Un simple visualisateur de journaux pour afficher les journaux de l'application.
