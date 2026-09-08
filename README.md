# La Cave · Le Rooftop · Le Bistro — Site vitrine

Site vitrine à page unique pour **La Cave, Le Rooftop et Le Bistro** (N'Djamena, Tchad) :
cave à vins & spiritueux, lounge-bar rooftop et restaurant.

- **Accueil** : présentation, vidéo d'entrée (lecture automatique), les 3 maisons, événements, service traiteur
- **Menu** : carte complète par catégories, avec photo et nom de chaque plat
- **Réservation** : formulaire qui envoie la demande directement sur WhatsApp (+235 63 67 46 46)
- Bouton **WhatsApp flottant** sur toutes les pages

Site 100% statique : un seul fichier `index.html` (photos et vidéo intégrées directement dedans). Aucune dépendance, aucune étape de build.

## Déployer sur Vercel

### Option A — via GitHub (recommandé)

1. Créer un nouveau dépôt sur [github.com/new](https://github.com/new) (par ex. `la-cave-ndjamena`), **sans** README/gitignore (déjà présents ici).
2. Dans ce dossier, lier et pousser le dépôt :
   ```bash
   git remote add origin https://github.com/<votre-utilisateur>/la-cave-ndjamena.git
   git branch -M main
   git push -u origin main
   ```
3. Aller sur [vercel.com/new](https://vercel.com/new), cliquer **Import** sur ce dépôt GitHub.
4. Vercel détecte un site statique automatiquement (aucun réglage à changer) → **Deploy**.
5. Le site est en ligne sur une adresse `https://la-cave-ndjamena.vercel.app` (personnalisable ensuite dans Project Settings → Domains).

### Option B — directement depuis cet ordinateur (CLI Vercel)

```bash
npm i -g vercel
vercel login
vercel --prod
```
Suivre les questions à l'écran (nom du projet, dossier = celui-ci). Aucune configuration supplémentaire nécessaire.

## Mettre à jour le site plus tard

Toute modification se fait dans `index.html`. Une fois modifié :
```bash
git add index.html
git commit -m "Mise à jour du site"
git push
```
Vercel republie automatiquement à chaque `push` sur la branche `main` (si connecté via GitHub).

## Domaine personnalisé

Une fois déployé, dans Vercel : **Project → Settings → Domains** → ajouter votre nom de domaine (ex. `lacavendjamena.com`) et suivre les instructions DNS affichées.
