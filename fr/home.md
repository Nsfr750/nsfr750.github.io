---
lang: fr
lang-niv: source
lang-ref: 001-jbk
layout: page
title: 'Accueil'
---

# Bienvenue sur mon Hub de Projets

Bonjour ! Je suis Nsfr750, un développeur passionné et enthousiaste de l'open source. C'est ici que je partage mes projets, mes réflexions et mes découvertes avec le monde entier.

## Derniers Articles de Blog

{% for post in site.posts limit:3 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Lire la suite...]({{ post.url }})

{% endfor %}

[Voir tous les articles](blog) | [Parcourir par catégorie](categories)

## Projets à la Une

Voici quelques-uns de mes projets open source les plus populaires :

- [3D Filament Manager](https://github.com/Nsfr750/3D_Filament_Manager) - Gérez facilement vos filaments d'impression 3D
- [Simulateur CDE550](https://github.com/Nsfr750/CDE550-sim) - Simulateur pour contrôleur de moteur Nidec CDE550
- [Email Duplicate Cleaner](https://github.com/Nsfr750/EmailDuplicateCleaner) - Nettoyez efficacement les e-mails en double

[Voir tous les projets](projects)

## Me Contacter

- [À Propos](about) - En savoir plus sur mon travail et mes centres d'intérêt
- [Documentation](docs) - Guides détaillés pour mes projets
- [Soutien](support) - Vous aimez mon travail ? Pensez à me soutenir
- [Contact](contact) - Contactez-moi pour des collaborations ou des questions

---

Dernière mise à jour : {{ site.time | date: "%d/%m/%Y" }}
