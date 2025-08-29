---
lang: it
lang-niv: fonto
lang-ref: 001-jbk
layout: page
title: 'Home'
---

# Benvenuti nel Mio Hub di Progetti

Ciao! Sono Nsfr750, uno sviluppatore appassionato e sostenitore dell'open-source. Qui condivido i miei progetti, pensieri e scoperte con il mondo.

## Ultimi Articoli del Blog

{% for post in site.posts limit:3 %}
### [{{ post.title }}]({{ post.url }})

{{ post.excerpt | strip_html | truncatewords: 30 }}

[Leggi di più...]({{ post.url }})

{% endfor %}

[Vedi tutti gli articoli](/blog) | [Esplora per categoria](/categories)

## Progetti in Evidenza

Ecco alcuni dei miei progetti open-source più popolari:

- [3D Filament Manager](https://github.com/Nsfr750/3D_Filament_Manager) - Gestisci i tuoi filamenti per la stampa 3D con facilità
- [Simulatore CDE550](https://github.com/Nsfr750/CDE550-sim) - Simulatore per il controller motore Nidec CDE550
- [Email Duplicate Cleaner](https://github.com/Nsfr750/EmailDuplicateCleaner) - Pulisci le email duplicate in modo efficiente

[Vedi tutti i progetti](/projects)

## Contatti

- [Chi Sono](/about) - Scopri di più sul mio lavoro e i miei interessi
- [Documentazione](/docs) - Guide dettagliate per i miei progetti
- [Supporto](/support) - Ti piace il mio lavoro? Considera di supportarmi
- [Contatti](/contact) - Contattami per collaborazioni o domande

---

Ultimo aggiornamento: {{ site.time | date: "%d/%m/%Y" }}
