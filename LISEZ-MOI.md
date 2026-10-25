# La course de Gabriel : mettre l'appli en ligne

Ce dossier contient tout le jeu. Une fois en ligne, Gabriel peut l'installer sur son
téléphone comme une vraie appli : icône, plein écran, et jeu possible sans internet.

## Contenu du dossier

| Fichier | Rôle |
|---|---|
| `index.html` | Le jeu |
| `manifest.webmanifest` | Nom, icône et plein écran de l'appli |
| `sw.js` | Garde le jeu en mémoire pour jouer sans internet |
| `icons/` | Les icônes de l'appli |

## Option A : GitHub Pages (gratuit)

1. Connectez-vous sur https://github.com et cliquez sur **New** (nouveau dépôt).
2. Nom du dépôt : par exemple `course-de-gabriel`. Choisissez **Public**, puis **Create repository**.
   Avec un compte gratuit, GitHub Pages ne marche qu'avec un dépôt public.
3. Sur la page du dépôt, cliquez sur **uploading an existing file** (ou **Add file → Upload files**).
4. Faites glisser **le contenu** de ce dossier : `index.html`, `manifest.webmanifest`, `sw.js`
   et le dossier `icons`. Ne glissez pas le dossier `appli-gabriel` lui-même :
   `index.html` doit se trouver à la racine du dépôt.
5. Cliquez sur **Commit changes**.
6. Allez dans **Settings → Pages**. Sous « Build and deployment », choisissez
   **Deploy from a branch**, branche **main**, dossier **/ (root)**, puis **Save**.
7. Après une ou deux minutes, le lien apparaît en haut de cette page, par exemple :
   `https://votre-pseudo.github.io/course-de-gabriel/`

## Option B : Netlify Drop

1. Allez sur https://app.netlify.com/drop.
2. Faites glisser **ce dossier entier** dans la page.
3. Créez un compte gratuit quand Netlify le demande, sinon le site disparaît au bout d'une heure.

## Installer le jeu sur le téléphone de Gabriel

Ouvrez le lien une première fois **avec internet**, puis :

- **iPhone** : ouvrez le lien dans **Safari**, touchez le bouton Partager ⬆️,
  puis **Sur l'écran d'accueil**.
- **Android** : ouvrez le lien dans **Chrome**, menu ⋮, puis **Installer l'application**
  (ou **Ajouter à l'écran d'accueil**).

L'icône de Gabriel à la casquette rouge apparaît. Après avoir lancé le jeu une fois,
on peut y jouer même en mode avion.

## Mettre le jeu à jour

1. Remplacez `index.html` par la nouvelle version.
2. Dans `sw.js`, changez le numéro de version : `gabriel-v1` devient `gabriel-v2`, etc.
3. Renvoyez les fichiers modifiés sur GitHub (ou glissez à nouveau le dossier sur Netlify).

Le téléphone récupère la nouvelle version la prochaine fois que le jeu s'ouvre avec internet.
Les pièces, les achats et le record sont gardés.
