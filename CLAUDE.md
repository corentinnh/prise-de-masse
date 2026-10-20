# Règles du projet

PWA statique servie par GitHub Pages depuis `main` (racine). Pas de build, pas de framework, pas de dépendances.

## À respecter à chaque modification

- **Toujours changer `VERSION` dans `sw.js`** quand un fichier de l'app change (format `pdms-AAAA-MM-JJ-N`), sinon les téléphones gardent l'ancienne version en cache.
- Un nouveau fichier statique (icône, police…) doit être ajouté à la liste `ASSETS` de `sw.js`.
- **Aucune donnée personnelle dans le repo** : le repo est public. Jamais de fichier d'export (`prise-de-masse-*.json`) ni de vraies valeurs de repas, poids ou mensurations.
- L'app doit marcher **hors connexion** : pas de CDN, tout est local (polices dans `fonts/`). Seule exception : la recherche Open Food Facts (bouton « Chercher les calories et protéines »), qui reste facultative. Sans réseau, l'app doit fonctionner normalement.
- Open Food Facts limite la recherche à 10 requêtes par minute et par IP : jamais de recherche automatique pendant la frappe, uniquement au clic.
- Les données sont dans `localStorage`, clé `pdms-v1`. Ne pas changer la clé ni casser la forme des données (`jours`, `aliments`, `mesures`, `objectifs`) : ça effacerait le journal des utilisateurs. Si la forme doit évoluer, écrire une migration au chargement.
- Garder le format d'export / import compatible avec les exports existants.
- Cible principale : **iPhone en mode écran d'accueil** (Safari). Tester à 390 px de large, thème clair et sombre.
- Interface et textes en français, ton simple et direct.
- Messages de commit en français.

## Tester en local

```
python3 -m http.server 8000
```
puis ouvrir http://localhost:8000 (le service worker a besoin de http, pas de `file://`).
