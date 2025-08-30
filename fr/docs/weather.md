---
lang: fr
lang-niv: fonto
lang-ref: 022-jbk
layout: doc
order: 13
title: 'Météo'
---

# Documentation de l'application Météo (v1.6.0)

Bienvenue dans la documentation de l'application Météo ! Cette application fournit des informations météorologiques en temps réel et des prévisions de plusieurs fournisseurs de données météorologiques.

## Fonctionnalités

- 🌦️ Conditions météorologiques actuelles avec des métriques détaillées
- 📅 Prévisions météorologiques sur 7 jours avec détails horaires
- 📖 Visionneuse de documentation Markdown intégrée
- 📊 Visionneuse de journaux d'application pour le diagnostic
- 🌍 Plusieurs fournisseurs de données météorologiques
- 🌐 Support multilingue
- ⭐ Emplacements favoris avec historique amélioré
- ⚙️ Paramètres et thèmes personnalisables

## Mises à jour récentes

Pour une liste détaillée des modifications, consultez le fichier [CHANGELOG.md](CHANGELOG.md).

## Pour commencer

1. [Guide d'installation](installation.md) - Comment installer et configurer l'application
2. [Guide d'utilisation](usage.md) - Comment utiliser l'application
3. [Configuration](configuration.md) - Comment configurer l'application

## Sujets avancés

- [Fournisseurs météo](providers.md) - Informations sur les fournisseurs de données météorologiques pris en charge
- [Traductions](translations.md) - Comment ajouter ou modifier des traductions
- [Guide de développement](development.md) - Comment contribuer au projet
- [Dépannage](troubleshooting.md) - Problèmes courants et solutions

## Support

Pour obtenir de l'aide, veuillez ouvrir un problème sur notre [dépôt GitHub](https://github.com/Nsfr750/weather).

## Licence

Ce projet est sous licence GPLv3 - voir le fichier [LICENCE](https://github.com/Nsfr750/weather/blob/main/LICENSE) pour plus de détails.

# Guide d'utilisation

## Pour commencer

1. **Lancer l'application**
   - Double-cliquez sur l'icône de l'application ou exécutez-la depuis la ligne de commande
   - La fenêtre principale s'ouvrira avec la météo de l'emplacement par défaut
   - Lors du premier démarrage, vous serez guidé à travers la configuration initiale

2. **Rechercher un emplacement**
   - Tapez un nom de ville dans la barre de recherche
   - Appuyez sur Entrée ou cliquez sur le bouton de recherche (🔍)
   - Pour des résultats plus précis, incluez le code pays (par exemple, "Paris, FR")
   - Faites un clic droit sur la carte pour sélectionner un emplacement

## Interface principale

### Affichage météorologique

- **Météo actuelle** : Affiche la température, les conditions et des détails supplémentaires
  - Cliquez sur n'importe quelle métrique pour basculer entre les unités (par exemple, °C/°F, km/h/mph)
  - Survolez les icônes pour plus d'informations

- **Prévisions sur 7 jours** : Affiche les prévisions météorologiques pour les 7 prochains jours
  - Cliquez sur un jour pour voir les prévisions horaires
  - Probabilité de précipitations codée par couleur
  - Inclut les plages de température et les conditions météorologiques pour chaque jour

- **Détails météorologiques** : Inclut :
  - Température ressentie
  - Humidité et point de rosée
  - Vitesse et direction du vent
  - Pression et visibilité
  - Indice UV et qualité de l'air
  - Heures de lever et de coucher du soleil

### Navigation

- **Barre de recherche** : Trouvez la météo pour n'importe quel emplacement
  - Les recherches récentes sont enregistrées automatiquement
  - Recherche par nom de ville, code postal ou coordonnées

- **Sélecteur de thème** : Basculez entre les thèmes clair, sombre ou système

- **Barre de menu** : Accédez à des fonctionnalités et paramètres supplémentaires
  - Fichier : Nouvelle fenêtre, paramètres, quitter
  - Affichage : Basculer les éléments de l'interface, actualiser les données, cartes météo et radar
  - Favoris : Gérer les emplacements enregistrés
  - Aide : Visionneuse de documentation, visionneuse de journaux, à propos, vérifier les mises à jour

## Cartes météo et radar

La fonction Cartes météo et radar fournit des visualisations interactives des conditions météorologiques.

### Accès aux cartes météo

1. Cliquez sur **Affichage** dans la barre de menu
2. Sélectionnez **Cartes météo et radar**
3. La boîte de dialogue des cartes météo s'ouvrira avec plusieurs onglets

### Fonctionnalités

#### Onglet Radar
- **Type de carte** : Basculez entre différentes cartes de base (OpenStreetMap, OpenTopoMap, Stamen Terrain)
- **Couche** : Activez/désactivez les superpositions radar et satellite
- **Recherche** : Trouvez des emplacements par nom ou coordonnées

#### Onglet Température
- Visualisez les variations de température par région
- Basculez entre Celsius et Fahrenheit
- Ajustez l'opacité de la superposition de température

#### Onglet Précipitations
- Voir les précipitations actuelles et prévues
- Basculez entre différentes couches de précipitations
- Affichez la pluie, la neige et d'autres types de précipitations

#### Onglet Vent
- Visualisez la vitesse et la direction du vent
- Basculez entre les flèches de vent ou les lignes de courant
- Ajustez les unités de vitesse du vent (km/h, m/s, mph, nœuds)

### Utilisation de la carte
- **Zoom** : Utilisez la molette de la souris ou les boutons +/-
- **Déplacement** : Cliquez et faites glisser la carte
- **Recherche** : Entrez un emplacement dans la zone de recherche et appuyez sur Entrée
- **Couches** : Activez/désactivez différentes couches météorologiques à l'aide des commandes
- **Plein écran** : Cliquez sur le bouton plein écran pour une vue plus grande

### Astuces
- La carte se centrera automatiquement sur votre position actuelle si les services de localisation sont activés
- Cliquez sur la carte pour obtenir des informations météorologiques détaillées pour cet emplacement
- Utilisez les commandes de la chronologie pour afficher les données de prévision pour différents moments
- Faites un clic droit sur la carte pour définir un marqueur ou obtenir des coordonnées

## Fonctionnalités

### Favoris

- **Ajouter aux favoris** : Cliquez sur l'étoile (☆) pour enregistrer un emplacement

- **Voir les favoris** : Accédez aux emplacements enregistrés depuis le menu Favoris
  - Réorganisez les favoris par glisser-déposer
  - Faites un clic droit pour des actions rapides

- **Synchroniser les favoris** : Activez la synchronisation dans les paramètres

- **Retirer des favoris** : Cliquez sur l'étoile remplie (★) pour supprimer

### Paramètres

1. Cliquez sur l'icône d'engrenage (⚙️) ou allez dans Menu > Paramètres
2. Configurez des options comme :
   - **Général** : Langue, thème, unités
   - **Météo** : Paramètres du fournisseur, fréquence de mise à jour
   - **Affichage** : Disposition, animations, taille de police
   - **Notifications** : Alertes météo, alertes de pluie
   - **Avancé** : Cache, journalisation, options développeur
3. Cliquez sur "Enregistrer" pour appliquer les modifications

### Interface en ligne de commande

```bash
# Utilisation de base
weather-app [emplacement] [options]

# Exemples
weather-app "Paris, FR"
weather-app --provider openweathermap --units metric
weather-app --config ~/.config/weather/config.ini

# Options
  -h, --help            Afficher le message d'aide et quitter
  -v, --version         Afficher les informations de version
  -c, --config FICHIER  Spécifier le fichier de configuration
  -d, --debug           Activer le mode débogage
  --provider FOURNISSEUR   Définir le fournisseur météo
  --units {metric,imperial}
                        Définir le système d'unités
  --lang LANGUE         Définir le code de langue
  --theme {clair,sombre,systeme}
                        Définir le thème de couleur
  --no-gui              Exécuter en mode console
```

## Raccourcis clavier

### Raccourcis globaux

| Raccourci | Action |
|-----------|--------|
| `Ctrl + F` | Placer le curseur dans la barre de recherche |
| `Ctrl + ,` | Ouvrir les paramètres |
| `Ctrl + Q` | Quitter l'application |
| `F1` | Afficher l'aide |
| `Échap` | Fermer les boîtes de dialogue ou effacer la recherche |
| `F5` | Actualiser les données météo |
| `Ctrl + R` | Actualiser toutes les données |
| `Ctrl + W` | Fermer la fenêtre actuelle |
| `Ctrl + N` | Nouvelle fenêtre |

### Raccourcis de navigation

| Raccourci | Action |
|-----------|--------|
| `Ctrl + Tab` | Basculer entre les emplacements |
| `Ctrl + F` | Basculer les favoris |
| `Ctrl + L` | Basculer la liste des emplacements |
| `Ctrl + M` | Basculer la vue carte |

## Astuces et conseils

- **Clic droit** sur n'importe quelle carte météo pour des actions rapides
- **Double-clic** sur la température pour basculer entre Celsius et Fahrenheit
- **Clic milieu** sur la carte pour définir un emplacement personnalisé
- Utilisez la **molette de la souris** sur la prévision pour faire défiler les heures
- **Glissez-déposez** pour réorganiser les emplacements favoris
- **Épinglez** la fenêtre pour qu'elle reste au-dessus des autres applications
- Utilisez l'icône de la **zone de notification** pour un accès rapide

### Visionneuse de documentation

- Accédez à la documentation Markdown intégrée depuis le menu Aide
- Parcourez une documentation complète
- Fonction de recherche pour trouver des sujets spécifiques
- Zoom avant/arrière pour une meilleure lisibilité
- Table des matières pour une navigation facile

### Visionneuse de journaux

- Affichez les journaux d'application depuis le menu Aide
- Filtrez les journaux par niveau (Débogage, Info, Avertissement, Erreur)
- Recherchez dans les messages de journal
- Copiez les journaux dans le presse-papiers pour le dépannage

### Cartes météo
- Accédez aux cartes météo depuis le menu Affichage
- Carte interactive avec plusieurs couches :
  - Température
  - Précipitations
  - Vitesse du vent
  - Couverture nuageuse
- Déplacez-vous et zoomez pour explorer différentes régions
- Cliquez sur la carte pour obtenir la météo pour cet emplacement

## Dépannage

Si vous rencontrez des problèmes :
1. Vérifiez votre connexion Internet
2. Vérifiez vos clés API dans les Paramètres
3. Essayez de passer à un autre fournisseur météo
4. Vérifiez les journaux de l'application pour les erreurs
5. Redémarrez l'application
6. Réinitialisez les paramètres si nécessaire

Pour une aide supplémentaire, veuillez visiter notre [dépôt GitHub](https://github.com/Nsfr750/weather) ou consulter le [Guide de dépannage](troubleshooting.md).

## Commentaires

Nous apprécions vos commentaires ! N'hésitez pas à nous faire savoir :
- Les fonctionnalités que vous aimeriez voir
- Les bogues que vous rencontrez
- Votre expérience avec l'application

Vous pouvez soumettre vos commentaires via l'application (Aide > Envoyer des commentaires) ou sur notre page [GitHub Issues](https://github.com/Nsfr750/weather/issues).

# Guide de dépannage

Ce guide vous aide à résoudre les problèmes courants que vous pourriez rencontrer lors de l'utilisation de l'application Météo.

## Table des matières
- [Problèmes courants](#problèmes-courants)
- [Fichiers journaux](#fichiers-journaux)
- [Débogage](#débogage)
- [Problèmes de performances](#problèmes-de-performances)
- [Questions fréquemment posées](#questions-fréquemment-posées)
- [Obtenir de l'aide](#obtenir-de-laide)

## Problèmes courants

### 1. L'application ne démarre pas

**Symptômes** :
- L'application plante immédiatement après le lancement
- Vous voyez un message d'erreur concernant des dépendances manquantes
- La fenêtre de l'application n'apparaît pas

**Solutions** :
1. **Vérifiez les exigences système** :
   - Assurez-vous d'avoir Python 3.10 ou une version ultérieure installé
   - Vérifiez que toutes les dépendances système sont installées
   - Vérifiez l'espace disque et les autorisations

2. **Réinstallez les dépendances** :
   ```bash
   # Activez d'abord votre environnement virtuel
   pip install --upgrade -r requirements.txt
   ```

3. **Vérifiez les logiciels conflictuels** :
   - Désactivez temporairement l'antivirus/le pare-feu
   - Fermez les autres applications qui pourraient entrer en conflit

4. **Réinitialisez la configuration** :
   ```bash
   # Sauvegardez d'abord votre configuration
   mv ~/.config/WeatherApp/config.ini ~/.config/WeatherApp/config.ini.bak
   ```

### 2. Aucune donnée météo affichée

**Symptômes** :
- L'application s'ouvre mais affiche "Aucune donnée disponible"
- Les informations météorologiques ne se mettent pas à jour
- L'emplacement ne peut pas être trouvé

**Solutions** :
1. **Vérifiez votre connexion Internet** :
   - Vérifiez que votre appareil est connecté à Internet
   - Essayez d'accéder à un site web dans votre navigateur

2. **Vérifiez les clés API** :
   - Vérifiez si votre clé API est valide et n'a pas expiré
   - Assurez-vous que la clé API a les bonnes autorisations
   - Essayez de régénérer la clé API

3. **État du fournisseur** :
   - Vérifiez si le service météo connaît des perturbations
   - Essayez de passer à un autre fournisseur météo

4. **Services de localisation** :
   - Assurez-vous que les services de localisation sont activés
   - Essayez de saisir l'emplacement manuellement

### 3. Utilisation élevée du processeur ou de la mémoire

**Symptômes** :
- L'application devient lente ou ne répond plus
- Le ventilateur de votre ordinateur tourne fortement
- Les autres applications deviennent lentes

**Solutions** :
1. **Réduisez la fréquence de mise à jour** :
   - Augmentez l'intervalle de mise à jour dans Paramètres > Météo
   - Désactivez les mises à jour de localisation automatiques si elles ne sont pas nécessaires

2. **Désactivez les animations** :
   - Allez dans Paramètres > Affichage
   - Désactivez "Activer les animations"

3. **Effacez le cache** :
   ```bash
   # Linux/macOS
   rm -rf ~/.cache/WeatherApp
   
   # Windows
   rmdir /s /q %LOCALAPPDATA%\WeatherApp\Cache
   ```

4. **Vérifiez les fuites de mémoire** :
   - Surveillez l'utilisation de la mémoire dans le Gestionnaire des tâches
   - Signalez toute augmentation constante de la mémoire

## Fichiers journaux

Les fichiers journaux contiennent des informations détaillées sur les événements et les erreurs de l'application. Ils sont essentiels pour le dépannage.

### Emplacements des journaux

- **Linux/macOS** : `~/.local/share/WeatherApp/logs/`
- **Windows** : `%APPDATA%\WeatherApp\logs\`
- **macOS** : `~/Library/Logs/WeatherApp/`

### Niveaux de journalisation

- **DÉBOGAGE** : Informations détaillées pour le débogage
- **INFO** : Événements généraux de l'application
- **AVERTISSEMENT** : Situations potentiellement problématiques
- **ERREUR** : Erreurs qui permettent à l'application de continuer
- **CRITIQUE** : Erreurs graves qui font planter l'application

### Consultation des journaux

1. **Depuis l'application** :
   - Allez dans Aide > Afficher les journaux
   - Filtrez par niveau de journal
   - Recherchez des termes spécifiques

2. **Depuis la ligne de commande** :
   ```bash
   # Linux/macOS
   tail -f ~/.local/share/WeatherApp/logs/app.log
   ```

## Questions fréquemment posées

### Comment changer d'unités métriques/impériales ?

1. Allez dans Paramètres > Général
2. Sélectionnez votre système d'unités préféré
3. Cliquez sur "Enregistrer"

### Comment signaler un bug ?

1. Vérifiez d'abord si le bug n'a pas déjà été signalé
2. Rassemblez les informations suivantes :
   - Version de l'application
   - Système d'exploitation et version
   - Étapes pour reproduire le bug
   - Messages d'erreur exacts
   - Fichiers journaux pertinents
3. Créez un nouveau problème sur [GitHub](https://github.com/Nsfr750/weather/issues)

## Obtenir de l'aide

Si vous ne trouvez pas de solution à votre problème :

1. **Consultez la documentation** :
   - [Guide d'utilisation](usage.md)
   - [Configuration](configuration.md)
   - [Documentation de l'API](api.md)

2. **Recherchez dans les problèmes existants** :
   - [Problèmes GitHub](https://github.com/Nsfr750/weather/issues)
   - [Questions fréquemment posées](faq.md)

3. **Demandez de l'aide** :
   - Créez un nouveau problème sur GitHub
   - Incluez autant de détails que possible
   - Joignez les fichiers journaux si nécessaire

## Traduction

L'application prend en charge plusieurs langues. Pour ajouter une nouvelle langue :

1. Créez un nouveau fichier de traduction dans le dossier `translations/`
2. Ajoutez des traductions pour toutes les chaînes dans le fichier `translations/en.json`
3. Ajoutez la langue au menu des langues en incluant ces clés :
   - `language_menu` : Le titre du menu (par exemple, "Langue")
   - `language_tip` : Texte d'info-bulle pour le menu des langues (par exemple, "Sélectionner la langue de l'application")

Exemple pour le français (`fr.json`) :
```json
{
  "language_menu": "Langue",
  "language_tip": "Sélectionner la langue de l'application",
  "settings": "Paramètres",
  "weather": "Météo",
  "forecast": "Prévisions",
  "map": "Carte",
  "favorites": "Favoris",
  "help": "Aide"
}
```
