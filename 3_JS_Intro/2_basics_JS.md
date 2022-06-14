<!-- omit in toc -->
# Module 3 - Introduction JavaScript

<!-- omit in toc -->
## Table des matières

- [À propos de JavaScript ?](#à-propos-de-javascript-)
- [La balise ``<script>``](#la-balise-script)
- [Votre première fonction](#votre-première-fonction)
- [Les variables](#les-variables)
  - [La syntaxe](#la-syntaxe)
  - [Les types de variables](#les-types-de-variables)
    - [1. Chaine de caractères (string)](#1-chaine-de-caractères-string)

## À propos de JavaScript ?

Le Javascript ça sert à quoi? Il fut un temps où l'utilisation du JS se résumait à l'animation de certains composants web. De nos jours, la totalité d'un contenu web peut être codé en Javascript, autant du côté front-end que back-end, ce qui fait de lui un langage prédominant sur le marché, voir indispensable. Les standards ECMAscript reprennent les bonnes pratiques actuelles. Avec les années le langage s'enrichit et s'étoffe de nouvelles fonctionnalités, parfois utiles, parfois performantes, parfois non. Les standards ECMAscript sont là pour indiquer au développeur ce qui est recommandé d'utilisation.
<br>
Comme nous venons de l'aborder, le Javascript est donc à la base des plus gros frameworks et librairies actuelles. React.JS, Vue.JS, Angular, Node.JS, Express.JS, Typescript, chacun de ces langages est soit une réécriture de Javascript, soit une librairie de fonctions pré-écrite par les développeurs, soit un super-set (une version améliorée et boostée du langage officiel). Il est donc primordial de maîtriser la base pour être capable de travailler avec ces langages plus avancés.

## La balise ``<script>``

La balise script permet d'injecter du contenu Javascript dans votre page HTML ou de lier un fichier script à votre page. Tout comme l'attribut onclick nous préfèrerons lier un fichier script.js plutôt que d'insérer du code en javascript directement dans cette balise.
Pour rendre fonctionnel votre eventListener il faut insérer la balise script non pas dans les méta donnée mais après la fermeture de la balise body dans votre index.html:
```html
</body> 
<script src="script.js"></script> 
</html> 
```
Pourquoi? Car de cette façon le navigateur pourra d'abord charger l'ensemble des balises html avant de passer au fichier script, si l'ensemble des balises sont chargées alors la récupération de l'élément HTML au sein du fichier script est assurée, si ce n'était pas le cas vous pourriez obtenir un "undefined" à la place de pointer vers l'élément désiré. 

[:arrow_up: Revenir au top](#table-des-matières)

## Votre première fonction

Avant d'entrer dans le vif du sujet, vous aurez besoin de connaitre LA fonction qui sera votre meilleur atout durant la suite de la formation :
```js
console.log();
```
Cette fonction vous permettra d'afficher les données que vous souhaitez dans la console de votre navigateur. Pour accèder à cette console, cliquez droit sur votre page web et ouvrez l'inspecteur, dans la fenêtre qui vient de s'ouvrir en haut cliquez sur l'onglet "Console". L'inspecteur est un outil formidable qui vous sera d'une grande aide et vous serez amené à l'utiliser régulièrement. Il existe plusieurs façons d'afficher dans votre [console](https://developer.mozilla.org/fr/docs/Web/API/Console).

[:arrow_up: Revenir au top](#table-des-matières)

## Les variables

Une variable est un conteneur. Elle contient les informations dont nous avons besoin pour les fonctionnalités de notre application, notre site. Une variable c'est par exemple:
```js
const firstname = "Lucas";
```
``const`` (pour constante) détermine la portée de la variable, en l'occurence elle ne peut être réassignée à une nouvelle valeur car c'est une valeur constante, en effet, mon prénom est Lucas et sauf demande de ma part aux autorités communales, il en restera ainsi toute ma vie. 

``let`` défini une variable dont la valeur est réassignable, par exemple :
```js
let javascriptCoach = "Lucas";
```
Nous ne sommes à l'abri de rien, un évenement m'empêchant de donner cours pourrait avoir lieu, un remplaçant serait donc désigné, cette variable doit donc pouvoir être réassignable si besoin.

``var`` = Portée globale, fortement dépréciée.

``let`` = Portée limitée à celle du bloc courant. 

``const`` = Portée limitée à celle du bloc comme ``let`` mais n'est pas réassignable.

[:arrow_up: Revenir au top](#table-des-matières)

### La syntaxe

Nous savons du coup que ``let`` ou ``const`` désignent la portée de la variable.<br>
``firstname`` est le nom donné à ma variable.<br>
Un nom de variable est toujours unique.<br>
Un bon nom de variable est défini par la clareté de son utilité (il n'y a pas de doute possible quant à l'utilité de ma variable firstname, elle se réfère à un prénom).<br>
Un nom de variable débute toujours par une lettre minuscule, cependant si elle comporte plusieurs mots (tel que dans l'exemple "javascriptTeacher") la première lettre du second mot sera toujours écrite en majuscule. On appelle cette pratique le [*camelCase*](https://en.wikipedia.org/wiki/Camel_case) il s'agit ici d'un cas de bonne pratique, une sorte de convention en matière de rédaction de code Javascript.<br>
Le signe ``=`` en JavaScript ne signifie **pas** égal mais **assigne** une valeur à la variable.
``" "`` définit le type de la variable sur "string" qui signifie chaîne de caractère en français.<br>
Nous verrons dans le chapitre suivant les différents types de variables, il peut s'agir d'un nombre, d'un texte, d'un booléen (vrai ou faux), d'un tableau, etc... 
<br>
``;`` Le point virgule désigne la fin de la ligne, le navigateur comprend qu'il doit passer à la ligne suivante et continue la lecture du code. Si vous vous abstenez d'ajouter le point virgule il peut arriver des erreurs de lecture de votre navigateur. Il est donc indispensable de toujours l'ajouter quand vous passez à la ligne après avoir terminé une ligne de code.

[:arrow_up: Revenir au top](#table-des-matières)

### Les types de variables

Javascript est langage dit "typé", la bonne pratique veut que pour chaque nouvelle variable, nous "déclarions" son type. Par type on entend : est-ce-que ma variable est un nombre? Est-ce une chaîne de caractère? Est-ce un booléen (vrai ou faux)? Est-ce-que ma variable est un tableau? Ou un objet? Pour ce dernier, nous y reviendrons plus tard mais l'ensemble du langage est basé sur les objets, on dit de lui qu'il est orienté objet. Il s'agit d'une notion plus avancée que nous aborderons plus tard mais il est toujours utile de le mentionner. 

#### 1. Chaine de caractères (string)
Une chaîne de caractère représente un texte, elle peut contenir l'ensemble des caractères reconnu de votre clavier DONT des chiffres. Les chiffres seront ici interprêtés sous forme de caractère et ne pourront pas être utilisé comme une variable typée nombre, vous ne pourrez donc pas l'utiliser pour effectuer une opération. Pour définir une variable en tant que chaîne de caractère nous utilisons les guillements ``" "``. Retenez que ``"1"`` est une chaîne de caractère si j'additione la chaîne de caractère ``"2"``, je n'obtiendrai **pas** 3 mais bien ``"12"``. Cela n'est même pas une addition mais une **concaténation**, vous verrez souvent ce terme qui est important à connaitre.

Plusieurs exemples de chaînes de caractère :
```js
const firstname = "Lucas";
let age = "29 ans";
let job = "Web Coach en Sirius !";
```
Comme nous l'avons vu précédement ma variable est préfixée ``let`` ou ``const`` en fonction de sa portée, le choix du nom est le plus explicite possible (firstname), elle est assignée grâce au signe ``=`` déclarée de type chaîne de caractère grâce aux guillemets ``" "``, et pour terminé, comme à chaque fin de déclaration le ``;`` qui indique au navigateur de passer à la ligne suivante. 

Imaginons que je souhaite afficher les valeurs de ces variables dans ma console:
```js
console.log(firstname + "," + age + "," + job);
```
Le résultat affiché dans la console sera :
``Lucas, 29 ans, Web Coach en Sirius !``

Cette opération est une concaténation. Le ``+`` est l'opérateur qui permet aux chaînes de caractères de se suivrent. Si vous êtes attentifs vous aurez remarqué que j'ai ajouté des virgules entourées de guillements ``","`` sans ça le résultat serait "Lucas29 ansWeb Coach en Sirius !"

Plutôt que de concaténer, il est possible d'utiliser les "backticks" ``" ` "`` et d'insérer la/les variable(s) directement dans la phrase. Comme ceci :

```js
console.log(`Je m'appelle ${firstname}, j'ai ${age} et je suis ${job}`);
```
Nous obtiendrons dans notre console :
``Je m'appelle Lucas, j'ai 29 ans et je suis Web Coach en Sirius !``


[:arrow_up: Revenir au top](#table-des-matières)

[:rewind: Retour au sommaire du cours](./README.md#table-des-matières)

> Cours original: Julie Vanderbyse
>
> Modification: Lucas Ielli 