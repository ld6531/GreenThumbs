# Green Thumb — Deploy sur Netlify via GitHub

## Structure
```
index.html                  ← l'app
netlify.toml                ← config Netlify
netlify/functions/claude.js ← proxy API serverless
```

## Déploiement (5 min)

### 1. Crée un repo GitHub
- Va sur github.com → New repository → nom : `green-thumb`
- Upload ces 3 fichiers/dossiers :
  - `index.html`
  - `netlify.toml`
  - `netlify/functions/claude.js`

### 2. Connecte Netlify à GitHub
- netlify.com → Add new site → Import from Git → GitHub
- Sélectionne le repo `green-thumb`
- Build settings : laisse tout vide (le netlify.toml gère)
- Clique Deploy

### 3. Ajoute ta clé API
- Site settings → Environment variables → Add variable
- Key : `ANTHROPIC_API_KEY`
- Value : `sk-ant-xxxxxxxxxxxx`

### 4. Redéploie
- Deploys → Trigger deploy → Deploy site

C'est tout ✅
