## Fondamentaux du CSS

### Vue d'ensemble
Le CSS (Cascading Style Sheets, ou Feuilles de Style en Cascade) est utilisé pour styliser le HTML.

Le CSS fonctionne en :

- sélectionnant un élément HTML
- choisissant une propriété à modifier
- appliquant une certaine valeur

### Syntaxe
```css
element-selector {
  une-propriété-de-style: valeur;
  une-autre-propriété-de-style: valeur;
}
```

Une propriété + valeur est connue sous le nom de « déclaration », comme ici : `text-align: center;`

En général, et pour des raisons de lisibilité, nous avons tendance à mettre chaque déclaration sur des lignes séparées, comme dans l'exemple ci-dessus. Certains argumentent qu'il est préférable de tout mettre (élément, propriété et valeur) sur une seule ligne (quand il n’y a qu’une seule déclaration), mais il est possible que vous ayez besoin d'ajouter d'autres déclarations à l'avenir. Placer chaque déclaration sur des lignes dédiées rend également le code beaucoup plus facile à lire et à suivre.

### Appliquer le CSS au HTML
Il existe plusieurs façons d'appliquer du CSS à un projet HTML. Voyons-les en revue.

#### Feuille de style externe
Une feuille de style externe contient du CSS dans un fichier séparé avec une extension `.css`. C’est la méthode la plus courante pour ajouter du CSS à un document. Vous pouvez également lier un seul fichier CSS à plusieurs pages web, en stylisant toutes ces pages avec la même feuille de style CSS.

Exemple d’un fichier de feuille de style externe lié à un document HTML :

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Adding Styles</title>
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <h1>Hello CSS!</h1>
  </body>
</html>
```

Le fichier externe pourrait ressembler à ceci :

```css
h1 {
  color: deepskyblue;
  text-align: center;
}
```

#### Feuille de style interne
Une feuille de style interne se trouve dans un document HTML. Pour créer une feuille de style interne, placez simplement le code CSS dans un élément `<style>` contenu dans l’élément `<head>` du HTML.

Exemple d'une feuille de style interne dans un document HTML :

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Adding Styles</title>
    <style>
      h1 {
        color: deepskyblue;
        text-align: center;
      }
    </style>
  </head>
  <body>
    <h1>Hello CSS!</h1>
  </body>
</html>
```

#### Styles en ligne
Les styles en ligne sont des déclarations CSS qui affectent un seul élément HTML, contenues dans un attribut `style`.

Exemple de style en ligne dans un document HTML :

```html
<h1 style="color: deepskyblue; text-align: center;">Hello CSS!</h1>
```

**Remarque :** Les styles en ligne prennent le pas sur les feuilles de style, donc un style en ligne prévaudra toujours sur tout autre.

### CSS invalide
Vous vous demandez peut-être ce qui se passe si un navigateur rencontre un sélecteur CSS ou une déclaration qu'il ne reconnaît pas ?

Si un navigateur analyse vos règles et rencontre une propriété ou une valeur qu'il ne comprend pas, il l'ignore et passe à la déclaration suivante. Cela se produit si vous avez mal orthographié une propriété ou une valeur, ou si la propriété ou la valeur est trop récente et que le navigateur ne la prend pas encore en charge. De même, si un navigateur rencontre un sélecteur qu'il ne comprend pas, il ignorera la règle entière et passera à la suivante.

Pour cette raison, il est conseillé de valider votre CSS. De cette manière, vous saurez immédiatement si quelque chose ne va pas.

**Astuce :** Les outils de développement d’un navigateur peuvent également mettre en évidence les noms de propriétés ou valeurs invalides.

> Inspection d’un élément de titre avec une valeur invalide en utilisant les Outils de Développement de Google Chrome.

### Ressources
[Premiers pas avec le CSS - Apprendre le développement web | MDN](https://developer.mozilla.org/fr/docs/Learn/CSS/First_steps)

--- 

N'hésitez pas si vous avez besoin d'autres informations ou d'exemples spécifiques !
