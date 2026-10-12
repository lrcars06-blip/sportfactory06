# Sport Factory Menton — site vitrine

Site statique de la salle de sport Sport Factory, 8 rue Isola, 06500 Menton.
Aucune dépendance, aucune étape de build : tous les fichiers sont à la racine.

## Contenu

| Fichier | Rôle |
|---|---|
| `index.html` | Page d'accueil complète, 6 langues (FR, EN, RU, UK, ZH, AR), intro animée |
| `mentions-legales.html` | Mentions légales (LCEN, Code de commerce) |
| `politique-de-confidentialite.html` | Politique de confidentialité (RGPD) |
| `politique-des-cookies.html` | Politique des cookies (CNIL) |
| `404.html` | Page d'erreur |
| `*.webp`, `logo.png`, `og-image.jpg` | Images |
| `*.woff2` | Polices hébergées localement (licence SIL OFL 1.1) |
| `favicon.ico`, `apple-touch-icon.png`, `icon-*.png`, `site.webmanifest` | Icônes |
| `robots.txt`, `sitemap.xml` | Référencement |
| `vercel.json` | Redirections des anciennes URL WordPress, cache, en-têtes de sécurité |

## Mise en ligne : GitHub → Vercel

1. Créer un dépôt sur GitHub (privé ou public), y déposer tous les fichiers de ce dossier à la racine.
   - Sans ligne de commande : sur la page du dépôt, **Add file → Upload files**, glisser tous les fichiers, **Commit changes**.
   - En ligne de commande :
     ```
     git init
     git add .
     git commit -m "Site Sport Factory Menton"
     git branch -M main
     git remote add origin https://github.com/<compte>/sport-factory-menton.git
     git push -u origin main
     ```
2. Sur https://vercel.com/new, **Import** le dépôt. Framework Preset : **Other**. Root Directory : `./`. **Deploy**.
3. Chaque modification poussée sur `main` est mise en ligne automatiquement.

## Nom de domaine (IONOS)

1. Vercel → projet → **Settings → Domains** : ajouter `sportfactorymenton.fr` et `www.sportfactorymenton.fr`.
2. IONOS → zone DNS du domaine :
   - **A** `@` → `76.76.21.21`
   - **CNAME** `www` → `cname.vercel-dns.com`
   - ne pas toucher aux enregistrements **MX** (messagerie)
3. Propagation : quelques minutes à 24 h. HTTPS automatique.

## Modifier le site

- Textes français : dans `index.html`.
- Traductions : bloc `var T = {...}` en bas de `index.html`.
- Photos : remplacer les fichiers en gardant les mêmes noms.
- Tarifs et horaires : présents à plusieurs endroits (bandeau, tarifs, FAQ, contact, pied de page, données structurées). Chercher la valeur avec Ctrl+F.

## Tarifs en ligne

Sans engagement 49 € / mois · 3 mois 130 € · 12 mois 30 € / mois (360 € l'an). Prix TTC.
