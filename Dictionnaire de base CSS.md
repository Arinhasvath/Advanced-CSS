# DICTIONNAIRE CSS DÉTAILLÉ

## 1. SÉLECTEURS FONDAMENTAUX

```css
/* Types de sélecteurs */
element         /* Sélecteur de balise (ex: p, div) */
.classe         /* Sélecteur de classe */
#id            /* Sélecteur d'identifiant */
element.classe  /* Élément avec classe spécifique */
element > enfant /* Enfant direct */
element + adjacent /* Élément adjacent suivant */
[attribute]     /* Sélecteur d'attribut */

/* Exemples concrets */
p { }               /* Tous les paragraphes */
.header { }         /* Éléments avec classe header */
#unique { }         /* Élément avec ID unique */
div.special { }     /* Divs avec classe special */
ul > li { }         /* Li directs dans ul */
h1 + p { }          /* P suivant directement h1 */
[type="text"] { }   /* Éléments avec attribut type="text" */
```

## 2. BOX MODEL & DIMENSIONS

```css
/* Box Model */
width: 100px;              /* Largeur */
height: 100px;             /* Hauteur */
max-width: 800px;          /* Largeur maximale */
min-height: 400px;         /* Hauteur minimale */

/* Marges */
margin: 10px;              /* Marge sur tous les côtés */
margin: 10px 20px;         /* Haut/Bas Gauche/Droite */
margin: 10px 20px 15px 25px; /* Haut Droite Bas Gauche */
margin-top: 10px;          /* Marge haute uniquement */

/* Padding (rembourrage) */
padding: 10px;             /* Padding sur tous les côtés */
padding: 10px 20px;        /* Haut/Bas Gauche/Droite */
padding-left: 15px;        /* Padding gauche uniquement */

/* Bordures */
border: 1px solid black;   /* Épaisseur Style Couleur */
border-radius: 5px;        /* Coins arrondis */
border-top: 2px dashed red; /* Border spécifique */

/* Box-sizing */
box-sizing: border-box;    /* Inclut padding et border dans width/height */
```

## 3. POSITIONNEMENT & LAYOUT

```css
/* Position */
position: static;          /* Par défaut */
position: relative;        /* Relatif à sa position normale */
position: absolute;        /* Par rapport au parent positionné */
position: fixed;           /* Fixe par rapport à la fenêtre */
position: sticky;          /* Hybride entre relative et fixed */

/* Coordonnées */
top: 0;                   /* Distance du haut */
right: 10px;              /* Distance de la droite */
bottom: 20px;             /* Distance du bas */
left: 15px;               /* Distance de la gauche */
z-index: 100;             /* Ordre d'empilement */

/* Display */
display: block;           /* Élément bloc */
display: inline;          /* Élément en ligne */
display: inline-block;    /* Hybride inline et block */
display: none;            /* Cache l'élément */

/* Flexbox (Conteneur) */
display: flex;            /* Active flexbox */
flex-direction: row;      /* Direction des éléments */
justify-content: center;  /* Alignement horizontal */
align-items: center;      /* Alignement vertical */
flex-wrap: wrap;          /* Retour à la ligne */
gap: 10px;               /* Espace entre les éléments */

/* Flexbox (Éléments) */
flex: 1;                 /* Croissance proportionnelle */
flex-grow: 1;            /* Facteur de croissance */
flex-shrink: 0;          /* Facteur de rétrécissement */
flex-basis: auto;        /* Taille de base */
```

## 4. TYPOGRAPHIE & TEXTE

```css
/* Police */
font-family: Arial, sans-serif; /* Famille de police */
font-size: 16px;               /* Taille de police */
font-weight: bold;             /* Graisse (400=normal, 700=bold) */
font-style: italic;            /* Style de police */
line-height: 1.5;             /* Hauteur de ligne */

/* Texte */
text-align: center;           /* Alignement du texte */
text-decoration: underline;   /* Décoration (soulignement, etc.) */
text-transform: uppercase;    /* Transformation du texte */
letter-spacing: 2px;         /* Espacement des lettres */
word-spacing: 4px;           /* Espacement des mots */
white-space: nowrap;         /* Gestion des espaces blancs */
```

## 5. COULEURS & ARRIÈRE-PLAN

```css
/* Couleurs */
color: #ff0000;              /* Couleur hexadécimale */
color: rgb(255, 0, 0);       /* Couleur RGB */
color: rgba(255, 0, 0, 0.5); /* RGB avec transparence */
color: hsl(0, 100%, 50%);    /* Couleur HSL */
opacity: 0.8;                /* Transparence globale */

/* Arrière-plan */
background-color: #fff;      /* Couleur de fond */
background-image: url('image.jpg'); /* Image de fond */
background-repeat: no-repeat; /* Répétition du fond */
background-position: center;  /* Position du fond */
background-size: cover;      /* Taille du fond */
```
# PROPRIÉTÉS CSS AVANCÉES

## 6. TRANSITIONS & ANIMATIONS

```css
/* Transitions de base */
transition: all 0.3s ease;    /* Propriété Durée Timing */
transition-property: color;    /* Propriété spécifique */
transition-duration: 0.5s;     /* Durée */
transition-timing-function: ease-in-out; /* Fonction de timing */
transition-delay: 0.1s;        /* Délai avant début */

/* Exemple pratique de transition */
.button {
    background: blue;
    transition: all 0.3s ease;
}
.button:hover {
    background: darkblue;     /* Transitionne en hover */
}

/* Animations */
@keyframes monAnimation {
    0% { transform: scale(1); }     /* État initial */
    50% { transform: scale(1.2); }  /* État milieu */
    100% { transform: scale(1); }   /* État final */
}

.element-anime {
    animation: monAnimation 2s infinite; /* Nom Durée Répétition */
}
```

## 7. TRANSFORMATIONS

```css
/* Types de transformations */
transform: translate(50px, 20px);  /* Déplacement X,Y */
transform: scale(1.5);            /* Agrandissement */
transform: rotate(45deg);         /* Rotation */
transform: skew(10deg);           /* Inclinaison */

/* Combinaisons */
transform: scale(1.2) rotate(45deg); /* Multiple transforms */

/* Point d'origine */
transform-origin: center;         /* Point de référence */
```

## 8. MEDIA QUERIES

```css
/* Points de rupture standard */
@media screen and (max-width: 768px) {
    /* Styles pour tablettes */
}

@media screen and (max-width: 480px) {
    /* Styles pour mobiles */
}

/* Orientation */
@media (orientation: landscape) {
    /* Styles en mode paysage */
}

/* Combinaisons */
@media screen and (min-width: 768px) and (max-width: 1024px) {
    /* Styles pour une plage spécifique */
}
```

## 9. PROPRIÉTÉS MODERNES

```css
/* Variables CSS (Custom Properties) */
:root {
    --couleur-primaire: #007bff;
    --espacement-base: 1rem;
}

.element {
    color: var(--couleur-primaire);
    margin: var(--espacement-base);
}

/* Filtres */
filter: blur(5px);              /* Flou */
filter: brightness(150%);       /* Luminosité */
filter: contrast(200%);         /* Contraste */
filter: grayscale(100%);        /* Niveaux de gris */

/* Ombres */
box-shadow: 0 2px 4px rgba(0,0,0,0.2);  /* Ombre de boîte */
text-shadow: 1px 1px 2px black;         /* Ombre de texte */

/* Dégradés */
background: linear-gradient(to right, #ff0000, #00ff00);
background: radial-gradient(circle, #ff0000, #00ff00);
```

## 10. ACCESSIBILITÉ & ÉTATS

```css
/* États de focus */
:focus {
    outline: 2px solid blue;
    outline-offset: 2px;
}

/* États d'interaction */
:hover  { /* Au survol */ }
:active { /* Au clic */ }
:focus  { /* Au focus */ }
:visited { /* Lien visité */ }

/* Sélecteurs d'attributs avancés */
[aria-hidden="true"] { display: none; }
[data-type~="special"] { /* Attributs personnalisés */ }
```
