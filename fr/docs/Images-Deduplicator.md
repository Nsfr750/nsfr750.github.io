---
lang: fr
lang-niv: fonto
lang-ref: 014-jbk
layout: doc
order: 4
title: 'Dédoublonneur d\'Images'
---

# Dédoublonneur d'Images

Le Dédoublonneur d'Images est une application Python puissante conçue pour la gestion et la suppression efficace des images en double. Utilisant la bibliothèque Wand (ImageMagick) pour le traitement d'images, cet outil offre des techniques avancées de comparaison visuelle pour identifier et gérer les images en double avec une grande précision.

## Fonctionnalités Principales

- **Traitement d'Images Avancé** : Utilise Wand/ImageMagick pour une prise en charge optimale des formats d'image
- **Détection de Doublons Visuels** : Hachage perceptuel pour identifier les images visuellement similaires
- **Prise en Charge Complète des Formats** : Gère tous les principaux formats d'image, notamment JPEG, PNG, WEBP, PSD, et plus encore
- **Interface Intuitive** : Interface graphique conviviale avec support des thèmes clair/sombre
- **Support Multilingue** : Internationalisation intégrée avec l'anglais et l'italien
- **Traitement par Lots** : Traite efficacement des milliers d'images
- **Aperçu et Comparaison** : Comparaison côte à côte avant toute action
- **Opérations Sûres** : Déplacement vers la corbeille au lieu d'une suppression définitive
- **Journalisation Détaillée** : Suivi complet des opérations pour une traçabilité optimale

## Configuration Système Requise

- **Python** : 3.8 ou supérieur (3.10+ recommandé)
- **ImageMagick** : Requis pour le traitement d'images Wand
  - Windows : Installez depuis [ImageMagick Windows](https://imagemagick.org/script/download.php#windows)
  - macOS : `brew install imagemagick`
  - Linux : `sudo apt-get install libmagickwand-dev`
- **Mémoire** : 4 Go minimum, 8 Go+ recommandé pour les grandes collections d'images
- **Stockage** : Espace suffisant pour les images à traiter + fichiers temporaires
- **Systèmes d'Exploitation** :
  - Windows 10/11
  - macOS 10.15+
  - Linux avec X11/Wayland

## Pourquoi Wand/ImageMagick ?

Le Dédoublonneur d'Images utilise Wand (une liaison Python pour ImageMagick) pour plusieurs avantages :

- Meilleure prise en charge des formats, y compris PSD, GIF et BMP
- Gestion de la mémoire optimisée pour les grandes images
- Comportement plus cohérent sur différentes plateformes
- Capacités avancées de manipulation d'images
- Maintenance active et mises à jour de sécurité

## Utilisation

### Interface Principale

L'application propose une interface moderne et conviviale avec les composants clés suivants :

1. **Barre de Menu** : Accès à toutes les fonctions et paramètres de l'application
2. **Barre d'Outils** : Accès rapide aux fonctions fréquemment utilisées
3. **Navigateur de Dossiers** : Parcourez et sélectionnez les répertoires à analyser
4. **Volet d'Aperçu** : Visualisez et comparez les images côte à côte
5. **Panneau des Résultats** : Affiche les doublons trouvés avec des scores de similarité
6. **Barre d'État** : Affiche la progression des opérations et les informations système

### Flux de Travail de Base

1. **Sélectionnez le Dossier Source**
   - Cliquez sur le bouton "Ouvrir un Dossier" ou utilisez `Fichier > Ouvrir un Dossier`
   - L'application recherchera les formats d'image pris en charge
   - Formats pris en charge : JPEG, PNG, WEBP, PSD, BMP, GIF, et plus (via Wand/ImageMagick)

2. **Configurez les Paramètres d'Analyse**
   - Ajustez le seuil de similarité (par défaut : 90%)
   - Définissez la taille minimale des images à prendre en compte
   - Choisissez les propriétés des images à comparer (taille, date, empreinte numérique du contenu)

3. **Lancez l'Analyse**
   - Cliquez sur "Démarrer l'Analyse" pour commencer la détection des doublons
   - La progression s'affiche dans la barre d'état
   - Mettez en pause ou arrêtez l'analyse à tout moment

4. **Passez en Revue les Résultats**
   - Les groupes de doublons s'affichent avec des aperçus
   - Triez par taille de fichier, date ou score de similarité
   - Utilisez l'outil de comparaison côte à côte pour vérification

5. **Gérez les Doublons**
   - Sélectionnez les images à conserver ou à supprimer
   - Déplacez les doublons vers la corbeille (récupérables) ou supprimez-les définitivement
   - Exportez les résultats vers CSV/JSON pour référence

### Fonctionnalités Avancées

#### Traitement par Lots

- Traitez plusieurs dossiers en séquence
- Enregistrez et chargez les configurations d'analyse
- Planifiez des analyses automatiques

#### Sélection Intelligente

- Sélection automatique des images par critères (les plus anciennes, les plus petites, etc.)
- Conservation de la version la plus haute résolution
- Préservation des images avec des modèles de nommage spécifiques

#### Outils de Comparaison d'Images

- Modes de comparaison côte à côte et par superposition
- Zoom et défilement synchronisés entre les images
- Comparaison d'histogrammes et de données EXIF

#### Filtres Personnalisés

- Filtrage par dimensions d'image
- Filtrage par date de création/modification
- Filtrage par format d'image ou profil couleur

#### Intégration Wand/ImageMagick

- Prise en charge avancée des formats d'image
- Meilleure gestion des profils couleur et des métadonnées
- Prise en charge des formats RAW des appareils photo lorsqu'activée dans ImageMagick

### Raccourcis Clavier

| Raccourci    | Action                           |
|-------------|----------------------------------|
| `Ctrl+O`   | Ouvrir un dossier                |
| `Ctrl+F`   | Démarrer une nouvelle analyse    |
| `Espace`   | Basculer la sélection de l'image courante |
| `Suppr`    | Déplacer la sélection vers la corbeille |
| `Ctrl+Z`   | Annuler la dernière action       |
| `F5`       | Actualiser la vue                |

## Optimisation des Performances

### Pour les Grandes Collections

- Utilisez le mode "Comparaison Rapide" pour un filtrage initial
- Augmentez la taille minimale des fichiers pour ignorer les miniatures
- Planifiez les analyses en dehors des heures de pointe pour les grandes collections

### Gestion de la Mémoire

- Fermez les applications gourmandes en mémoire
- Ajustez les limites de ressources d'ImageMagick si nécessaire (voir Installation)
- Traitez les images par lots plus petits

### Considérations de Stockage

- Assurez-vous d'avoir suffisamment d'espace libre pour les fichiers temporaires
- Traitez les images directement depuis le lecteur source lorsque c'est possible
- Envisagez d'utiliser un SSD rapide pour de meilleures performances

## Dépannage

### Performances Lentes

- Vérifiez les paramètres de stratégie d'ImageMagick (voir Installation)
- Réduisez le nombre d'opérations simultanées
- Désactivez l'aperçu en temps réel pour les grandes collections

### Images Manquantes

- Vérifiez qu'ImageMagick prend en charge le format d'image
- Vérifiez les permissions des fichiers
- Consultez les messages d'erreur dans la visionneuse de journaux

### Résultats Inattendus

- Ajustez le seuil de similarité
- Vérifiez si les filtres sont trop restrictifs
- Vérifiez que les métadonnées des images sont correctement lues

## Configuration

### Options Principales

#### Précision de la Comparaison

- **Niveau de précision (1-100)** :
  - Les valeurs plus basses trouvent plus de doublons
  - Les valeurs plus élevées ne trouvent que les doublons presque identiques

#### Tailles Minimales

- **Ignorer les images en dessous de** :
  - Largeur minimale (pixels)
  - Hauteur minimale (pixels)
  - Taille minimale (Ko)

#### Formats Pris en Charge

- **Extensions autorisées** :
  - .jpg, .jpeg
  - .png
  - .gif
  - .bmp
  - .webp

#### Dossiers Exclus

- **Liste des dossiers à ignorer** :
  - Dossiers système
