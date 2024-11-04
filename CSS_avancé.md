# CSS avancé

## Tag vs Classe vs ID (Sélecteurs)

Les développeurs utilisent de moins en moins d'IDs dans leurs CSS. La raison en est que les IDs doivent toujours être uniques sur une page. Pour une flexibilité maximale, l’utilisation de classes uniquement simplifie la réutilisation des éléments de l’interface utilisateur (UI).

### Cascade ou ordre

```css
* { } /* sélectionne tous les éléments */
section /* sélectionne toutes les balises section */
.my-class { } /* sélectionne tous les éléments ayant cette classe */
.my-block > .my-title { }
.my-block + .my-title { }
.my-block ~ .my-title { }
#my-div /* sélectionne l’élément avec cet ID */
```

## Couleurs

La propriété `color` en CSS définit la couleur du texte dans un élément HTML.

Les couleurs en CSS sont généralement représentées par des noms, des valeurs hexadécimales ou des valeurs RGB.

### Conseil d'accessibilité
Lorsque vous choisissez des couleurs pour votre design, il est toujours conseillé de prendre en compte l'accessibilité. Les navigateurs modernes permettent désormais de vérifier facilement si une couleur est accessible ou non.

### Exemple de code
```css
p { color: red; }
p { color: #f00; }
p { color: #ff0000; }
p { color: rgb(255,0,0); }
p { color: rgb(100%, 0%, 0%); }
p { color: hsl(0, 100%, 50%); }
```

### Ressources
- [color - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/color)
- Liste des couleurs
- Colors - A nicer color palette for the web
- Color Names — HTML Color Codes
- Noms de couleur CSS

---

## Variables CSS

Les propriétés personnalisées ou variables CSS représentent des valeurs pouvant être réutilisées dans plusieurs déclarations.

### Exemple de code
```css
:root {
  --main-bg-color: blue;
}
body {
  color: var(--main-bg-color);
}
```

### Ressources
- [var() - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/var)
- [Custom properties (–*): CSS variables - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/--*)

---

## Unités et valeurs

Différentes unités CSS peuvent être utilisées. `px` est l’une des plus utilisées, et il s’agit d’une unité absolue, contrairement aux unités relatives comme `rem`.

Les unités absolues et relatives sont utilisées dans des contextes différents.

- `rem` : taille de la police, remplissage, marge
- `em` : requêtes de média

### Attention !
`REM` est relatif à l’élément racine (`<html>`), pas à `<body>`.

### Exemple de code
```css
font-size: 2rem;
padding: 1.2rem 2rem;
```

### Ressources
- [CSS values and units - Learn web development | MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units)

---

## Interligne (`line-height`)

La propriété `line-height` définit la hauteur entre les lignes de texte.

### Conseil d'accessibilité
Utilisez un minimum de 1,5 pour l’interligne dans le contenu principal. Cela aidera les personnes ayant des troubles visuels à lire plus facilement.

### Exemple de code
```css
p {
    line-height: 1;
}
```

---

## Décoration de texte (`text-decoration`)

La propriété abrégée `text-decoration` définit l'apparence des lignes décoratives sur le texte.

### Exemple de code
```css
a {
  text-decoration: line-through;
}
```

---

## Alignement du texte (`text-align`)

La propriété `text-align` détermine l’alignement horizontal d’un élément de type BLOCK.

### Ressources
- [text-align - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)

---

## Transformation de texte (`text-transform`)

La propriété `text-transform` permet de capitaliser un texte.

### Exemple de code
```css
p {
  text-transform: lowercase;
}
```

---

## Espacement des lettres (`letter-spacing`)

La propriété `letter-spacing` détermine l’espacement entre les caractères.

### Exemple de code
```css
a {
  letter-spacing: -0.4rem;
}
```

---

## Pseudo-classes

Une pseudo-classe CSS est un mot-clé ajouté à un sélecteur pour spécifier un état différent de l’élément.

```css
selector:pseudo-class {
  property: value;
}
```

### Exemple de code
```css
a:link {
  color: green;
}
a:visited {
  color: cadetblue;
}
a:hover {
  text-decoration: underline;
}
a:active {
  color: darkcyan;
}
```

### Ressources
- [Pseudo-classes - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

---

## Réinitialisation/Normalisation CSS

L’expression `CSS reset` vient d'Eric Meyer, qui a créé une feuille de style de réinitialisation en 2007 pour réduire les incohérences entre navigateurs.

### Ressources
- CSS Tools: Reset CSS
- Normalize CSS ou CSS Reset?! - Elad Shechter - Medium

---

## Box Model

Le box model est une base essentielle à comprendre pour créer des mises en page et aligner les éléments sur la page.

### Exemple de code
```css
.box {
  box-sizing: content-box;
}
.box {
  box-sizing: border-box;
}
.box-dimensions {
  width: 100px;
  height: 50px;
  padding-top: 30px;
  margin: 5px;
}
```

### Ressources
- [Introduction to the CSS basic box model - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)

---

## Flux et affichage CSS

Le flux normal, ou Flow Layout, est la façon dont les éléments Block et Inline sont affichés sur une page avant tout changement de mise en page.

---

## Système de grille

Les systèmes de grille sont utilisés pour organiser le contenu des sites web. Avant `flexbox` et `css grid`, les systèmes de grille utilisaient des `floats`.

### Ressources
- [Floats Tutorial | HTML & CSS Is Hard](https://internetingishard.com/html-and-css/floats/)

---

## Pseudo-éléments

Un pseudo-élément CSS permet de styliser une partie spécifique d’un élément.

### Exemple de code
```css
a::after {
  content: '→';
}
p::first-letter {
  font-size: 130%;
}
```

---

## Sélecteurs d'attributs

Les sélecteurs d'attributs vous permettent de cibler un attribut présent sur un élément HTML.

### Exemple de code
```css
a[href*="facebook"] {
  color: #3C5A99;
}
a[href^="#"] {
  background-color: gold;
}
a[href$=".org"] {
  color: red;
}
```

---

## Fond

```css
.box {
  background: ;
}
```

---

## Bordures

La propriété abrégée `border` définit la bordure d’un élément.

### Exemple de code
```css
.box {
  display: block;
  padding: 1rem;
  border-width: 2px;
  border-style: double;
  border-color: orange;
  border-radius: 12px;
}
```

---

## Positionnement

Le positionnement en CSS utilise plusieurs propriétés permettant de positionner les éléments sur une page HTML.

### Exemple de code
```css
.component {
  position: sticky;
  top: 0;
}
```

---

## Transformation CSS

Les propriétés de transformation CSS permettent de faire pivoter, agrandir, déformer ou déplacer un élément.

### Exemple de code
```css
transform: perspective(17px);
transform: rotate3d(1, 2.0, 3.0, 10deg);
transform: translate(12px, 50%);
transform: scale(2, 0.5);
transform: skew(30deg, 20deg);
```

---

## Animation CSS

Les propriétés d'animation en CSS permettent d'animer d'autres propriétés d'un élément.

### Exemple de code
```css
@keyframes example {
  from {
    background-color: blue;
  }
  to {
    background-color: red;
  }
}
.box {
  width: 10rem;
  height: 10rem;
  background-color: blue;
  animation-name: example;
  animation-duration: 3s;
}
```

---

