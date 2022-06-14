<!-- omit in toc -->
# Module 3 - Introduction JavaScript

<!-- omit in toc -->
## Table des matières

- [À propos de JavaScript ?](#à-propos-de-javascript-)
- [La balise ``<script>``](#la-balise-script)
- [Les variables](#les-variables)
  - [La syntaxe :](#la-syntaxe-)

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

### La syntaxe :

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

[:rewind: Retour au sommaire du cours](./README.md#table-des-matières)

> Cours original: Julie Vanderbyse
>
> Modification: Lucas Ielli
 