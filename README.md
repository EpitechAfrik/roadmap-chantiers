# Chantiers digitaux AEIG

Page de pilotage des chantiers (Odoo, Zeno, Mydocs) : **sprint en cours**, sprint suivant,
gros sujets et deadlines, backlog, historique. Site statique publié par GitHub Pages.

## D'où viennent les données

| Fichier | Contenu | Mise à jour |
|---|---|---|
| `sprints.js` | sprints, gros sujets, backlog, imprévus | **généré** par le tableau de bord local (onglet *Sprints* → *Publier sur la page*) — ne pas modifier à la main |
| `data.js` | réalisations déjà livrées et pistes à cadrer | à la main, rarement |

## Fonctionnement des sprints

- Un sprint dure **une semaine** (lundi → vendredi), avec un objectif et une **capacité en jours par personne**.
- Les sous-sujets sont estimés en jours ; on ne s'engage pas sur plus que la capacité.
- Un **imprévu** est soit *traité dans le sprint* (il consomme de la capacité), soit *basculé au sprint suivant*
  (il devient un sous-sujet du prochain sprint).
- À la clôture, chaque sous-sujet non fini est basculé au sprint suivant (« reporté de Sxx ») ou renvoyé au backlog.

## Aperçu en local

```bash
python3 -m http.server 8799
```
