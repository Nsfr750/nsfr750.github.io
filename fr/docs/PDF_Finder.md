---
lang: fr
lang-niv: fonto
lang-ref: 019-jbk
layout: doc
order: 9
title: 'PDF Finder'
---

# Chercheur de PDF en double

[![Licence : GPL v3](https://img.shields.io/badge/Licence-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Style de code : black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Un outil puissant pour trouver et gérer les fichiers PDF en double sur votre ordinateur. Le Chercheur de PDF en double vous aide à identifier et supprimer les documents PDF dupliqués, économisant ainsi de l'espace disque et organisant vos fichiers plus efficacement.

## ✨ Fonctionnalités

- 🔍 **Comparaison intelligente des PDF** : Trouvez les PDF en double en fonction du contenu, pas seulement des noms ou des tailles de fichiers
- 📝 **Comparaison basée sur le texte** : Identifiez les doublons même avec des différences visuelles mineures grâce à une analyse de texte avancée
- 👁 **Visionneuse PDF intégrée** : Apercevez les PDF directement dans l'application
- 📋 **Interface à double vue** : Visualisez à la fois la liste des fichiers et les groupes de doublons dans des onglets séparés
- 🎯 **Filtrage avancé** : Filtrez par taille de fichier, date de modification et motifs de noms
- 🚀 **Analyse rapide** : Algorithmes optimisés pour une analyse rapide de grandes collections de PDF
- 🎨 **Interface intuitive** : Interface épurée et conviviale avec support des thèmes clair/sombre
- 🔄 **Traitement par lots** : Traitez plusieurs fichiers ou dossiers entiers en une seule fois
- 📊 **Analyse détaillée** : Affichez les détails des fichiers, les aperçus et les résultats de comparaison
- 🛠 **Outils avancés** : Modes de sélection multiples, filtrage et options de tri
- 🌍 **Multilingue** : Disponible en plusieurs langues
- 📊 **Suivi de la progression** : Barre de progression en temps réel pour les opérations de traitement de fichiers
- ⏱ **Fichiers récents** : Accès rapide aux fichiers récemment ouverts avec options de menu contextuel

## 📦 Installation

### Prérequis

- Python 3.8 ou supérieur
- pip (gestionnaire de paquets Python)
- Moteurs de rendu PDF optionnels (basculement automatique en cas d'échec) :
  - PyMuPDF (fitz) — inclus par défaut via les dépendances
  - Ghostscript (pour Wand) — installez Ghostscript et définissez son chemin d'exécution dans les paramètres

Voir [PREREQUIS.md](PREREQUIS.md) pour la configuration spécifique à chaque plateforme.

### Installation à partir des sources

1. Clonez le dépôt :

   ```bash
   git clone https://github.com/Nsfr750/PDF_finder.git
   cd PDF_finder
   ```

2. Créez et activez un environnement virtuel (recommandé) :

   ```bash
   python -m venv venv
   .\venv\Scripts\activate  # Windows
   source venv/bin/activate  # Linux/Mac
   ```

3. Installez les dépendances requises :

   ```bash
   pip install -r requirements.txt
   ```

## Utilisation

1. Lancez l'application :

   ```bash
   python main.py
   ```

2. Cliquez sur "Parcourir un dossier" pour sélectionner un répertoire à analyser à la recherche de PDF en double.

3. Consultez les résultats dans la fenêtre principale. Après une analyse, la liste des fichiers est automatiquement remplie avec les PDF analysés et les groupes de doublons.

4. Utilisez les outils pour gérer les doublons :
   - Marquez les fichiers à conserver
   - Supprimez les doublons indésirables
   - Apercevez les fichiers avant toute action

## Fonctionnalités clés en détail

### Comparaison intelligente des PDF

- Compare le contenu des PDF à l'aide d'algorithmes de hachage avancés
- Détecte les documents similaires même avec des noms ou des métadonnées différents
- Seuil de similarité configurable pour des résultats précis

### Optimisations des performances

- Analyse multithread pour un traitement plus rapide
- Gestion efficace de la mémoire pour les fichiers PDF volumineux
- Suivi de la progression et possibilité d'annulation

### Expérience utilisateur

- Interface moderne et réactive
- Options d'affichage personnalisables
- Raccourcis clavier complets
- Informations et aperçus détaillés des fichiers
- Barre d'outils avec un espacement amélioré et une meilleure lisibilité
- La boîte de dialogue des paramètres inclut un bouton "Tester les moteurs" pour vérifier la disponibilité de PyMuPDF et Ghostscript

### Moteurs de rendu PDF et basculement

- Choisissez votre moteur préféré dans Paramètres → Rendu PDF
- Utilisez "Tester les moteurs" pour vérifier si Ghostscript est correctement configuré
- Si le moteur sélectionné échoue, l'application bascule automatiquement vers un moteur disponible et affiche un avertissement dans la barre d'état (localisé)

## Historique des versions

Consultez [CHANGELOG.md](CHANGELOG.md) pour une liste complète des modifications de chaque version.

## Contribution

Les contributions sont les bienvenues ! Veuillez lire nos [Directives de contribution](CONTRIBUTING.md) pour plus de détails sur la façon de contribuer à ce projet.

## 📄 Licence

Ce projet est sous licence GNU General Public License v3.0 - voir le fichier [LICENCE](LICENCE) pour plus de détails.

## 🙏 Remerciements

- Merci à tous les contributeurs qui ont aidé à améliorer le Chercheur de PDF en double
- Développé avec ❤️ en utilisant Python et PyQt6

## 🐞 Bugs connus

- La sélection de la langue ne fonctionne pas

---

📅 **Dernière mise à jour** : août 2025  
🐍 **Version de Python** : 3.8+  
📜 **Licence** : GPL-3.0
