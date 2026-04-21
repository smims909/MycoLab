# MycoLab v6.8.0

Application web de suivi de cultures mycologiques — fichier HTML unique, zéro dépendance.

## Fonctionnalités

- **Recettes** — formulation de substrats par volumes/poids, gestion des ingrédients
- **Cultures** — création de lots avec snapshot figé de la recette, journal d'événements horodatés
- **Suivi** — Gantt interactif, mini-calendrier 28j, températures récentes (lecture seule)
- **Ingrédients** — référentiel avec masse volumique et pH
- Bilingue FR/EN, dark mode persisté, export JSON, impression PDF par lot

## Utilisation

Ouvrir `mycolab.html` dans un navigateur. Aucune installation, aucune dépendance.

Les données sont stockées dans le `localStorage` du navigateur.  
**Sauvegarde** : Menu "Sauvegarde" → télécharger un JSON.

## GitHub Pages

Settings → Pages → source `main` / `root`  
→ `https://<user>.github.io/<repo>/mycolab.html`

## Architecture

- Point unique de modification : `updateCulture(id, action, payload)`
- Culture autonome : snapshot figé, status/temp stockés après chaque event
- Suivi = lecture seule stricte
- Aucun calcul au rendu

## Données

Stockage local uniquement. Aucune donnée envoyée à un serveur.
