---
lang: fr
lang-niv: font
lang-ref: 012-jbk
layout: doc
order: 2
title: 'CDE550-Sim'
---

# Simulateur Nidec Commander CDE 550

[![Version Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Licence: GPL v3](https://img.shields.io/badge/Licence-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Version](https://img.shields.io/badge/version-0.0.2-green.svg)](CHANGELOG.md)

Simulateur logiciel pour l'onduleur Nidec Commander CDE 550 avec interface graphique, développé en Python avec PyQt6.

## Nouveautés de la version 0.0.2

- **Localisation complète** de l'interface utilisateur en italien
- **Gestion améliorée des alarmes** avec réduction des faux positifs
- **Optimisations des performances** au démarrage et lors des variations de charge
- **Documentation mise à jour** avec un journal des modifications détaillé

## Fonctionnalités

- Simulation réaliste du comportement de l'onduleur Nidec Commander CDE 550
- Interface graphique intuitive avec PyQt6 entièrement localisée en italien
- Communication série via pyserial
- Prise en charge des commandes de contrôle principales
- Simulation de pannes et d'alarmes avec gestion avancée
- Surveillance des paramètres en temps réel
- Journalisation des événements et des erreurs

## Prérequis

- Python 3.8 ou supérieur
- Pip (gestionnaire de paquets Python)
- Environnement virtuel Python (recommandé)

## Installation

1. Clonez le dépôt :
   ```bash
   git clone https://github.com/Nsfr750/CDE550-sim.git
   cd CDE550-sim
   ```

2. Créez et activez un environnement virtuel (optionnel mais recommandé) :
   ```bash
   # Sous Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # Sous macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Installez les dépendances :
   ```bash
   pip install -r requirements.txt
   ```

## Utilisation

1. Démarrez le simulateur :
   ```bash
   python main.py
   ```

2. L'interface graphique affichera :
   - L'état de l'onduleur
   - Les paramètres de fonctionnement
   - Le journal des événements
   - Les commandes de simulation

3. Pour la connexion série :
   - Allez dans Connexion -> Se connecter
   - Sélectionnez le port COM souhaité
   - Définissez la vitesse de communication (débit en bauds)
   - Cliquez sur "Se connecter"

## Commandes Série Prises en Charge

| Commande | Description | Exemple |
|----------|-------------|---------|
| `RUN` | Démarrer l'onduleur | `RUN` |
| `STOP` | Arrêter l'onduleur | `STOP` |
| `RST` | Réinitialiser les alarmes | `RST` |
| `FREQ <valeur>` | Définir la fréquence (Hz) | `FREQ 50.0` |
| `DIR <1\|-1>` | Définir la direction | `DIR 1` (avant) |
| `STATUS` | Afficher l'état complet | `STATUS` |
| `HELP` | Afficher la liste des commandes | `HELP` |

## Structure du Projet

```
CDE550-sim/
├── main.py              # Point d'entrée de l'application
├── inverter_sim.py      # Logique de simulation de l'onduleur
├── serial_handler.py    # Gestion de la communication série
├── script/              # Interface utilisateur et fichiers d'aide
│   ├── help.py          # Fenêtre d'aide
│   ├── serial_dialog.py # Fenêtre de connexion série
│   └── version.py       # Gestion des versions
├── requirements.txt     # Dépendances du projet
├── README.md            # Documentation principale
└── CHANGELOG.md         # Journal des modifications
```

## Contribution

Les contributions sont les bienvenues ! Pour proposer des améliorations :

1. Forkez le projet
2. Créez une branche de fonctionnalité (`git checkout -b feature/FonctionnaliteGeniale`)
3. Validez vos modifications (`git commit -m 'Ajouter une fonctionnalité géniale'`)
4. Poussez vers la branche (`git push origin feature/FonctionnaliteGeniale`)
5. Ouvrez une Pull Request

## Licence

Distribué sous licence GPL-3.0. Voir le fichier `LICENCE` pour plus d'informations.

## Contact

- Auteur : Nsfr750
- Email : [nsfr750@yandex.com]
- Dépôt : https://github.com/Nsfr750/CDE550-sim

---

<div align="center">
  <sub>Développé avec ❤️ par Nsfr750</sub>
</div>
