# Tableau de Bord Financier

Une PWA (Progressive Web App) pour suivre votre portefeuille d'investissement et votre budget.

## 📱 Installation sur iPhone et Mac

### Sur iPhone :
1. Ouvrez la page dans Safari
2. Appuyez sur le bouton de partage (carré avec flèche)
3. Sélectionnez "Sur l'écran d'accueil"
4. Confirmez

### Sur Mac :
1. Ouvrez la page dans Chrome ou Safari
2. Appuyez sur le bouton "Installer l'app" (ou menu → "Installer l'app")
3. Confirmez

## 🚀 Déploiement sur GitHub Pages

### Étape 1 : Créer un repository GitHub
1. Allez sur [github.com/new](https://github.com/new)
2. Nommez-le `budget-app` (ou le nom que vous voulez)
3. Créez le repository

### Étape 2 : Télécharger vos fichiers
1. Clonez le repo :
```bash
cd /tmp
git clone https://github.com/VOTRE_USERNAME/budget-app.git
cd budget-app
```

2. Copiez ces fichiers du dossier `Claude - Cowork` :
   - `dashboard.html`
   - `manifest.json`
   - `sw.js`

3. Renommez `dashboard.html` en `index.html`

4. Créez un fichier `.gitignore` :
```
node_modules/
.DS_Store
*.log
```

### Étape 3 : Pusher sur GitHub
```bash
git add .
git commit -m "Initial commit: Budget app"
git push origin main
```

### Étape 4 : Activer GitHub Pages
1. Allez sur votre repo GitHub
2. Settings → Pages
3. Sous "Source", sélectionnez "Deploy from a branch"
4. Sélectionnez "main" et "/root"
5. Cliquez "Save"

### Étape 5 : Accéder à votre app
L'app sera disponible à : `https://VOTRE_USERNAME.github.io/budget-app/`

Attendez 1-2 minutes pour que GitHub Pages déploie.

## ⚙️ Fonctionnalités

- 📊 Suivi du budget mensuel
- 📈 Portefeuille d'investissements (PEA)
- 💰 Analyse des dépenses
- 🔄 Récupération automatique des cours de bourse
- 📱 Fonctionne hors-ligne (mode PWA)
- 🎨 Interface responsive (Mobile, Tablet, Desktop)

## 🔗 Google Apps Script

Le dashboard utilise un Google Apps Script pour récupérer les cours de bourse via Yahoo Finance.

L'URL du script est définie dans le code :
```javascript
const GAS_URL = 'https://script.google.com/macros/s/YOUR_SCRIPT_ID/exec';
```

## 📝 Notes

- Vos données sont stockées localement dans le navigateur (localStorage)
- Les données ne sont pas synchronisées entre appareils
- Vous pouvez exporter/importer vos données manuellement si besoin
