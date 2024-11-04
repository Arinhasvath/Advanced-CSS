# Fondamentaux CSS

## Aperçu

Les CSS (Feuilles de Style en Cascade) sont utilisées pour styliser le HTML.

Le CSS fonctionne en :

1. Sélectionnant un élément HTML
2. Choisissant une propriété à modifier
3. Appliquant une certaine valeur

## Syntaxe

```css
selecteur-element {
    propriete-de-style-1: valeur;
    propriete-de-style-2: valeur;
}
```

Une propriété + valeur est appelée une "déclaration". Par exemple : `text-align: center;`

En général, pour des raisons de lisibilité, nous avons tendance à mettre chaque déclaration sur des lignes séparées comme dans l'exemple ci-dessus. Certains soutiennent qu'il est préférable de tout mettre (élément, propriété et valeur) sur une seule ligne (lorsqu'il n'y a qu'une seule déclaration), mais vous pourriez avoir besoin d'ajouter plus de déclarations à l'avenir. De plus, placer chaque déclaration sur des lignes dédiées rend le code beaucoup plus facile à lire et à suivre.

## Application du CSS au HTML

Il existe plusieurs façons d'appliquer du CSS à un projet HTML. Passons-les en revue.

### Feuille de style externe

Une feuille de style externe contient du CSS dans un fichier séparé avec une extension .css. C'est la méthode la plus couramment utilisée pour ajouter du CSS à un document. Vous pouvez également lier un seul fichier CSS à plusieurs pages web, les stylisant toutes avec la même feuille de style CSS.

Exemple d'un fichier de feuille de style externe lié au HTML :

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Ajout de Styles</title>
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <h1>Bonjour CSS !</h1>
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

### Feuille de style interne

Une feuille de style interne réside dans un document HTML. Pour créer une feuille de style interne, il suffit de placer le code CSS à l'intérieur d'un élément `<style>` contenu dans l'élément `<head>` du HTML.

Exemple d'une feuille de style interne liée au HTML :

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Ajout de Styles</title>
  <style>
    h1 {
      color: deepskyblue;
      text-align: center;
    }
  </style>
</head>
<body>
  <h1>Bonjour CSS !</h1>
</body>
</html>
```

### Styles en ligne

Les styles en ligne sont des déclarations CSS qui affectent un seul élément HTML, contenues dans un attribut style.

Exemple d'un style en ligne dans un document HTML :

```html
<h1 style="color: deepskyblue; text-align: center;">Bonjour CSS !</h1>
```

**Note** : Les styles en ligne ont priorité sur les feuilles de style, donc un style en ligne prévaudra toujours sur tout autre.

## CSS invalide

Vous vous demandez peut-être ce qui se passe si un navigateur rencontre un sélecteur ou une déclaration CSS qu'il ne reconnaît pas ?

Si un navigateur analyse vos règles et rencontre une propriété ou une valeur qu'il ne comprend pas, il l'ignore et passe à la déclaration suivante. Il fera cela si vous avez mal tapé/mal orthographié une propriété ou une valeur, ou si la propriété ou la valeur est trop nouvelle et que le navigateur ne la prend pas encore en charge. De même, si un navigateur rencontre un sélecteur qu'il ne comprend pas, il ignorera simplement toute la règle et passera à la suivante.

Pour cette raison, il est judicieux de valider votre CSS. Ainsi, vous saurez immédiatement si quelque chose ne va pas.

**Astuce** : Les outils de développement d'un navigateur peuvent également mettre en évidence les noms de propriétés ou les valeurs invalides.

## Ressources

[CSS first steps - Learn web development | MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps)

Citations:
[1] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/29334386/616ee405-6a45-45c3-87ce-f8cb31b499a5/paste.txt
[2] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/29334386/de2c6f8a-5372-4950-98e9-36f0c61974b9/paste.txt
[3] https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/29334386/09c7772c-1f1d-4805-8038-d0d82f43fb6a/paste-2.txt
