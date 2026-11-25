# Suidepro — Suivi de production

Application de suivi de plusieurs lignes de production par listes de tâches, en trois onglets : **Production**, **Social**, **À faire**.
Tout tient dans `index.html`. Les données sont stockées dans le navigateur (IndexedDB) et restent après un redémarrage du PC.

## Utilisation rapide
- **Nouvelle liste** : bouton en haut (ou `Alt+N`). Cliquer sur le titre pour le renommer.
- **Ajouter une tâche** : taper dans le champ de la liste puis `Entrée` (le champ reste actif pour enchaîner).
  `!` en début de texte = importante, `!!` = urgente.
- **Priorité** : clic sur la pastille ronde (normale → importante → urgente).
- **Réorganiser** : glisser une tâche (dans sa liste ou vers une autre), glisser une liste par son en-tête.
  Déposer une liste sur un onglet la déplace dans cet onglet.
- **Trier par priorité** : icône ⇅ de la liste.
- **Terminer** : cocher. Les tâches terminées descendent dans « Terminées (n) », repliable, avec « Effacer ».
- **Supprimer** : icône corbeille (liste) ou ✕ (tâche). Toujours annulable quelques secondes (ou `Ctrl+Z`).
- **Onglets** : `Ctrl+1`, `Ctrl+2`, `Ctrl+3`.
- **Sauvegarder / Restaurer** : export/import d'un fichier `.json` (utile pour changer de PC ou en sécurité).

## Utilisation locale
Double-cliquer sur `index.html`. (L'installation en application nécessite de passer par GitHub Pages, voir ci-dessous.)

> Les données sont liées à l'adresse de la page : la version locale (`file://`) et la version GitHub Pages ont chacune leurs propres données.
> Utilisez « Sauvegarder » / « Restaurer » pour passer de l'une à l'autre.

## Mise en ligne sur GitHub Pages (PWA installable)
1. Créer un dépôt sur GitHub et y déposer tous les fichiers de ce dossier (`index.html`, `manifest.webmanifest`, `sw.js`, `icons/`).
2. Dans le dépôt : **Settings → Pages → Branch : `main` / `(root)` → Save**.
3. Ouvrir l'adresse donnée (`https://<utilisateur>.github.io/<depot>/`) dans Chrome ou Edge.
4. Cliquer sur l'icône **Installer** dans la barre d'adresse : l'application apparaît avec son icône dans le menu Démarrer et fonctionne hors ligne.

Lors d'une mise à jour d'`index.html`, changer `VERSION` dans `sw.js`.
