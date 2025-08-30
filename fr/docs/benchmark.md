---
lang: fr
lang-niv: fonto
lang-ref: 023-jbk
layout: doc
order: 14 # Optionnel : pour le tri dans le menu
title: 'benchmark'
---

[![Licence : GPL v3](https://img.shields.io/badge/Licence-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Style de code : black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Un outil de benchmarking Python moderne construit avec PySide6, offrant une interface conviviale pour exécuter et analyser des tests Pystone et d'autres benchmarks.

## 📥 Installation

### Prérequis

- Python 3.9 ou supérieur
- Windows ou Linux

### Démarrage rapide

1. Clonez le dépôt :

   ```bash
   git clone https://github.com/Nsfr750/benchmark.git
   cd benchmark
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

## ✨ Fonctionnalités

- **Interface utilisateur moderne** : Interface propre et réactive construite avec PySide6
- **Benchmark complet** :
  - Durée des tests personnalisable
  - Suivi en temps réel de la progression
  - Résultats détaillés avec statistiques
  - Comparaison avec les données historiques
- **Journalisation** :
  - Journaux d'opérations détaillés
  - Filtrage des journaux par niveau
  - Rotation des fichiers journaux
- **Support multilingue** :
  - Anglais (en)
  - Italien (it)
- **Accessibilité** :
  - Raccourcis clavier
  - Mode contraste élevé
  - Taille du texte réglable

## ⌨️ Raccourcis clavier

- `Ctrl+L` : Afficher les journaux de l'application
- `F1` : Afficher l'aide
- `Échap` : Fermer les boîtes de dialogue
- `Ctrl+Q` : Quitter l'application

## 📊 Utilisation

1. Définissez le nombre d'itérations pour le benchmark
2. Cliquez sur "Démarrer le benchmark" pour commencer
3. Surveillez la progression en temps réel
4. Consultez les résultats détaillés et les statistiques
5. Accédez aux journaux pour le dépannage

## 📂 Structure du projet

```
benchmark/
├── .github/                            # GitHub Actions
│   ├── workflows/                      # Workflows GitHub Actions
│   │   └── ci-cd.yml                   # Pipeline CI/CD
│   ├── issues/                         # Problèmes GitHub
│   |   └── templates/                  # Modèles de problèmes GitHub
│   └── FUNDING.yml                     # Fichier de financement
├── assets/                             # Fichiers d'actifs
├── config/                             # Fichiers de configuration
│   ├── config.json                     # Fichier de configuration
│   └── updates.json                    # Cache des mises à jour
├── docs/                               # Documentation
│   ├── images/                         # Images de la documentation
│   ├── pdf/                            # Documentation PDF
│   └── USER_GUIDE.md                   # Guide utilisateur
├── lang/                               # Fichiers de langue
│   ├── en.json                         # Fichier en anglais
│   └── it.json                         # Fichier en italien
├── logs/                               # Fichiers journaux
├── script/                             # Code source
│   ├── __init__.py                     # Initialisation du package
│   ├── about.py                        # Boîte de dialogue "À propos"
│   ├── benchmark_history.py            # Historique des benchmarks
│   ├── benchmark_tests.py              # Tests de benchmark
│   ├── CLI_pystone.py                  # Benchmark Pystone en ligne de commande
│   ├── config_manager.py               # Gestionnaire de configuration
│   ├── export_results.py               # Exportation des résultats
│   ├── hardware_monitor.py             # Moniteur matériel
│   ├── help.py                         # Boîte de dialogue d'aide
│   ├── history_dialog.py               # Boîte de dialogue d'historique
│   ├── lang_mgr.py                     # Gestionnaire de langue
│   ├── logger.py                       # Configuration de la journalisation
│   ├── menu.py                         # Fonctionnalités de la barre de menu
│   ├── settings.py                     # Boîte de dialogue des paramètres
│   ├── sponsor.py                      # Boîte de dialogue des sponsors
│   ├── system_info.py                  # Informations système
│   ├── test_menu.py                    # Menu des tests
│   ├── theme_manager.py                # Gestionnaire de thème
│   ├── updates.py                      # Système de mise à jour
│   ├── version.py                      # Système de version
│   ├── view_log.py                     # Visionneuse de journaux
│   └── visualization.py                # Visualisation des benchmarks
├── tests/                              # Fichiers de test
│   ├── test_benchmark.py               # Test de benchmark
│   ├── test_hardware_monitor.py        # Test du moniteur matériel
│   ├── test_monitor_manual.py          # Test manuel du moniteur
│   ├── test_monitor.py                 # Test du moniteur
│   └── TEST_README.md                  # README des tests
├── .gitignore                          # Fichier .gitignore
├── CHANGELOG.md                        # Journal des modifications
├── CONTRIBUTING.md                     # Lignes directrices pour les contributions
├── LICENSE                             # Fichier de licence GPLv3
├── main.py                             # Application principale
├── README.md                           # Ce fichier
├── requirements.txt                    # Fichier des dépendances
└── TO_DO.md                            # Liste des tâches
```
