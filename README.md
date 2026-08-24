# zigeStore PWA

## Mise en ligne sur GitHub Pages (5 minutes)

### Étape 1 — Créer le repo
1. Va sur github.com → New repository
2. Nom : `zigestore`
3. Coche "Public"
4. Clique "Create repository"

### Étape 2 — Upload les fichiers
1. Clique "uploading an existing file"
2. Glisse tous les fichiers du dossier (index.html, apps.json, manifest.json, sw.js)
3. Commit changes

### Étape 3 — Activer GitHub Pages
1. Settings → Pages
2. Source : Deploy from a branch → main → / (root)
3. Save

Ton store sera dispo sur : https://TON_USERNAME.github.io/zigestore

### Étape 4 — Installer sur les téléphones
1. Ouvre le lien sur Chrome Android
2. Un bandeau "Installer" apparaît automatiquement
3. Tape Installer → l'app apparaît sur l'écran d'accueil

---

## Ajouter une app

Édite `apps.json` et ajoute :
```json
{
  "name": "Nom de l'app",
  "description": "Description courte",
  "version": "v1.0.0",
  "category": "Médias",
  "apkUrl": "apks/nomapp.apk",
  "iconEmoji": "🎵",
  "sizeMb": 10.0,
  "featured": false
}
```

Puis upload l'APK dans le dossier `apks/` du repo.

Catégories : Médias · Utilitaires · Système · Confidentialité
