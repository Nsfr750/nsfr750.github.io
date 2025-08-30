---
lang: fr
lang-niv: fonto
lang-ref: 018-jbk
layout: doc
order: 8
title: 'OpenPGP'
---

# Documentation de l'Application OpenPGP GUI

Bienvenue dans la documentation officielle de l'**Application OpenPGP GUI**.

## Vue d'ensemble
Cette application fournit une interface moderne et conviviale pour la gestion des clés OpenPGP, le chiffrement, le déchiffrement, la signature de messages, la vérification et la génération de certificats SSL. Toutes les opérations cryptographiques sont effectuées localement pour une confidentialité maximale.

# Fonctionnalités

- Interface utilisateur moderne avec ttkbootstrap (thème Superhero)
- Générer, charger et exporter des paires de clés OpenPGP
- Définir le nom, l'email, la phrase secrète et visualiser l'empreinte de la clé
- Chiffrer et déchiffrer des messages
- Signer et vérifier des messages (signatures détachées)
- Exporter la clé publique au format ASCII armé (.asc)
- Visualiser l'empreinte de la clé pour des vérifications de sécurité
- Générer des certificats SSL avec CN personnalisé
- Effacer/réinitialiser tous les champs en un clic
- **Système de journalisation centralisé** (info, avertissement, erreur, exceptions non gérées)
- **Visionneuse de journaux avec filtrage en temps réel** (TOUT, INFO, AVERTISSEMENT, ERREUR)
- Utilisez `log_info`, `log_warning`, `log_error` pour des entrées de journal personnalisées
- Capture et affichage automatiques des traces d'exécution dans la visionneuse de journaux
- Barre de menus dynamique avec boîtes de dialogue À propos, Aide, Visionneuse de journaux, Sponsor, Version
- Gestion sémantique des versions et informations de version
- Structure modulaire (`struttura`, `gui`, etc.)
- Extensibilité et personnalisation faciles (via ttkbootstrap)

# Pour commencer

## Configuration requise
- Python 3.9 ou supérieur
- PySide6 (inclus dans les dépendances)
- pgpy (inclus dans les dépendances)
- cryptography (inclus dans les dépendances)
- pyperclip (inclus dans les dépendances)

> **Remarque** : L'application a été migrée de Tkinter/ttkbootstrap vers PySide6 pour une interface utilisateur plus moderne et maintenable.

## Installation
1. Clonez ou téléchargez ce dépôt.
2. (Optionnel) Créez un environnement virtuel :
   ```
   python -m venv venv
   venv\Scripts\activate
   ```
3. Installez les dépendances :
   ```
   pip install -r requirements.txt
   ```

## Exécution de l'application
Exécutez depuis la racine du projet :
```
python main.py
```

Si vous rencontrez des erreurs d'importation, assurez-vous d'exécuter depuis la racine et non depuis un sous-dossier.

# Guide de l'utilisateur

## Aperçu de la fenêtre principale
- Entrez votre nom, email et phrase secrète pour la génération de clé.
- Sélectionnez l'algorithme (actuellement RSA ; d'autres à venir).
- Utilisez les boutons pour générer, charger ou exporter des clés.
- L'empreinte de la clé chargée/générée est affichée pour vérification.
- Utilisez la zone de texte pour saisir des messages à chiffrer, déchiffrer, signer ou vérifier.
- Exportez votre clé publique pour la partager en toute sécurité.
- Générez des certificats SSL depuis l'interface graphique.
- Utilisez le bouton 'Effacer' pour réinitialiser tous les champs.

## Barre de menus
- **Fichier** : Exporter la clé publique, Quitter
- **Journal** : Voir le journal (avec filtres pour TOUT, INFO, AVERTISSEMENT, ERREUR)
- **Aide** : Aide, À propos, Sponsor

## Journalisation et visionneuse de journaux
- Toutes les informations, avertissements, erreurs et exceptions non gérées sont automatiquement journalisées.
- Utilisez `log_info(msg)`, `log_warning(msg)`, `log_error(msg)` dans vos scripts pour une journalisation personnalisée.
- La visionneuse de journaux (Journal > Voir le journal) vous permet de filtrer et d'afficher les journaux par niveau.
- Si le fichier journal est manquant, la dernière trace d'exécution est affichée si disponible.

## Conseils
- Toutes les opérations cryptographiques sont locales (pas de cloud).
- Pour de meilleurs résultats, utilisez des phrases secrètes solides.
- La fenêtre de journal fournit des retours et des détails sur les erreurs.

# Utilisation avancée

## Exportation des clés publiques
- Utilisez le bouton 'Exporter la clé publique' ou l'élément de menu pour enregistrer votre clé publique au format ASCII armé (.asc).

## Vérification de l'empreinte
- Vérifiez toujours l'empreinte avant de partager votre clé publique pour une sécurité renforcée.

## Génération de certificats SSL
- Entrez le nom commun (CN) souhaité dans le champ de nom.
- Cliquez sur le bouton 'Générer un certificat SSL' pour créer un certificat auto-signé.

## Extension de l'application
- Vous pouvez ajouter la prise en charge de plus d'algorithmes (ECC, Ed25519) en étendant la logique de génération de clés dans `main_window.py`.
- L'interface utilise ttkbootstrap pour une personnalisation et un thème faciles.

## Journalisation et débogage
- Toutes les actions, avertissements, erreurs et exceptions non gérées sont enregistrées dans `traceback.log`.
- Utilisez `log_info`, `log_warning`, `log_error` pour des entrées de journal personnalisées dans votre code.
- La visionneuse de journaux prend en charge le filtrage par TOUT, INFO, AVERTISSEMENT, ERREUR.
- Les exceptions non gérées sont automatiquement journalisées et affichées dans la visionneuse de journaux (avec trace d'exécution).

## Dépannage
- Si vous rencontrez des erreurs d'importation, assurez-vous d'exécuter depuis la racine du projet.
- Pour les problèmes de dépendances, vérifiez `requirements.txt` ou réinstallez les paquets nécessaires.

# Guide du développeur

Bienvenue, développeur ! Ce guide fournit l'essentiel pour contribuer à et étendre l'application OpenPGP GUI.

---

## Structure du projet
- `main.py` — Point d'entrée, lance la fenêtre principale.
- `gui/` — Tous les composants de l'interface utilisateur (fenêtre principale, widgets, boîtes de dialogue).
- `struttura/` — Logique principale, boîtes de dialogue, utilitaires, gestion des versions, aide/à propos, etc.
- `docs/` — Documentation.
- `requirements.txt` — Dépendances Python.

## Technologies clés
- **Python 3.x**
- **Tkinter** — Cadre d'interface graphique (avec ttkbootstrap pour le thème)
- **pgpy** — Cryptographie OpenPGP
- **cryptography** — Génération de certificats SSL
- **Pillow** — (optionnel) pour les icônes

## Comment contribuer
1. Forkez et clonez le dépôt.
2. Créez un environnement virtuel et installez les dépendances.
3. Suivez les conventions PEP8 et gardez le code modulaire.
4. Documentez les nouvelles fonctionnalités et mettez à jour `CHANGELOG.md`.
5. Ajoutez ou mettez à jour les tests si possible.
6. Ouvrez une demande d'extraction avec une description claire.

## Ajout de fonctionnalités
- Pour ajouter de nouveaux algorithmes (par exemple, ECC), étendez la logique de génération de clés dans `main_window.py`.
- Pour les nouveaux composants d'interface, ajoutez des widgets dans `gui/` et gardez la logique séparée de l'interface utilisateur.
- Utilisez les styles `ttkbootstrap` pour une apparence cohérente.

## Tests
- Ajoutez des tests pour les nouvelles fonctionnalités et corrections de bogues.
- Tests manuels : exécutez `python main.py` et utilisez toutes les fonctions de l'interface.
- (Optionnel) Intégrez avec CI/CD pour des tests automatisés.

## Style de code
- Suivez les conventions PEP8.
- Utilisez des docstrings pour les fonctions/classes publiques.
- Gardez l'interface utilisateur et la logique aussi séparées que possible.

## Journalisation et débogage
- Utilisez `log_info(msg)`, `log_warning(msg)`, `log_error(msg)` n'importe où dans le code pour des entrées de journal personnalisées.
- Tous les journaux sont enregistrés dans `traceback.log` et affichés dans la visionneuse de journaux.
- La visionneuse de journaux prend en charge le filtrage par TOUT, INFO, AVERTISSEMENT, ERREUR.
- Les exceptions non gérées sont automatiquement journalisées et affichées dans la visionneuse de journaux (avec trace d'exécution).

## Support et questions
- Ouvrez des problèmes sur GitHub pour des rapports de bogues ou des demandes de fonctionnalités.
- Voir `README.md` pour les informations de contact et de contribution.

---

## Sujets avancés

### Référence d'API

L'application est modulaire : la logique principale est dans `struttura/`, l'interface dans `gui/`.

**Classes et fonctions principales :**
- `MainWindow` (`gui/main_window.py`) : Logique principale de l'interface et gestion des événements.
- `gen_key`, `export_pubkey`, `clear_fields`, etc. : Méthodes pour les opérations cryptographiques.
- `Help`, `About`, `LogViewer`, etc. : Boîtes de dialogue et utilitaires dans `struttura/`.
- `get_version()` (`struttura/version.py`) : Retourne la chaîne de version actuelle.

Pour plus d'informations, lisez les docstrings dans le code et consultez `docs/user_guide.md` pour le flux d'utilisation.

### Exemples d'extension

#### Ajout d'un nouvel algorithme de clé
1. Dans `gui/main_window.py`, localisez le menu déroulant de sélection d'algorithme.
2. Ajoutez votre nouvel algorithme (par exemple, ECC, Ed25519) aux options du menu déroulant.
3. Dans la logique de génération de clés, implémentez la gestion du nouvel algorithme en utilisant `pgpy`.
4. Testez soigneusement et mettez à jour la documentation.

#### Ajout d'un widget personnalisé
1. Créez votre widget dans `gui/widgets.py` ou un nouveau fichier.
2. Importez et utilisez-le dans la fenêtre principale ou une boîte de dialogue.
