---
lang: fr
lang-niv: font
lang-ref: 021-jbk
layout: doc
order: 12
title: 'RasPY Utility'
---

# Utilitaire RasPY

<div align="center">
  <img src="../images/logo.png" alt="Logo de l'utilitaire RasPY" width="50%">
</div>

## Bienvenue dans la documentation de RasPY Utility

RasPY Utility est une application complète pour contrôler et surveiller les broches GPIO du Raspberry Pi via une interface graphique intuitive ou une API REST.

## Table des matières

### Introduction
- [Installation](installazione.md)
- [Guide](guida.md)

### Développement
- [Développement](sviluppo.md)
- [API](api.md)
- [Interface graphique](gui.md)
- [Exemples](esempi.md)

### Ressources supplémentaires
- [Journal des modifications](changelog.md)
- [FAQ](faq.md)

### Communauté
- [Contribuer](contribuire.md)
- [Remerciements](ringraziamenti.md)

## Fonctionnalités principales

### ✅ **Interface graphique moderne**
- Thème sombre/clair
- Support multilingue
- Visualisation en temps réel de l'état des broches
- Intégration avec la zone de notification

### 🔌 **Support complet des GPIO**
- Contrôle des broches numériques E/S
- Simulateur intégré pour le développement
- Détection automatique du matériel
- Support des GPIO à distance

### 🌐 **Interface web**
- Serveur web intégré
- Conception réactive pour mobile/bureau
- Mises à jour en temps réel
- Documentation API intégrée

## Démarrage rapide

1. [Installation](installazione.md) - Comment installer et configurer RasPY Utility
2. [Guide](guida.md) - Guide d'utilisation de l'application
3. [API](api.md) - Documentation de l'API pour les développeurs
4. [Développement](sviluppo.md) - Guide de développement et de contribution

## Guide d'utilisation

### Interface graphique

L'interface graphique de RasPY 4 Utility est conçue pour être intuitive et facile à utiliser.

#### Menu principal

- **Fichier** : Commandes générales de l'application
- **GPIO** : Gestion des broches GPIO et du simulateur
- **Affichage** : Personnalisation de l'interface
- **Aide** : Documentation et informations

#### Contrôle des GPIO

1. Ouvrez la fenêtre de contrôle GPIO depuis le menu
2. Sélectionnez la broche à contrôler
3. Utilisez les boutons pour basculer les broches
4. Surveillez l'état en temps réel

#### Simulateur GPIO
Le simulateur vous permet de tester le code sans matériel physique :

1. Démarrez le simulateur depuis le menu GPIO
2. Utilisez l'interface pour simuler les entrées/sorties
3. Les modifications se reflètent en temps réel

### Journalisation et débogage
L'application enregistre les événements importants dans le fichier `logs/app.log`. Utilisez la visionneuse de journaux intégrée pour :

- Filtrer les messages par niveau (INFO, AVERTISSEMENT, ERREUR)
- Rechercher des messages spécifiques
- Exporter les journaux pour analyse

### Raccourcis clavier

- **Ctrl+Q** : Quitter l'application
- **F1** : Afficher l'aide
- **Ctrl+L** : Ouvrir la visionneuse de journaux
- **F5** : Actualiser l'interface

## Référence de l'API

### Aperçu

L'API REST de RasPY 4 Utility permet de contrôler les broches GPIO via des requêtes HTTP.
Toutes les réponses sont au format JSON.

### Points de terminaison disponibles

#### `GET /api/gpio`

Retourne l'état de toutes les broches GPIO configurées.

**Exemple de réponse :**

```json
{
  "17": {"state": 0, "mode": "out", "description": "LED rouge"},
  "18": {"state": 1, "mode": "in", "description": "Bouton"}
}
```

#### `GET /api/gpio/<int:pin>`

Retourne l'état d'une broche spécifique.

**Paramètres :**
- `pin` : Numéro de la broche GPIO

**Codes de statut :**
- 200 : Opération réussie
- 404 : Broche introuvable

**Exemple de réponse :**

```json
{
  "state": 0,
  "mode": "out",
  "description": "LED rouge"
}
```

#### `POST /api/gpio/<int:pin>/on`

Active la broche spécifiée.

**Paramètres :**
- `pin` : Numéro de la broche GPIO

**Codes de statut :**
- 200 : Opération réussie
- 400 : Broche invalide ou non accessible en écriture

#### `POST /api/gpio/<int:pin>/off`

Désactive la broche spécifiée.

**Paramètres :**
- `pin` : Numéro de la broche GPIO

**Codes de statut :**
- 200 : Opération réussie
- 400 : Broche invalide ou non accessible en écriture

## Exemples d'utilisation

### Contrôle GPIO avec Python

```python
import requests

BASE_URL = "http://localhost:5000/api/gpio"

# Obtenir l'état de toutes les broches
response = requests.get(f"{BASE_URL}")
print("État actuel :", response.json())

# Activer la broche 17
response = requests.post(f"{BASE_URL}/17/on")
print("Réponse de l'activation :", response.status_code)
```

## Ressources utiles

- [Site officiel de Raspberry Pi](https://www.raspberrypi.org/)
- [Documentation Python](https://www.python.org/)
- [Documentation des broches GPIO](https://pinout.xyz/)
