---
lang: fr
lang-niv: fonto
lang-ref: 017-jbk
layout: page
title: 'Nidec CommanderCDE'
---

# Nidec CommanderCDE

Une application graphique Python complète pour le contrôle et la surveillance des variateurs Nidec Commander CDE via Modbus RTU.

## ✨ Fonctionnalités

- **Support multilingue** : Interface complète en anglais et en italien avec changement de langue dynamique
- **Support multi-modèles** : Compatible avec les modèles de variateurs CDE400, CDE550, CDE750 et CDE1100S
- **Contrôle du variateur** :
  - Connexion aux variateurs Nidec Commander CDE via RS-485/Modbus RTU
  - Contrôle de la vitesse et du sens du moteur
  - Démarrage/Arrêt du variateur
  - Surveillance en temps réel de l'état et des diagnostics du variateur
  - Détection des défauts et fonction de réinitialisation
  - Sauvegarde et restauration des paramètres
- **Interface utilisateur** :
  - Interface moderne à onglets avec des commandes intuitives
  - Tableau de bord complet avec des mesures en temps réel
  - Barre d'état avec l'état de la connexion et du variateur
  - Conception réactive avec support des thèmes clair/sombre
  - Éléments d'interface personnalisables
- **Gestion des données** :
  - Surveillance et journalisation en temps réel des paramètres du variateur
  - Exportation des données vers CSV/Excel
  - Visualisation graphique des tendances des paramètres
  - Intervalles de journalisation configurables
- **Diagnostics** :
  - Surveillance complète des paramètres
  - Historique et journalisation des défauts
  - Indicateurs d'état du système
  - Métriques de performance en temps réel

## 🆕 Nouveautés de la v0.0.4

### Nouvelles fonctionnalités
- Ajout de la prise en charge de plusieurs modèles de variateurs Nidec (CDE400, CDE550, CDE750, CDE1100S)
- Traductions complètes en italien pour tous les éléments de l'interface
- Système d'aide amélioré avec une documentation détaillée
- Thème bleu pour une meilleure lisibilité dans les sections d'aide

### Améliorations
- Interface utilisateur mise à jour pour une meilleure expérience
- Messages d'erreur et journalisation améliorés
- Performances optimisées pour la surveillance en temps réel
- Problèmes de compatibilité avec PyQt6 résolus
- Correction du changement de langue dans les boîtes de dialogue d'aide

## 🚀 Configuration requise

- Python 3.8 ou supérieur
- PyQt6 >= 6.6.1
- pyserial >= 3.5
- pymodbus >= 3.5.4
- PyQt6-QScintilla >= 2.14.1
- python-dotenv >= 1.0.0

## 🛠 Installation et configuration

1. Clonez le dépôt :

   ```bash
   git clone https://github.com/Nsfr750/nidec-commandercde.git
   cd nidec-commandercde
   ```

2. Créez et activez un environnement virtuel (recommandé) :

   ```bash
   python -m venv venv
   # Sous Windows :
   .\venv\Scripts\activate
   # Sous Unix ou MacOS :
   # source venv/bin/activate
   ```

3. Installez les paquets requis :

   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Utilisation de base

1. Connectez votre variateur Nidec Commander CDE à votre ordinateur via un adaptateur RS-485
2. Lancez l'application :

   ```bash
   python main.py
   ```

3. Sélectionnez le port COM approprié et la vitesse de transmission
4. Cliquez sur 'Connecter' pour établir la communication avec le variateur
5. Utilisez l'interface pour contrôler et surveiller le variateur

## Paramètres de connexion

- Vitesse de transmission : 9600
- Bits de données : 8
- Parité : Paire
- Bits d'arrêt : 1
- Adresse Modbus : 1 (par défaut, peut être modifiée dans les paramètres du variateur)

## Notes importantes

- Ce logiciel est fourni tel quel, sans aucune garantie
- Assurez-vous toujours de disposer de connexions électriques appropriées et de respecter les mesures de sécurité lors de l'utilisation des variateurs de moteur
- Les adresses de registre par défaut sont basées sur des configurations typiques des variateurs Nidec mais peuvent nécessiter des ajustements pour votre modèle spécifique
- Reportez-vous au manuel Nidec CDE 400 Commander pour des informations détaillées sur les paramètres et les adresses de registre
