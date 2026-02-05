# Tutoriel : Développement Web Front-End

Bienvenue dans ce guide qui vous explique les bases du développement web front-end, de la création de pages HTML à l'utilisation de JavaScript pour rendre vos sites interactifs.

- [Tutoriel : Développement Web Front-End](#tutoriel--développement-web-front-end)
  - [Introduction : Qu'est-ce que le Front-End ?](#introduction--quest-ce-que-le-front-end-)
  - [Partie 1 : HTML — La structure de votre page](#partie-1--html--la-structure-de-votre-page)
    - [Qu'est-ce que le HTML ?](#quest-ce-que-le-html-)
    - [Structure de base d'un fichier HTML](#structure-de-base-dun-fichier-html)
    - [Les balises HTML essentielles](#les-balises-html-essentielles)
    - [Exemple complet](#exemple-complet)
  - [Partie 2 : CSS — Le style de votre page](#partie-2--css--le-style-de-votre-page)
  - [Partie 3 : JavaScript — L'interactivité de votre page](#partie-3--javascript--linteractivité-de-votre-page)
    - [Qu'est-ce que JavaScript ?](#quest-ce-que-javascript-)
    - [Lier JavaScript à HTML](#lier-javascript-à-html)
      - [1. JavaScript dans la balise `<script>` (dans le HTML)](#1-javascript-dans-la-balise-script-dans-le-html)
      - [2. JavaScript dans un fichier externe (recommandé)](#2-javascript-dans-un-fichier-externe-recommandé)
    - [Ordre de chargement important](#ordre-de-chargement-important)
    - [📌 Dans votre projet](#-dans-votre-projet)
  - [Partie 4 : JavaScript — Les bases du langage](#partie-4--javascript--les-bases-du-langage)
    - [Les variables](#les-variables)
      - [Déclaration de variables](#déclaration-de-variables)
      - [Types de données essentiels](#types-de-données-essentiels)
    - [Les structures conditionnelles (if/else)](#les-structures-conditionnelles-ifelse)
      - [Structure de base](#structure-de-base)
      - [Opérateurs de comparaison](#opérateurs-de-comparaison)
      - [Opérateurs logiques](#opérateurs-logiques)
      - [Exemples pratiques](#exemples-pratiques)
    - [Les fonctions](#les-fonctions)
      - [Déclaration de fonction classique](#déclaration-de-fonction-classique)
      - [Fonction avec paramètres](#fonction-avec-paramètres)
      - [Fonction avec valeur de retour](#fonction-avec-valeur-de-retour)
    - [📌 Dans votre projet](#-dans-votre-projet-1)
      - [Exemple concret du projet](#exemple-concret-du-projet)
  - [Partie 5 : Déboguer avec la console — Les bases](#partie-5--déboguer-avec-la-console--les-bases)
    - [Ouvrir les outils de développement](#ouvrir-les-outils-de-développement)
    - [Les onglets principaux](#les-onglets-principaux)
    - [Utiliser `console.log()` pour déboguer](#utiliser-consolelog-pour-déboguer)
      - [Syntaxe de base](#syntaxe-de-base)
      - [Afficher plusieurs valeurs](#afficher-plusieurs-valeurs)
    - [Inspecter les erreurs](#inspecter-les-erreurs)
    - [En résumé](#en-résumé)
  - [Partie 6 : Ressources pour aller plus loin](#partie-6--ressources-pour-aller-plus-loin)
  - [Conclusion](#conclusion)

---

## Introduction : Qu'est-ce que le Front-End ?

Le **développement front-end** concerne tout ce que l'utilisateur voit et avec lequel il interagit dans un navigateur web.

**Les trois piliers du front-end :**

| Technologie | Rôle | Analogie |
|-------------|------|----------|
| **HTML** | Structure et contenu | Le squelette d'une maison |
| **CSS** | Apparence et style | La décoration et la peinture |
| **JavaScript** | Interactivité et logique | L'électricité et la plomberie |

---

## Partie 1 : HTML — La structure de votre page

### Qu'est-ce que le HTML ?

**HTML** (HyperText Markup Language) est le langage qui définit la **structure** et le **contenu** de votre page web.

Dans votre projet, vous allez lancer votre page web en ouvrant le fichier `index.html` dans un navigateur (Edge, Chrome, Firefox, etc.). Ce fichier est écrit en HTML.

### Structure de base d'un fichier HTML

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ma première page</title>
</head>
<body>
  <h1>Bonjour le monde !</h1>
  <p>Ceci est ma première page web.</p>
</body>
</html>
```

**Explication des balises :**

- `<!DOCTYPE html>` : Indique au navigateur qu'il s'agit d'un document HTML5
- `<html>` : Balise racine qui contient tout le document
- `<head>` : Contient les métadonnées (titre, liens CSS, etc.)
- `<body>` : Contient le contenu visible de la page

### Les balises HTML essentielles

```html
<!-- Titres (h1 = plus important, h6 = moins important) -->
<h1>Titre principal</h1>
<h2>Sous-titre</h2>
<h3>Sous-sous-titre</h3>

<!-- Paragraphe -->
<p>Ceci est un paragraphe de texte.</p>

<!-- Lien -->
<a href="https://www.exemple.com">Cliquez ici</a>

<!-- Image -->
<img src="mon-image.jpg" alt="Description de l'image">

<!-- Bouton -->
<button>Cliquez-moi</button>

<!-- Zone de texte -->
<input type="text" placeholder="Entrez votre nom">

<!-- Division (conteneur) -->
<div>
  <p>Contenu regroupé dans une division</p>
</div>

<!-- Liste non ordonnée -->
<ul>
  <li>Élément 1</li>
  <li>Élément 2</li>
  <li>Élément 3</li>
</ul>
```
<!-- Liste ordonnée 
<ol>
  <li>Premier</li>
  <li>Deuxième</li>
  <li>Troisième</li>
</ol>
-->

### Exemple complet

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Mon Portfolio</title>
</head>
<body>
  <h1>Bienvenue sur mon site</h1>
  
  <h2>À propos de moi</h2>
  <p>Je m'appelle Alice et j'apprends le développement web.</p>
  
  <h2>Mes projets</h2>
  <ul>
    <li>Site personnel</li>
    <li>Galerie d'art interactive</li>
    <li>Application de to-do list</li>
  </ul>
  
  <button>Contactez-moi</button>
</body>
</html>
```

Vous pouvez copier ce code dans un fichier `.html` et l'ouvrir dans votre navigateur pour voir le résultat.

<!-- 
Si vous regardez le code source de la page index.html vous verrez beaucoup de `<div>` et d'autres balises similaires, voilà à quoi elles correspondent:
### Les conteneurs : `<div>` et balises sémantiques

#### La balise `<div>` — Conteneur générique

La balise `<div>` (division) est un **conteneur générique** qui permet de regrouper d'autres éléments HTML. Elle n'a pas de signification particulière, mais elle est très utile pour organiser et styliser votre page.
```html
<!-- Regrouper des éléments liés -->
<!-- 
<div class="carte-produit">
  <h3>Ordinateur portable</h3>
  <p>Prix : 899€</p>
  <button>Acheter</button>
</div>

<!-- Créer des sections de mise en page -->
<!-- 
<div class="conteneur-principal">
  <div class="colonne-gauche">
    <p>Menu</p>
  </div>
  <div class="colonne-droite">
    <p>Contenu</p>
  </div>
</div>
```

#### Les balises sémantiques HTML5 — Conteneurs avec signification

HTML5 introduit des balises qui ont la même fonction que `<div>` mais avec une **signification sémantique** (elles indiquent le type de contenu qu'elles contiennent).
```html
<!-- En-tête de la page -->
<!-- 
<header>
  <h1>Mon Site Web</h1>
  <nav>
    <a href="#accueil">Accueil</a>
    <a href="#apropos">À propos</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<!-- Barre de navigation -->
<!-- 
<nav>
  <ul>
    <li><a href="#accueil">Accueil</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- Contenu principal de la page -->
<!-- 
<main>
  <article>
    <h2>Mon premier article</h2>
    <p>Contenu de l'article...</p>
  </article>
</main>

<!-- Section thématique -->
<!-- 
<section>
  <h2>Nos services</h2>
  <p>Description des services...</p>
</section>

<!-- Contenu annexe (barre latérale) -->
<!-- 
<aside>
  <h3>Articles récents</h3>
  <ul>
    <li>Article 1</li>
    <li>Article 2</li>
  </ul>
</aside>

<!-- Pied de page -->
<!-- 
<footer>
  <p>&copy; 2024 Mon Site Web. Tous droits réservés.</p>
</footer>
```

#### Comparaison : `<div>` vs balises sémantiques

```html
<!-- ❌ AVEC DIV UNIQUEMENT (moins clair) -->
<!-- 
<div class="header">
  <div class="nav">...</div>
</div>
<div class="main">
  <div class="article">...</div>
</div>
<div class="footer">...</div>

<!-- ✅ AVEC BALISES SÉMANTIQUES (meilleur) -->
<!-- 
<header>
  <nav>...</nav>
</header>
<main>
  <article>...</article>
</main>
<footer>...</footer>
```

**Avantages des balises sémantiques :**
- ✅ **Lisibilité** : le code est plus facile à comprendre
- ✅ **Accessibilité** : aide les lecteurs d'écran pour personnes malvoyantes
- ✅ **SEO** : aide les moteurs de recherche à comprendre votre page
- ✅ **Maintenance** : structure plus claire pour vous et votre équipe

**Quand utiliser `<div>` ?**
- Quand vous avez besoin d'un conteneur purement pour la mise en page CSS
- Quand aucune balise sémantique ne correspond au contenu

#### Exemple complet de structure de page
```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Structure de page complète</title>
</head>
<body>
  <!-- En-tête du site -->
  <!-- 
  <header>
    <h1>Mon Blog</h1>
    <nav>
      <a href="#accueil">Accueil</a>
      <a href="#articles">Articles</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- Contenu principal -->
  <!-- 
  <main>
    <!-- Article 1 -->
<!-- 
    <article>
      <header>
        <h2>Titre de l'article</h2>
        <p>Publié le 15 janvier 2024</p>
      </header>
      <p>Contenu de l'article...</p>
      <footer>
        <p>Tags: HTML, CSS, JavaScript</p>
      </footer>
    </article>

    <!-- Section spéciale -->
<!-- 
    <section>
      <h2>À propos de moi</h2>
      <p>Je suis un développeur web passionné...</p>
    </section>
  </main>

  <!-- Barre latérale -->
<!-- 
  <aside>
    <h3>Articles populaires</h3>
    <ul>
      <li><a href="#">Introduction à HTML</a></li>
      <li><a href="#">CSS pour débutants</a></li>
    </ul>
  </aside>

  <!-- Pied de page -->
<!-- 
  <footer>
    <p>&copy; 2024 Mon Blog. Tous droits réservés.</p>
    <div class="reseaux-sociaux">
      <a href="#">Facebook</a>
      <a href="#">Twitter</a>
    </div>
  </footer>
</body>
</html>
```

**Note importante :** Vous pouvez imbriquer des `<div>` et des balises sémantiques autant que nécessaire pour organiser votre contenu !
--->
---

## Partie 2 : CSS — Le style de votre page

C'est le CSS qui rend votre page jolie et agréable à utiliser. Si vous êtes intéressé par le design web, le CSS est votre meilleur allié ! Mais dans notre projet, nous ne vous demanderons pas de changer l'apparence visuelle du site web donc nous n'allons pas présenter le CSS en détail. Sachez juste que si vous voyez dans le fichier HTML des liens vers des fichiers `.css`, c'est pour appliquer du style à la page.

Dans votre projet, le fichier `styles.css` contient déjà tous les styles nécessaires. Vous n'aurez pas besoin de le modifier, mais vous pouvez le consulter si vous êtes curieux de voir comment les éléments sont stylisés !

Passons maintenant à JavaScript, qui est **le cœur de votre projet**.

<!-- IGNORE - Vous pouvez sauter cette partie si vous le souhaitez. 
### Qu'est-ce que le CSS ?

**CSS** (Cascading Style Sheets) est le langage qui définit l'**apparence visuelle** de votre page (couleurs, tailles, positions, etc.).

### Trois façons d'ajouter du CSS

#### 1. CSS inline (dans la balise HTML)

```html
<p style="color: blue; font-size: 20px;">Texte bleu en 20px</p>
```

❌ **Déconseillé** : difficile à maintenir

#### 2. CSS dans la balise `<style>` (dans le `<head>`)

```html
<head>
  <style>
    p {
      color: blue;
      font-size: 20px;
    }
  </style>
</head>
```

⚠️ **Acceptable** pour de petits projets

#### 3. CSS dans un fichier externe (recommandé)

**index.html :**
```html
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```

**styles.css :**
```css
p {
  color: blue;
  font-size: 20px;
}
```

✅ **Recommandé** : séparation des préoccupations, code réutilisable

### Sélecteurs CSS de base

```css
/* Sélecteur de balise */
p {
  color: blue;
}

/* Sélecteur de classe */
.ma-classe {
  background-color: yellow;
}

/* Sélecteur d'ID */
#mon-id {
  font-weight: bold;
}

/* Sélecteur multiple */
h1, h2, h3 {
  font-family: Arial, sans-serif;
}

/* Sélecteur descendant */
div p {
  margin-left: 20px;
}
```
-->
<!--
**Utilisation dans HTML :**

```html
-->
<!-- Classe -->
<!--
<p class="ma-classe">Texte avec fond jaune</p>

<!-- ID -->
<!--
<p id="mon-id">Texte en gras</p>
-->
<!-- Plusieurs classes -->
<!--
<p class="ma-classe autre-classe">Texte avec plusieurs styles</p>
```

### Propriétés CSS courantes

```css
.exemple {
  /* Couleurs */
  color: red;                    /* Couleur du texte */
  background-color: lightblue;   /* Couleur de fond */
  
  /* Texte */
  font-size: 18px;               /* Taille du texte */
  font-weight: bold;             /* Épaisseur (normal, bold) */
  font-family: Arial, sans-serif;/* Police */
  text-align: center;            /* Alignement (left, center, right) */
  
  /* Espacement */
  margin: 20px;                  /* Marge extérieure */
  padding: 10px;                 /* Marge intérieure */
  
  /* Dimensions */
  width: 300px;                  /* Largeur */
  height: 200px;                 /* Hauteur */
  
  /* Bordures */
  border: 2px solid black;       /* Bordure */
  border-radius: 10px;           /* Coins arrondis */
}
```
-->

---

## Partie 3 : JavaScript — L'interactivité de votre page

### Qu'est-ce que JavaScript ?

**JavaScript** est le langage de programmation qui permet d'ajouter de l'**interactivité** à vos pages web (réagir aux clics, modifier le contenu, communiquer avec des serveurs, communiquer avec l'API chatgpt, etc.).

### Lier JavaScript à HTML

<!--
#### 1. JavaScript inline (dans la balise HTML)

```html
<button onclick="alert('Bonjour !')">Cliquez-moi</button>
```

❌ **Déconseillé** : mélange HTML et JavaScript
--->
#### 1. JavaScript dans la balise `<script>` (dans le HTML)

```html
<body>
  <button id="monBouton">Cliquez-moi</button>
  
  <script>
    document.getElementById('monBouton').onclick = function() {
      alert('Bonjour !');
    };
  </script>
</body>
```

⚠️ **Acceptable** pour de petits scripts

#### 2. JavaScript dans un fichier externe (recommandé)

**index.html :**

```html
<body>
  <button id="monBouton">Cliquez-moi</button>
  
  <!-- Fichier JS à la fin du body -->
  <script src="script.js"></script>
</body>
```

**script.js :**

```javascript
document.getElementById('monBouton').onclick = function() {
  alert('Bonjour !');
};
```

Ce petit code affichera une alerte "Bonjour !" lorsque l'utilisateur cliquera sur le bouton. Le code JavaScript est placé dans un fichier séparé `script.js` et lié à la page HTML via la balise `<script>`. Le bouton est créé dans le HTML avec un identifiant `monBouton`, ce qui permet au script de le sélectionner et d'ajouter un gestionnaire d'événement pour le clic.

✅ **Recommandé** : code organisé et réutilisable

### Ordre de chargement important

⚠️ **Le JavaScript doit être chargé APRÈS les éléments HTML qu'il manipule !**

```html
<!-- ❌ MAUVAIS : le bouton n'existe pas encore -->
<head>
  <script src="script.js"></script>
</head>
<body>
  <button id="monBouton">Cliquez-moi</button>
</body>

<!-- ✅ BON : le bouton existe déjà -->
<body>
  <button id="monBouton">Cliquez-moi</button>
  <script src="script.js"></script>
</body>
```

### 📌 Dans votre projet

Vous allez principalement travailler dans les fichiers JavaScript :

- `manip.js` — Gère les commandes prédéterminées
- `data.js` — Définit les scènes et les prompts
- `prompt.js` — Construit les prompts système

Tous ces fichiers sont déjà liés à `index.html` via des balises `<script>` à la fin du `<body>`.

---

## Partie 4 : JavaScript — Les bases du langage

### Les variables

#### Déclaration de variables

```javascript
// let : variable qui peut changer
let age = 25;
age = 26;  // OK

// const : variable qui ne peut PAS changer (constante)
const nom = "Alice";
// nom = "Bob";  // ❌ ERREUR !
```

**Règle d'or :** Utilisez `const` par défaut, `let` si la valeur doit changer.

#### Types de données essentiels

En JavaScript, les variables peuvent contenir différents types de valeurs :

```javascript
// Nombres
let age = 25;
let prix = 19.99;

// Texte (chaînes de caractères)
let nom = "Alice";
let message = 'Bonjour';

// Booléens (vrai/faux)
let estMajeur = true;
let estConnecte = false;

// Tableaux (listes)
let couleurs = ["rouge", "vert", "bleu"];

// Objets (données structurées)
let personne = {
  nom: "Alice",
  age: 25
};
```

**Astuce :** Vous pouvez toujours vérifier le type d'une variable avec `typeof` :

```javascript
console.log(typeof age);  // "number"
console.log(typeof nom);  // "string"
```

<!--
#### Types de données

```javascript
// Nombres (number)
let age = 25;
let prix = 19.99;

// Chaînes de caractères (string)
let nom = "Alice";
let message = 'Bonjour le monde';
let phrase = `J'ai ${age} ans`;  // Template literals (avec backticks)

// Booléens (boolean)
let estMajeur = true;
let estEtudiant = false;

// Tableaux (array)
let couleurs = ["rouge", "vert", "bleu"];
let nombres = [1, 2, 3, 4, 5];

// Objets (object)
let personne = {
  nom: "Alice",
  age: 25,
  ville: "Paris"
};

// Null et undefined
let valeurVide = null;
let nonDefini;  // undefined
```

#### Opérations sur les variables

```javascript
// Arithmétique
let a = 10;
let b = 3;

let somme = a + b;        // 13
let difference = a - b;   // 7
let produit = a * b;      // 30
let quotient = a / b;     // 3.333...
let reste = a % b;        // 1 (modulo)

// Incrémentation
let compteur = 0;
compteur++;      // compteur = 1
compteur += 5;   // compteur = 6
compteur--;      // compteur = 5

// Concaténation de chaînes
let prenom = "Alice";
let nom = "Dupont";
let nomComplet = prenom + " " + nom;  // "Alice Dupont"

// Template literals (recommandé)
let presentation = `Je m'appelle ${prenom} ${nom}`;
```
--->
### Les structures conditionnelles (if/else)

#### Structure de base

```javascript
let age = 18;

if (age >= 18) {
  console.log("Vous êtes majeur");
} else {
  console.log("Vous êtes mineur");
}
```

#### Opérateurs de comparaison

```javascript
let x = 10;

// Égalité
x == 10    // true  (égalité de valeur, éviter)
x === 10   // true  (égalité stricte, recommandé)
x === "10" // false (types différents)

// Inégalité
x != 5     // true
x !== "10" // true  (recommandé)

// Comparaisons
x > 5      // true  (supérieur)
x >= 10    // true  (supérieur ou égal)
x < 20     // true  (inférieur)
x <= 10    // true  (inférieur ou égal)
```

#### Opérateurs logiques

```javascript
let age = 25;
let permis = true;

// ET (&&) : toutes les conditions doivent être vraies
if (age >= 18 && permis) {
  console.log("Vous pouvez conduire");
}

// OU (||) : au moins une condition doit être vraie
if (age < 18 || !permis) {
  console.log("Vous ne pouvez pas conduire");
}

// NON (!) : inverse la condition
if (!permis) {
  console.log("Vous n'avez pas le permis");
}
```

#### Exemples pratiques

```javascript
// If / else if / else
let note = 15;

if (note >= 16) {
  console.log("Très bien");
} else if (note >= 14) {
  console.log("Bien");
} else if (note >= 12) {
  console.log("Assez bien");
} else if (note >= 10) {
  console.log("Passable");
} else {
  console.log("Insuffisant");
}

// Conditions imbriquées
let age = 20;
let nationalite = "française";

if (age >= 18) {
  if (nationalite === "française") {
    console.log("Vous pouvez voter en France");
  } else {
    console.log("Vous êtes majeur mais pas français");
  }
} else {
  console.log("Vous êtes mineur");
}

// Opérateur ternaire (condition courte)
let statut = age >= 18 ? "majeur" : "mineur";
console.log(statut);  // "majeur"
```

### Les fonctions

#### Déclaration de fonction classique

```javascript
// Fonction sans paramètre ni retour
function direBonjour() {
  console.log("Bonjour !");
}

// Appel de la fonction
direBonjour();  // Affiche "Bonjour !"
```

#### Fonction avec paramètres

```javascript
function direBonjour(nom) {
  console.log("Bonjour " + nom + " !");
}

direBonjour("Alice");  // "Bonjour Alice !"
direBonjour("Bob");    // "Bonjour Bob !"

// Plusieurs paramètres
function addition(a, b) {
  let resultat = a + b;
  console.log(resultat);
}

addition(5, 3);  // 8
```

#### Fonction avec valeur de retour

```javascript
function addition(a, b) {
  return a + b;
}

let resultat = addition(5, 3);
console.log(resultat);  // 8

// Utilisation directe
console.log(addition(10, 20));  // 30

// Exemple plus complexe
function estMajeur(age) {
  if (age >= 18) {
    return true;
  } else {
    return false;
  }
}

// Version simplifiée
function estMajeur(age) {
  return age >= 18;
}

if (estMajeur(20)) {
  console.log("Accès autorisé");
}
```
<!--
#### Fonctions fléchées (arrow functions)

```javascript
// Syntaxe classique
function addition(a, b) {
  return a + b;
}

// Syntaxe fléchée (moderne)
const addition = (a, b) => {
  return a + b;
};

// Version ultra-courte (return implicite)
const addition = (a, b) => a + b;

// Un seul paramètre (pas besoin de parenthèses)
const carre = x => x * x;

console.log(carre(5));  // 25
```

#### Portée des variables (scope)

```javascript
// Variable globale (accessible partout)
let compteur = 0;

function incrementer() {
  // Variable locale (seulement dans la fonction)
  let message = "Incrémentation...";
  compteur++;
  console.log(message);
}

incrementer();
console.log(compteur);  // 1
// console.log(message); // ❌ ERREUR : message n'existe pas ici

// Paramètres = variables locales
function afficher(texte) {
  console.log(texte);  // OK
}

afficher("Bonjour");
// console.log(texte);  // ❌ ERREUR : texte n'existe pas ici
```

---

## Partie 5 : Interaction HTML ↔ JavaScript

### Sélectionner des éléments HTML

```javascript
// Par ID (retourne UN élément)
let titre = document.getElementById("monTitre");

// Par classe (retourne une LISTE d'éléments)
let paragraphes = document.getElementsByClassName("texte");

// Par balise (retourne une LISTE d'éléments)
let tousLesTitres = document.getElementsByTagName("h2");

// Sélecteur CSS (retourne le PREMIER élément trouvé)
let bouton = document.querySelector("#monBouton");
let premierParagraphe = document.querySelector(".texte");

// Sélecteur CSS (retourne TOUS les éléments trouvés)
let tousLesBoutons = document.querySelectorAll("button");
```

**HTML correspondant :**
```html
<h1 id="monTitre">Titre principal</h1>
<p class="texte">Premier paragraphe</p>
<p class="texte">Deuxième paragraphe</p>
<button id="monBouton">Cliquez-moi</button>
```

### Modifier le contenu d'un élément

```javascript
// Modifier le texte
let titre = document.getElementById("monTitre");
titre.textContent = "Nouveau titre";

// Modifier le HTML (avec balises)
titre.innerHTML = "Nouveau <strong>titre</strong>";

// Lire le contenu
let contenu = titre.textContent;
console.log(contenu);
```

### Modifier les styles CSS

```javascript
let titre = document.getElementById("monTitre");

// Modifier une propriété CSS
titre.style.color = "red";
titre.style.fontSize = "32px";
titre.style.backgroundColor = "yellow";

// Ajouter/retirer une classe CSS
titre.classList.add("important");
titre.classList.remove("petit");
titre.classList.toggle("cache");  // Ajoute si absent, retire si présent

// Vérifier si une classe existe
if (titre.classList.contains("important")) {
  console.log("Le titre est important");
}
```

### Écouter les événements

```javascript
// Clic sur un bouton
let bouton = document.getElementById("monBouton");

bouton.addEventListener("click", function() {
  console.log("Bouton cliqué !");
});

// Version avec fonction fléchée
bouton.addEventListener("click", () => {
  console.log("Bouton cliqué !");
});

// Version avec fonction nommée
function gererClic() {
  console.log("Bouton cliqué !");
}
bouton.addEventListener("click", gererClic);

// Autres événements courants
let input = document.getElementById("monInput");

// Changement de valeur
input.addEventListener("input", () => {
  console.log("Valeur : " + input.value);
});

// Touche pressée
input.addEventListener("keypress", (event) => {
  console.log("Touche : " + event.key);
});

// Souris entre dans l'élément
bouton.addEventListener("mouseenter", () => {
  console.log("Souris sur le bouton");
});
```

### Exemple complet : Compteur interactif

**HTML :**
```html
<div>
  <h1 id="compteur">0</h1>
  <button id="incrementer">+1</button>
  <button id="decrementer">-1</button>
  <button id="reset">Reset</button>
</div>
```

**JavaScript :**
```javascript
// Récupérer les éléments
let affichage = document.getElementById("compteur");
let btnPlus = document.getElementById("incrementer");
let btnMoins = document.getElementById("decrementer");
let btnReset = document.getElementById("reset");

// Variable pour stocker la valeur
let valeur = 0;

// Fonction pour mettre à jour l'affichage
function actualiser() {
  affichage.textContent = valeur;
  
  // Changer la couleur selon la valeur
  if (valeur > 0) {
    affichage.style.color = "green";
  } else if (valeur < 0) {
    affichage.style.color = "red";
  } else {
    affichage.style.color = "black";
  }
}

// Événements
btnPlus.addEventListener("click", () => {
  valeur++;
  actualiser();
});

btnMoins.addEventListener("click", () => {
  valeur--;
  actualiser();
});

btnReset.addEventListener("click", () => {
  valeur = 0;
  actualiser();
});
```
--->

### 📌 Dans votre projet

Vous utiliserez souvent :
- **Variables** : `userName`, `scenes`, `chatHistory`
- **Conditions** : pour gérer les commandes dans `manip.js`
- **Fonctions** : `beforeAI()`, `buildSystemPromptForScene()`, etc.
  
#### Exemple concret du projet

Voici une fonction simple qu'on pourrait ajouter dans `manip.js` :

```javascript
// Fonction pour vérifier si l'utilisateur est un adulte
function estAdulte(age) {
  return age >= 18;
}

// Utilisation dans beforeAI
if (userText === "age") {
  if (estAdulte(promptVars.age)) {
    msg = "Tu es adulte, bienvenue !";
  } else {
    msg = "Tu es mineur, contenu adapté.";
  }
  addMessageToUI("assistant", msg);
  laisseAIdecider = false;
}
```

Ce type de fonction vous permet de **réutiliser** la même logique à plusieurs endroits.

---

## Partie 5 : Déboguer avec la console — Les bases

### Ouvrir les outils de développement

**Raccourcis clavier :**
- **Windows/Linux** : `F12` ou `Ctrl + Shift + I`
- **Mac** : `Cmd + Option + I`

**Ou via le menu :**
- Chrome : Menu (⋮) → Plus d'outils → Outils de développement
- Firefox : Menu (☰) → Développement web → Outils de développement

### Les onglets principaux

| Onglet | Utilité |
|--------|---------|
| **Elements** (ou Inspecteur) | Voir et modifier le HTML et CSS en temps réel |
| **Console** | Voir les logs, erreurs, et exécuter du JavaScript |
| **Sources** (ou Débogueur) | Déboguer le code JavaScript ligne par ligne |
| **Network** (ou Réseau) | Voir les requêtes réseau (images, API, etc.) |

### Utiliser `console.log()` pour déboguer

#### Syntaxe de base

```javascript
// Afficher un message simple
console.log("Début du script");

// Afficher une variable
let age = 25;
console.log(age);

// Afficher avec un label
console.log("L'âge est :", age);
```

#### Afficher plusieurs valeurs

```javascript
let nom = "Alice";
let age = 25;
let ville = "Paris";

// Plusieurs valeurs séparées par des virgules
console.log("Nom:", nom, "Age:", age, "Ville:", ville);

// Avec template literal (plus lisible)
console.log(`Nom: ${nom}, Age: ${age}, Ville: ${ville}`);
```
<!--
#### Afficher des objets

```javascript
let personne = {
  nom: "Alice",
  age: 25,
  ville: "Paris"
};

// Affichage simple
console.log(personne);

// Affichage sous forme de tableau (plus lisible)
console.table(personne);

// Affichage détaillé
console.dir(personne);
```

### Autres commandes de console utiles

```javascript
// Avertissement (jaune)
console.warn("Attention : valeur inhabituelle");

// Erreur (rouge)
console.error("Erreur : impossible de charger les données");

// Information (bleu)
console.info("Information : chargement terminé");

// Nettoyer la console
console.clear();

// Grouper des logs
console.group("Détails de l'utilisateur");
console.log("Nom: Alice");
console.log("Age: 25");
console.groupEnd();

// Mesurer le temps d'exécution
console.time("Calcul");
// ... code à mesurer ...
console.timeEnd("Calcul");  // Affiche le temps écoulé
```

### Déboguer avec des breakpoints

**Méthode 1 : Dans le code**

```javascript
let resultat = 0;

for (let i = 0; i < 10; i++) {
  debugger;  // Le code s'arrête ici
  resultat += i;
}

console.log(resultat);
```

**Méthode 2 : Dans les outils (recommandé)**

1. Ouvrez l'onglet **Sources** (ou Débogueur)
2. Trouvez votre fichier JavaScript
3. Cliquez sur un numéro de ligne pour ajouter un breakpoint (point rouge)
4. Rechargez la page
5. Le code s'arrête au breakpoint
6. Utilisez les boutons pour :
   - ▶️ Continuer
   - ⤵️ Step Over (ligne suivante)
   - ⬇️ Step Into (entrer dans une fonction)
   - ⬆️ Step Out (sortir d'une fonction)
--->
### Inspecter les erreurs

Quand une erreur se produit, la console affiche :

```
Uncaught ReferenceError: maVariable is not defined
    at script.js:15
```

**Informations fournies :**
- **Type d'erreur** : `ReferenceError`
- **Message** : `maVariable is not defined`
- **Fichier et ligne** : `script.js:15`

**Cliquez sur le lien** pour aller directement à la ligne problématique !

### En résumé

Pour déboguer efficacement votre code :
1. **Ouvrez la console** avec F12
2. **Utilisez `console.log()`** pour afficher des valeurs
3. **Lisez les messages d'erreur** pour trouver les bugs
4. **Testez régulièrement** votre code au fur et à mesure

💡 **Astuce :** Prenez l'habitude d'ouvrir la console dès que vous travaillez sur votre projet !
<!--
### Astuces de débogage

```javascript
// 1. Vérifier qu'un élément existe
let bouton = document.getElementById("monBouton");
console.log("Bouton trouvé ?", bouton);  // null si pas trouvé

if (!bouton) {
  console.error("Erreur : bouton non trouvé !");
}

// 2. Vérifier le type d'une variable
let age = "25";  // Oups, c'est une chaîne !
console.log("Type de age :", typeof age);  // "string"

// 3. Afficher les étapes d'une fonction
function calculer(a, b) {
  console.log("Entrée dans calculer avec a =", a, "et b =", b);
  
  let resultat = a + b;
  console.log("Résultat calculé :", resultat);
  
  return resultat;
}

// 4. Vérifier les conditions
if (age >= 18) {
  console.log("✓ Condition vraie : age >= 18");
} else {
  console.log("✗ Condition fausse : age < 18");
}

// 5. Logger au bon endroit
bouton.addEventListener("click", () => {
  console.log("🖱️ Clic détecté sur le bouton");
  // ... reste du code
});
```
-->
<!--
---

## Partie 7 : Projet complet — Mettre tout ensemble

### Objectif

Créer une **liste de tâches** (to-do list) avec :

- Ajout de tâches
- Suppression de tâches
- Marquage des tâches comme complétées

### Structure du projet

```
mon-projet/
│
├── index.html
├── styles.css
└── script.js
```

### index.html

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ma To-Do List</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="container">
    <h1>Ma Liste de Tâches</h1>
    
    <div class="input-section">
      <input type="text" id="taskInput" placeholder="Nouvelle tâche...">
      <button id="addButton">Ajouter</button>
    </div>
    
    <ul id="taskList"></ul>
  </div>
  
  <script src="script.js"></script>
</body>
</html>
```

### styles.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  background-color: #f5f5f5;
  padding: 20px;
}

.container {
  max-width: 600px;
  margin: 0 auto;
  background: white;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

h1 {
  color: #333;
  margin-bottom: 20px;
  text-align: center;
}

.input-section {
  display: flex;
  gap: 10px;
  margin-bottom: 20px;
}

#taskInput {
  flex: 1;
  padding: 10px;
  border: 2px solid #ddd;
  border-radius: 5px;
  font-size: 16px;
}

#taskInput:focus {
  outline: none;
  border-color: #4CAF50;
}

button {
  padding: 10px 20px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 16px;
}

button:hover {
  background-color: #45a049;
}

#taskList {
  list-style: none;
}

.task-item {
  display: flex;
  align-items: center;
  padding: 15px;
  background: #f9f9f9;
  margin-bottom: 10px;
  border-radius: 5px;
  transition: background 0.3s;
}

.task-item:hover {
  background: #f0f0f0;
}

.task-item.completed {
  opacity: 0.6;
}

.task-item.completed .task-text {
  text-decoration: line-through;
  color: #888;
}

.task-checkbox {
  margin-right: 15px;
  cursor: pointer;
  width: 20px;
  height: 20px;
}

.task-text {
  flex: 1;
  font-size: 16px;
  color: #333;
}

.delete-button {
  background-color: #f44336;
  padding: 5px 15px;
  font-size: 14px;
}

.delete-button:hover {
  background-color: #da190b;
}
```

### script.js

```javascript
// Récupérer les éléments
const taskInput = document.getElementById('taskInput');
const addButton = document.getElementById('addButton');
const taskList = document.getElementById('taskList');

// Tableau pour stocker les tâches
let tasks = [];

// Fonction pour ajouter une tâche
function addTask() {
  // Récupérer et nettoyer le texte
  const taskText = taskInput.value.trim();
  
  // Vérifier que le champ n'est pas vide
  if (taskText === '') {
    alert('Veuillez entrer une tâche !');
    return;
  }
  
  console.log('Ajout de la tâche :', taskText);
  
  // Créer un objet tâche
  const task = {
    id: Date.now(),  // ID unique basé sur le timestamp
    text: taskText,
    completed: false
  };
  
  // Ajouter au tableau
  tasks.push(task);
  
  // Vider le champ
  taskInput.value = '';
  
  // Rafraîchir l'affichage
  renderTasks();
}

// Fonction pour supprimer une tâche
function deleteTask(id) {
  console.log('Suppression de la tâche avec ID :', id);
  
  // Filtrer pour garder toutes les tâches sauf celle à supprimer
  tasks = tasks.filter(task => task.id !== id);
  
  // Rafraîchir l'affichage
  renderTasks();
}

// Fonction pour basculer le statut d'une tâche
function toggleTask(id) {
  console.log('Toggle de la tâche avec ID :', id);
  
  // Trouver la tâche et inverser son statut
  const task = tasks.find(task => task.id === id);
  if (task) {
    task.completed = !task.completed;
  }
  
  // Rafraîchir l'affichage
  renderTasks();
}

// Fonction pour afficher toutes les tâches
function renderTasks() {
  console.log('Rendu de', tasks.length, 'tâche(s)');
  
  // Vider la liste
  taskList.innerHTML = '';
  
  // Créer un élément pour chaque tâche
  tasks.forEach(task => {
    // Créer l'élément <li>
    const li = document.createElement('li');
    li.className = 'task-item';
    
    // Ajouter la classe 'completed' si la tâche est terminée
    if (task.completed) {
      li.classList.add('completed');
    }
    
    // Créer la checkbox
    const checkbox = document.createElement('input');
    checkbox.type = 'checkbox';
    checkbox.className = 'task-checkbox';
    checkbox.checked = task.completed;
    checkbox.addEventListener('change', () => toggleTask(task.id));
    
    // Créer le texte
    const span = document.createElement('span');
    span.className = 'task-text';
    span.textContent = task.text;
    
    // Créer le bouton supprimer
    const deleteBtn = document.createElement('button');
    deleteBtn.className = 'delete-button';
    deleteBtn.textContent = 'Supprimer';
    deleteBtn.addEventListener('click', () => deleteTask(task.id));
    
    // Assembler les éléments
    li.appendChild(checkbox);
    li.appendChild(span);
    li.appendChild(deleteBtn);
    
    // Ajouter à la liste
    taskList.appendChild(li);
  });
}

// Événements
addButton.addEventListener('click', addTask);

// Permettre d'ajouter avec la touche Entrée
taskInput.addEventListener('keypress', (event) => {
  if (event.key === 'Enter') {
    addTask();
  }
});

// Initialisation
console.log('Application to-do list chargée');
renderTasks();
```

### Tester le projet

1. Ouvrez `index.html` dans votre navigateur
2. Ouvrez la console (F12)
3. Ajoutez des tâches
4. Cochez/décochez des tâches
5. Supprimez des tâches
6. Observez les logs dans la console

---

## Partie 8 : Bonnes pratiques

### Organisation des fichiers

```
mon-projet/
│
├── index.html              # Point d'entrée
├── css/
│   ├── styles.css         # Styles principaux
│   └── responsive.css     # Styles responsive
├── js/
│   ├── main.js           # Code principal
│   └── utils.js          # Fonctions utilitaires
└── assets/
    └── images/           # Images
```

### Nommage

**Variables et fonctions :**
```javascript
// ✅ BON : camelCase
let monNomDeVariable = "valeur";
function faireQuelqueChose() { }

// ❌ MAUVAIS
let MaVariable = "valeur";       // PascalCase (réservé aux classes)
let mon_nom_de_variable = "val"; // snake_case (pas en JavaScript)
```

**Classes CSS :**
```css
/* ✅ BON : kebab-case */
.ma-classe-css { }
.bouton-principal { }

/* ❌ MAUVAIS */
.maClasseCss { }    /* camelCase */
.Ma_Classe { }      /* mélange */
```

**ID HTML :**
```html
<!-- ✅ BON -->
<!--
<div id="mon-conteneur"></div>
<button id="bouton-ajouter"></button>
--->
<!-- ❌ MAUVAIS -->
<!--
<div id="MonConteneur"></div>
```

### Code propre

```javascript
// ✅ BON : indenté, espacé, commenté
function calculerTotal(prix, quantite) {
  // Calculer le sous-total
  const sousTotal = prix * quantite;
  
  // Appliquer la TVA (20%)
  const tva = sousTotal * 0.2;
  
  // Retourner le total
  return sousTotal + tva;
}

// ❌ MAUVAIS : tout collé, illisible
function calculerTotal(prix,quantite){const sousTotal=prix*quantite;const tva=sousTotal*0.2;return sousTotal+tva;}
```

### Débogage

```javascript
// ✅ BON : logs descriptifs
console.log('=== Début du chargement ===');
console.log('Nombre de tâches :', tasks.length);
console.log('Utilisateur connecté :', userName);

// ❌ MAUVAIS : logs inutiles
console.log('test');
console.log(1);
console.log('aaaaa');
```
--->
---

## Partie 6 : Ressources pour aller plus loin

**Documentation officielle :**

- [MDN Web Docs](https://developer.mozilla.org/fr/) — La référence pour HTML, CSS, JavaScript
- [W3Schools](https://www.w3schools.com/) — Tutoriels et exemples pratiques

**Apprendre JavaScript :**

- [JavaScript.info](https://javascript.info/) — Cours complet et moderne
- [Eloquent JavaScript](https://eloquentjavascript.net/) — Livre gratuit en ligne

**Pratiquer :**

- [freeCodeCamp](https://www.freecodecamp.org/) — Exercices interactifs gratuits
- [Codecademy](https://www.codecademy.com/) — Cours interactifs

**Outils utiles :**

- [CodePen](https://codepen.io/) — Tester du code HTML/CSS/JS en ligne
- [JSFiddle](https://jsfiddle.net/) — Idem
- [Visual Studio Code](https://code.visualstudio.com/) — Éditeur de code recommandé

---
<!--
## Conclusion

Vous avez maintenant les bases du développement web front-end !

**Ce que vous savez faire :**
- ✅ Créer la structure d'une page avec HTML
- ✅ Styliser une page avec CSS
- ✅ Ajouter de l'interactivité avec JavaScript
- ✅ Manipuler le DOM (Document Object Model)
- ✅ Déboguer votre code avec F12 et la console
- ✅ Créer un projet complet fonctionnel

**Prochaines étapes :**
1. **Pratiquez** : créez vos propres projets
2. **Explorez** : découvrez les frameworks (React, Vue, etc.)
3. **Approfondissez** : apprenez ES6+, async/await, APIs
4. **Partagez** : mettez vos projets en ligne (GitHub Pages, Netlify)
--->

## Conclusion

Vous avez maintenant les connaissances de base pour comprendre et modifier votre projet de galerie interactive !

**Ce que vous maîtrisez :**
- ✅ La structure HTML de base
- ✅ Le rôle du JavaScript dans l'interactivité
- ✅ Les variables, conditions et fonctions
- ✅ L'utilisation de la console pour déboguer

**Pour votre projet spécifique :**
1. **Commencez par lire** le code existant pour comprendre la structure
2. **Utilisez `console.log()`** pour voir ce qui se passe
3. **Testez vos modifications** une par une
4. **Consultez ce tutoriel** quand vous avez un doute

**N'oubliez pas :** Chaque développeur, même expérimenté, consulte régulièrement la documentation et fait des erreurs. C'est normal et ça fait partie de l'apprentissage !

**Bon développement ! 🚀**


