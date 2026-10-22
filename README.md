# Prise de masse sèche

Web app installable (PWA) pour suivre une prise de masse sèche au quotidien.

**App en ligne :** https://corentinnh.github.io/prise-de-masse/

## Fonctions

L'app est organisée en 4 onglets : **Aujourd'hui** (cercles, compléments, repas par moment, idées pour le prochain repas avec « Mes goûts »), **Ajouter** (recherche, portions, récents, favoris, mes repas, copie de la veille, activité), **Progrès** (poids lissé, semaine, activité, mesures) et **Profil** (profil, planning sportif, objectifs, repas composés, sauvegarde).

- **Ajout rapide** : calories et protéines (glucides et lipides facultatifs) sans chercher l'aliment, pour le resto ou chez quelqu'un.
- **Série** : nombre de jours d'affilée avec l'objectif de protéines atteint, et le record.
- **Bilan de la semaine** : moyennes calories / protéines, jours dans la cible, poids moyen, séances faites par rapport au planning, eau. Affiché sur Aujourd'hui le dimanche et le lundi, et toujours dans Progrès.
- **Ajustement guidé** : après 3 semaines de pesées, si le poids lissé monte de plus de 0,5 kg par mois ou stagne 3 semaines, l'app propose −150 ou +150 kcal en un appui.
- **Poids cible** : progression, date estimée au rythme actuel et au rythme conseillé ; la courbe du poids montre la cible et la tendance sur le mois suivant.
- **Courbes des mensurations** : une courbe par tour (bras, taille, poitrine, cuisse) et une phrase qui compare bras et taille sur 4 semaines (plutôt du muscle ou du gras).
- **Récents et favoris** : remettre un aliment déjà noté en un appui, ou copier un repas de la veille.
- **Repas composés** : un repas enregistré une fois (« Mon bowl du midi ») s'ajoute d'un coup.
- **Portions en unités** : œuf, tranche, pot, dose, pièce, cuillère… avec conversion en grammes.
- **Annuler** : chaque suppression ou ajout peut être annulé pendant 6 secondes.
- **Premier lancement** : 3 écrans (profil, objectif, premier repas) pour un nouvel utilisateur.
- **Poids lissé** : moyenne des pesées sur 7 jours et rythme par mois comparé à l'objectif.
- **Dépense mesurée** : après 2 à 3 semaines de repas notés et de pesées, l'app compare ce que tu manges à l'évolution réelle de ton poids pour calculer ta vraie dépense et ajuster les recommandations.
- **Glucides et lipides** : barres avec repères (lipides ≈ 28 % des calories, glucides pour le reste), calculés aussi pour les anciens repas.
- **Protéines par repas** : repère de 25 g minimum sur le petit-déj, le déjeuner et le dîner.
- **Eau** : compteur avec liste dépliante (250 ml, 330 ml, 500 ml, 750 ml, 1 L), correction en cas d'erreur (−250 ml, −500 ml, remise à 0) et objectif de 35 ml par kg.
- **Planning du lendemain** : 4 repas générés selon les objectifs et les goûts, changeables un par un, ajoutés au journal le jour même, avec la liste de courses à cocher et à copier.
- **Repas** : aliment + grammage → calories et protéines calculées automatiquement (liste d'aliments intégrée, et les aliments saisis à la main sont retenus).
- **Bases d'aliments hors connexion** : liste de l'app, table officielle **Ciqual 2025** (environ 3 200 aliments et plats) et environ 150 plats du monde. Recherche souple et choix parmi plusieurs résultats.
- **Estimation en ligne** : pour un produit de marque absent des bases, recherche dans [Open Food Facts](https://world.openfoodfacts.org) (nécessite du réseau).
- **Profil** : âge, taille, sexe, objectif (perte de poids, maintien, prise de masse sèche) → IMC, dépense estimée et calories / protéines recommandées, applicables en un clic.
- **Activité physique** : séances par jour (une trentaine de sports, intensité, durée) avec dépense estimée ; la moyenne des 14 derniers jours sert au calcul de la dépense.
- **Planning sportif** (Profil) : séances prévues et pas habituels pour chaque jour de la semaine, avec « Copier sur » d'autres jours. La dépense prévue compte pour les jours sans activité notée, une séance notée remplace le prévu. Dans Ajouter, la séance du jour se note en un appui (« Fait comme prévu » ou « Pas fait »). Un bandeau propose de mettre à jour les objectifs quand la recommandation change de plus de 100 kcal.
- **Semaines types** : plusieurs plannings enregistrés (« Normale », « Avec match », « Vacances »…), à créer, dupliquer, renommer ou supprimer ; celle qui est active sert aux calculs.
- **Noter automatiquement** : case à cocher qui ajoute toute seule au journal, une fois par jour, les séances et les pas prévus (y compris les jours où l'app n'a pas été ouverte). Une séance ratée se retire avec ×.
- **Objectifs** : cercles de progression calories / protéines pour la journée.
- **Idées pour compléter** : suggestions de repas selon ce qu'il reste à manger et l'heure, ajoutables en un clic. « Mes goûts » : soit seulement des plats avec les aliments cochés, soit un mode découverte avec des plats du monde qui changent chaque jour. Recherche dans toute la base pour ajouter un aliment ou un plat aimé (un plat aimé devient une idée de repas) et « Afficher plus » pour une liste étendue.
- **Compléments** : cases whey et créatine.
- **Poids et mensurations** : pesées, tours de taille / bras / poitrine / cuisse, courbe et historique.
- **Sauvegarde** : export / import JSON et résumé texte à copier. Avant un import, l'app montre ce que contient le fichier et garde une copie du journal pour pouvoir revenir en arrière. Un bandeau rappelle d'exporter quand le dernier export date de plus de 7 jours.
- **Hors connexion** : fonctionne sans réseau une fois installée.

## Installation

- **iPhone** : ouvrir le lien dans Safari → Partager → « Sur l'écran d'accueil ».
- **PC (Chrome / Edge)** : icône « Installer » dans la barre d'adresse.

## Données

Toutes les données restent **sur l'appareil** (stockage local du navigateur). Rien n'est envoyé sur un serveur ni dans ce repo. Seul le nom d'un aliment recherché est envoyé à Open Food Facts quand on utilise la recherche. Chaque personne qui utilise l'app a son propre journal, séparé.

La page n'autorise que ses propres fichiers et Open Food Facts (règle `Content-Security-Policy`), et n'envoie pas d'adresse d'origine aux recherches. Les fichiers d'export sont exclus du repo par `.gitignore`.

Penser à faire un export régulier : supprimer l'app ou effacer les données du navigateur efface le journal.

## Structure

| Fichier | Rôle |
|---|---|
| `index.html` | Toute l'app : interface, styles et logique |
| `sw.js` | Service worker : cache hors connexion et mises à jour |
| `manifest.webmanifest` | Nom, icônes et affichage de l'app installée |
| `icons/` | Icônes de l'app |
| `fonts/` | Polices hébergées en local (Unbounded, Manrope) |
| `data/ciqual-2025.json` | Table Ciqual 2025 réduite (nom, kcal, protéines, glucides, lipides pour 100 g) |
| `data/plats-du-monde.json` | Plats du monde absents de Ciqual, valeurs moyennes estimées |

## Sources et calculs

- **Ciqual 2025** : ANSES, Table de composition nutritionnelle des aliments Ciqual 2025, Licence Ouverte Etalab 2.0 (fichier repris du dépôt public d'Open Food Facts).
- **Plats du monde** : valeurs moyennes estimées, à prendre comme ordre de grandeur.
- **Open Food Facts** : données sous licence ODbL.
- **Métabolisme de base** : formule de Mifflin-St Jeor. Dépense = métabolisme × 1,2 (vie quotidienne) + moyenne des activités notées.
- **Dépense mesurée** : apports moyens des jours complets − variation du poids lissé × 7 700 kcal/kg, sur 4 semaines (au moins 10 jours notés et 14 jours de pesées).
- **Plats du monde, glucides / lipides** : seuls kcal et protéines sont estimés ; le reste des calories est réparti moitié glucides, moitié lipides.
- **Activités** : valeurs MET du Compendium des activités physiques, dépense nette = (MET − 1) × poids × durée.
- **Marche** : saisie au nombre de pas de la journée. Longueur de pas ≈ 41,4 % de la taille, coût net ≈ 0,5 kcal/kg/km (ACSM) ; les 3 000 premiers pas sont déjà comptés dans la vie quotidienne.
- **Recommandations** : perte de poids −20 %, maintien, prise de masse sèche +10 % ; protéines 2 g/kg (1,6 g/kg en maintien).

Aucune dépendance ni étape de build : le site est servi tel quel par GitHub Pages depuis la branche `main`.
