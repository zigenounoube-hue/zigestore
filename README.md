# ⚡ zigeStore

> Store APK privé pour la famille. Design cyberpunk violet.

---

## Mise en ligne (5 min)

### 1. Créer le repo GitHub
- Va sur [github.com](https://github.com) → **New repository**
- Nom : `zigestore` · Public · Create

### 2. Upload les fichiers
- Clique **"uploading an existing file"**
- Glisse tous les fichiers du zip → **Commit changes**

### 3. Activer GitHub Pages
- **Settings** → **Pages** → Source : `main` → `/ (root)` → **Save**
- Ton store sera dispo sur : `https://TON_USERNAME.github.io/zigestore`

### 4. Installer sur les téléphones
- Ouvre le lien dans **Chrome Android**
- Tape le bandeau **"Installer"** → l'app s'ajoute à l'écran d'accueil

---

## Ajouter une app

Édite `apps.json` et ajoute un objet :

```json
{
  "id": "mon-app",
  "name": "Mon App",
  "developer": "Développeur",
  "description": "Description courte affichée sur la carte.",
  "longDescription": "Description complète visible dans la page info.",
  "version": "v1.0.0",
  "category": "Médias",
  "apkUrl": "apks/mon-app.apk",
  "externalUrl": "https://github.com/user/repo/releases/latest",
  "website": "https://monsite.com",
  "iconEmoji": "🎵",
  "iconBg": "#1a0f2a",
  "sizeMb": 10.0,
  "featured": false,
  "available": true,
  "addedDate": "2025-01-15",
  "changelog": "• Nouveauté 1\n• Correctif 2",
  "permissions": ["Internet", "Stockage"],
  "screenshots": [
    "https://lien-vers-screenshot-1.png",
    "https://lien-vers-screenshot-2.png"
  ]
}
```

Puis upload l'APK dans le dossier `apks/` du repo.

---

## Champs `apps.json`

| Champ | Type | Description |
|---|---|---|
| `id` | string | Identifiant unique (pas d'espaces) |
| `name` | string | Nom affiché |
| `developer` | string | Nom du développeur |
| `description` | string | Description courte (carte) |
| `longDescription` | string | Description longue (page info) |
| `version` | string | Ex: `v1.2.3` |
| `category` | string | `Médias` · `Utilitaires` · `Système` · `Confidentialité` |
| `apkUrl` | string | Chemin vers l'APK dans `apks/` |
| `externalUrl` | string | Lien GitHub/F-Droid si pas d'APK local |
| `website` | string | Site officiel de l'app |
| `iconEmoji` | string | Emoji affiché comme icône |
| `iconBg` | string | Couleur de fond de l'icône (hex) |
| `sizeMb` | number | Taille en MB |
| `featured` | boolean | Affiché en section "En vedette" |
| `available` | boolean | `true` = APK dispo · `false` = lien externe |
| `addedDate` | string | Date d'ajout `YYYY-MM-DD` |
| `changelog` | string | Notes de version (supporte `\n`) |
| `permissions` | array | Liste des permissions requises |
| `screenshots` | array | URLs des captures d'écran |

---

## Structure du repo

```
zigestore/
├── index.html        ← L'app entière
├── apps.json         ← Liste des apps (édite ici)
├── manifest.json     ← Config PWA
├── sw.js             ← Service worker (offline)
├── apks/             ← Tes fichiers APK
│   ├── newpipe.apk
│   └── ...
└── README.md
```

---

## Fonctionnalités

- ⚡ Design cyberpunk violet
- 🔍 Recherche en temps réel
- 🗂️ Filtres par catégorie
- ⇅ Tri (A→Z, taille, date)
- ℹ️ Page info complète par app (screenshots, changelog, permissions)
- ⬇️ Historique des téléchargements
- 🔗 Partage du store et des apps
- 📲 Guide d'installation APK intégré
- 📦 Installable comme une vraie app (PWA)
- 🔄 Pull to refresh

---

Made with 💜 by Ayoub
