---
lang: fr
lang-niv: fonto
lang-ref: 010-jbk
layout: doc
order: 1
title: 'Gestionnaire de Filament 3D'
---

# Gestionnaire de Filament 3D

![Gestionnaire de Filament 3D](assets/logo.png)

Une application de bureau pour gérer votre inventaire de filaments d'impression 3D. Gardez une trace des matériaux, couleurs, utilisations, coûts et paramètres de tranchage au même endroit.

## ✨ Fonctionnalités

* **🌐 Support Multilingue** : Disponible en anglais et en italien
* **🎨 Interface Moderne** : Interface épurée avec icônes émojis et support des thèmes (mode clair/sombre)
* **📊 Gestion Complète des Filaments** :
  * Stockez des informations détaillées sur les filaments (marque, matériau, couleur, diamètre, etc.)
  * Suivez l'utilisation et la quantité restante de filament
  * Calculez les coûts des matériaux
  * Suivi des prix et historique
  * Analyse interactive des prix avec visualisations
  * Comparaison des prix des fournisseurs
* **⚙️ Intégration avec les Logiciels de Tranchage** :
  * Enregistrez et gérez les profils de tranchage (Cura, PrusaSlicer, eQuidiSlicer)
  * Profils d'impression personnalisés pour différentes imprimantes
* **🔍 Recherche et Filtrage Avancés** :
  * Recherche par n'importe quelle propriété de filament
  * Tri par n'importe quelle colonne
  * Filtrage par type de matériau, couleur ou étiquettes personnalisées
* **📂 Importation/Exportation** :
  * Sauvegardez et restaurez votre bibliothèque de filaments
  * Partagez des profils avec d'autres
  * Prise en charge de l'importation/exportation groupée
* **🔒 Sécurité des Données** :
  * Paramètres enregistrés dans le répertoire `config/`
  * Aucune connexion Internet requise
  * Stockage des données en local

## 🚀 Prérequis

* Python 3.8+
* Paquets requis (installés automatiquement) :
  * `lxml` - Traitement XML rapide
  * `pillow` - Traitement d'images pour les icônes
  * `matplotlib` - Visualisation des données pour l'analyse des prix

## 🛠️ Installation

### Prérequis

* Python 3.8 ou supérieur
* Git (optionnel, pour le développement)

### Étapes d'Installation

1. **Clonez le dépôt** (ou téléchargez-le en ZIP) :

   ```bash
   git clone https://github.com/Nsfr750/3D_Filament_Manager.git
   cd 3D_Filament_Manager
   ```

2. **Créez et activez un environnement virtuel** (recommandé) :

   ```bash
   # Sur Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # Sur macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Installez les dépendances** :

   ```bash
   pip install -r requirements.txt
   ```

4. **Lancez l'application** :

   ```bash
   python main.py
   ```

### Stockage des Données

* Les profils de filament sont stockés dans le répertoire `fdm/`
* Les paramètres de l'application sont enregistrés dans le répertoire `config/`
* Les journaux sont écrits dans le répertoire `logs/`

## 🤝 Contribution

Nous apprécions les contributions ! Voici comment vous pouvez aider :

* Signalez des bogues en ouvrant une [issue](https://github.com/Nsfr750/3D_Filament_Manager/issues)
* Proposez de nouvelles fonctionnalités ou des améliorations
* Soumettez des demandes de tirage avec des modifications de code
* Aidez à améliorer la documentation
* Traduisez l'application dans de nouvelles langues

### Configuration du Développement

1. Forkez le dépôt
2. Créez une branche de fonctionnalité (`git checkout -b feature/feature-impressionnante`)
3. Validez vos modifications (`git commit -m 'Ajouter une fonctionnalité impressionnante'`)
4. Poussez vers la branche (`git push origin feature/feature-impressionnante`)
5. Ouvrez une demande de tirage

### Style de Code

* Suivez les directives [PEP 8](https://www.python.org/dev/peps/pep-0008/)
* Utilisez les indications de type pour une meilleure clarté du code
* Écrivez des docstrings pour toutes les fonctions et classes publiques

## 📜 Licence

Ce projet est sous licence **GNU General Public License v3.0**. Voir le fichier [LICENCE](LICENSE) pour plus de détails.

## 🙏 Soutien

Si vous trouvez ce projet utile, envisagez de soutenir son développement :

* ⭐ Ajoutez une étoile au dépôt
* 🐛 Signalez des problèmes
* 💡 Proposez de nouvelles fonctionnalités
* 💰 [Soutenez le projet sur GitHub](https://github.com/sponsors/Nsfr750)

## 📞 Contact

* GitHub : [@Nsfr750](https://github.com/Nsfr750)
* Email : nsfr750@yandex.com

---

### Soutenez le Développeur

Si vous trouvez cette application utile, veuillez envisager de soutenir le développeur :

* **PayPal** : [https://paypal.me/3dmega](https://paypal.me/3dmega)
* **GitHub** : [https://github.com/Nsfr750](https://github.com/Nsfr750)
