# Chantiers digitaux AEIG

Page de suivi des chantiers (Odoo, Zeno, Mydocs) : ce qui est fait, en cours, à venir.
Site statique, sans build : `index.html` (mise en page) + `data.js` (contenu).

## Mettre à jour

Tout le contenu est dans **`data.js`**. Pour un sujet :

```js
{ title: "Gestion du courrier", period: "octobre", status: "en_cours", owner: "Pissano",
  update: "Cahier des charges validé, développement démarré." }
```

- `status` : `fait` · `en_cours` · `en_attente` · `a_venir` · `bloque` · `a_preciser` · `annule`
- `label` (optionnel) : libellé affiché à la place du statut standard (ex. `"En finalisation"`, `"Vigilance"`)
- `update` : ce qui a bougé récemment, en une phrase
- `blocker` : affiché en rouge
- `details` : sous-sujets dépliables `[{ text, status }]`

Pensez à changer `updated` (date en haut de la page) à chaque mise à jour, puis commit + push :
GitHub Pages republie automatiquement en une minute environ.

## Aperçu en local

```bash
python3 -m http.server 8799
```

puis ouvrir http://localhost:8799

## Publication (GitHub Pages)

Settings → Pages → Source : *Deploy from a branch* → branche `main`, dossier `/ (root)`.
