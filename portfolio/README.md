# portfolio

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

---

## Présentation du Portfolio

Ce projet est un portfolio personnel conçu pour présenter mes compétences en développement web, mes projets professionnels et personnels, ainsi que mon parcours. Il a été développé avec Vue.js, et il intègre plusieurs sections dynamiques et interactives.

### Objectifs du projet
Le but principal de ce portfolio est de :
- **Présenter mes compétences** : Vous trouverez une section dédiée à mes compétences techniques, en développement front-end et back-end.
- **Mettre en valeur mes projets** : Une section de création dynamique affiche les projets sur lesquels j'ai travaillé, avec des informations détaillées sur chaque projet.
- **Permettre une interaction avec les visiteurs** : Un formulaire de contact intégré permet aux utilisateurs de m'envoyer des messages directement depuis le site.

### Fonctionnalités principales

1. **Section Présentation** :
   - Introduction de moi-même avec une brève description, une photo, et un lien vers mes réseaux sociaux.
   - Tout est centré pour donner une mise en page professionnelle et élégante.

2. **Section Compétences** :
   - Liste de mes compétences techniques avec des icônes associées.
   - Utilisation de **CSS** pour un effet de survol (hover) sur les compétences, mettant en évidence chaque compétence individuellement.

3. **Section Expérience** :
   - Description de mes expériences professionnelles avec une mise en page en colonnes : **Compétences** à gauche et **Expérience** à droite.
   - Séparation claire des sections avec des effets visuels au survol pour donner un aspect interactif.

4. **Créations (Portfolio)** :
   - Utilisation de modals dynamiques pour présenter mes projets avec des détails comme le nom du projet, une brève description, les technologies utilisées, et des captures d'écran.
   - Les modals sont alignés horizontalement avec un affichage fluide, inspiré du flux Instagram déjà mis en place.

5. **Formulaire de contact** :
   - Intégré avec **EmailJS** pour permettre aux visiteurs de m'envoyer des e-mails directement via le formulaire de contact. Ce formulaire inclut les champs de base : nom, e-mail, sujet et message.
   - Confirmation d'envoi après soumission réussie.

### Technologies utilisées

- **Vue.js** : Utilisé pour la structure de l'application et pour rendre l'interface dynamique et réactive.
- **Vue Router** : Pour gérer la navigation entre les différentes sections du portfolio.
- **CSS (ou SCSS)** : Pour la mise en page, les animations et les transitions.
- **EmailJS** : Pour l'envoi des e-mails via le formulaire de contact sans backend.
- **ESLint** : Pour assurer que le code suive les bonnes pratiques et éviter les erreurs courantes de syntaxe.
- **HTML5** et **JavaScript** : Pour la structure de base et l'interactivité.
  
### Structure du projet

Voici un aperçu de la structure des fichiers dans ce projet :

```plaintext
├── public
│   ├── index.html        # Fichier principal de la page HTML
├── src
│   ├── assets/           # Images, icônes, et autres ressources statiques
│   ├── components/       # Composants Vue.js, incluant le Header, Footer, etc.
│   ├── views/            # Vues principales (sections) du portfolio
│   ├── router/           # Configuration du routeur Vue.js
│   ├── App.vue           # Composant racine de l'application
│   ├── main.js           # Point d'entrée de l'application Vue.js
└── README.md             # Documentation du projet
