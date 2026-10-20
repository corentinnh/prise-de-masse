# Prise de masse sèche

Web app installable (PWA) pour suivre une prise de masse sèche au quotidien.

**App en ligne :** https://corentinnh.github.io/prise-de-masse/

## Fonctions

- **Repas** : aliment + grammage → calories et protéines calculées automatiquement (liste d'aliments intégrée, et les aliments saisis à la main sont retenus).
- **Estimation** : pour un aliment inconnu, recherche des valeurs pour 100 g dans [Open Food Facts](https://world.openfoodfacts.org) (nécessite du réseau).
- **Objectifs** : cercles de progression calories / protéines pour la journée.
- **Idées pour compléter** : suggestions de repas selon ce qu'il reste à manger et l'heure, ajoutables en un clic.
- **Compléments** : cases whey et créatine.
- **Poids et mensurations** : pesées, tours de taille / bras / poitrine / cuisse, courbe et historique.
- **Sauvegarde** : export / import JSON et résumé texte à copier.
- **Hors connexion** : fonctionne sans réseau une fois installée.

## Installation

- **iPhone** : ouvrir le lien dans Safari → Partager → « Sur l'écran d'accueil ».
- **PC (Chrome / Edge)** : icône « Installer » dans la barre d'adresse.

## Données

Toutes les données restent **sur l'appareil** (stockage local du navigateur). Rien n'est envoyé sur un serveur ni dans ce repo. Seul le nom d'un aliment recherché est envoyé à Open Food Facts quand on utilise la recherche. Chaque personne qui utilise l'app a son propre journal, séparé.

Penser à faire un export régulier : supprimer l'app ou effacer les données du navigateur efface le journal.

## Structure

| Fichier | Rôle |
|---|---|
| `index.html` | Toute l'app : interface, styles et logique |
| `sw.js` | Service worker : cache hors connexion et mises à jour |
| `manifest.webmanifest` | Nom, icônes et affichage de l'app installée |
| `icons/` | Icônes de l'app |
| `fonts/` | Polices hébergées en local (Bricolage Grotesque, IBM Plex Sans / Mono) |

Aucune dépendance ni étape de build : le site est servi tel quel par GitHub Pages depuis la branche `main`.
