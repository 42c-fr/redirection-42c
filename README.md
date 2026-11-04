# Redirection de 42c.fr vers www.42c.fr

Le site de 42c est servi sur `https://www.42c.fr` (Scaleway Edge Services). La racine `42c.fr` ne peut pas y pointer : un CNAME est interdit à la racine d'une zone, et la zone `42c.fr` (OVH) ne propose pas d'ALIAS. Ce dépôt, publié par GitHub Pages sur le domaine `42c.fr`, renvoie toute adresse `https://42c.fr/<chemin>` vers `https://www.42c.fr/<chemin>`.

- `index.html` et `404.html` : redirection immédiate (JavaScript qui conserve le chemin, balise `meta refresh` en secours). GitHub Pages ne sait pas émettre de 301 ; Google traite une redirection meta instantanée comme permanente.
- `CNAME` : domaine personnalisé de GitHub Pages.
- DNS (zone `42c.fr` chez OVH) : racine en A vers `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`, aucun autre A ni AAAA sur la racine.

Aucun secret, aucune donnée : ce dépôt est public par nécessité (GitHub Pages sur GitHub Free).

Décision : `JOURNAL.md` du projet d'automatisation, 04/11/2026.
