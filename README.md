# Prise de masse sèche

Web app installable (PWA) pour suivre une prise de masse sèche au quotidien.

**App en ligne :** https://corentinnh.github.io/prise-de-masse/

## Fonctions

- **Repas** : aliment + grammage → calories et protéines calculées automatiquement (liste d'aliments intégrée, et les aliments saisis à la main sont retenus).
- **Bases d'aliments hors connexion** : liste de l'app, table officielle **Ciqual 2025** (environ 3 200 aliments et plats) et environ 150 plats du monde. Recherche souple et choix parmi plusieurs résultats.
- **Estimation en ligne** : pour un produit de marque absent des bases, recherche dans [Open Food Facts](https://world.openfoodfacts.org) (nécessite du réseau).
- **Profil** : âge, taille, sexe, objectif (perte de poids, maintien, prise de masse sèche) → IMC, dépense estimée et calories / protéines recommandées, applicables en un clic.
- **Activité physique** : séances par jour (type, intensité, durée) avec dépense estimée ; la moyenne des 14 derniers jours sert au calcul de la dépense.
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
| `data/ciqual-2025.json` | Table Ciqual 2025 réduite (nom, kcal, protéines, glucides, lipides pour 100 g) |
| `data/plats-du-monde.json` | Plats du monde absents de Ciqual, valeurs moyennes estimées |

## Sources et calculs

- **Ciqual 2025** : ANSES, Table de composition nutritionnelle des aliments Ciqual 2025, Licence Ouverte Etalab 2.0 (fichier repris du dépôt public d'Open Food Facts).
- **Plats du monde** : valeurs moyennes estimées, à prendre comme ordre de grandeur.
- **Open Food Facts** : données sous licence ODbL.
- **Métabolisme de base** : formule de Mifflin-St Jeor. Dépense = métabolisme × 1,2 (vie quotidienne) + moyenne des activités notées.
- **Activités** : valeurs MET du Compendium des activités physiques, dépense nette = (MET − 1) × poids × durée.
- **Recommandations** : perte de poids −20 %, maintien, prise de masse sèche +10 % ; protéines 2 g/kg (1,6 g/kg en maintien).

Aucune dépendance ni étape de build : le site est servi tel quel par GitHub Pages depuis la branche `main`.
