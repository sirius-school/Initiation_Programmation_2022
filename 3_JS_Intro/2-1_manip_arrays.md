<!-- omit in toc -->
# Manipulation de tableaux (arrays)

Avant de vous lancer dans les exercices nous allons apprendre comment manipuler vos données contenues dans un tableau.
<!-- omit in toc -->
## Tables des matières
- [Boucler dans un tableau](#boucler-dans-un-tableau)
- [Ajouter une donnée](#ajouter-une-donnée)
- [Supprimer la dernière donnée](#supprimer-la-dernière-donnée)
- [Supprimer le première donnée](#supprimer-le-première-donnée)
- [Ajouter une donnée à l'indice 0](#ajouter-une-donnée-à-lindice-0)
- [Supprimer une donnée grâce à son indice[]](#supprimer-une-donnée-grâce-à-son-indice)
- [Copier un tableau](#copier-un-tableau)
- [Petite précision !](#petite-précision-)
<!-- omit in toc -->
## Opérations de tableaux (arrays operations)

### Boucler dans un tableau

La boucle ``.foreach()`` est *la* boucle que vous devez utiliser dès que vous entendez le mot ``Array``. En effet elle vous permettra d'afficher tous les éléments d'un tableau et ce un par un :

```js
let fruits = ["Pomme", "Orange", "Fraise"];

fruits.forEach((fruit) => {
  console.log(fruit);
});
```
Output console : ``Pomme`` ``Orange`` ``Fraise``

### Ajouter une donnée

Tu souhaites ajouter des données dans ton tableau ``(.push)`` :

```js
let fruits = ["Pomme", "Orange", "Fraise"];

fruits.push("Kiwi");

console.log(fruits);
```
Output console : ``["Pomme", "Orange", "Fraise", "Kiwi"]``

### Supprimer la dernière donnée

Avec ``.pop()`` tu pourras supprimer le dernier élément de ton tableau :

```js
let fruits = ["Pomme", "Orange", "Fraise", "Kiwi"];

fruits.pop();

console.log(fruits);
```
Output console : ``["Pomme", "Orange", "Fraise"]``

### Supprimer le première donnée

``.shift()`` fonctionne comme .pop() mais supprimera le premier élément du tableau :

```js
let fruits = ["Pomme", "Orange", "Fraise", "Kiwi"];

fruits.shift();

console.log(fruits);
```
Output console : ``["Orange", "Fraise", "Kiwi"]``

### Ajouter une donnée à l'indice 0

```js
let fruits = ["Pomme", "Orange", "Fraise"];

fruits.unshift("Kiwi");

console.log(fruits);
```
Output console : ``["Kiwi", "Pomme", "Orange", "Fraise"]``

### Supprimer une donnée grâce à son indice[]

Si vous souhaitez supprimer un élément et que vous connaissez son indice, utilisez ``.splice()`` dans les parenthèses indiquez l'indice de l'élément que vous voulez supprimer :

```js
let fruits = ["Pomme", "Orange", "Fraise"];

fruit.splice(1);

console.log(fruits);
```
Output console : ``["Pomme", "Fraise"]``

### Copier un tableau

``.slice()`` le mot ressemble beaucoup à celui du dessus alors attention 😉 :

```js
let fruits = ["Pomme", "Orange", "Fraise"];

let copyFruits = fruit.slice();

console.log(copyFruits);
```
Output console : ``["Pomme", "Orange", "Fraise"]``

### Petite précision !

Dans votre code vous avez encodé vous-même votre tableau **mais** quand vous serez développeur, vous utiliserez des tableaux qui ne seront peut-être pas dans votre code source et dont vous ne serez pas le "propriétaire". Donc si vous faites une suppression, ce sera **irréversible**... C'est à ce moment qu'on se dit heureusement il y a ``.slice()`` attention quand même de ne pas copier un tableau avec des milliers de données 😋

## Let's go practice !

Pour vous habituer à lire de la documentation, l'exercice ne portera pas que sur les tableaux mais aussi sur votre compréhension à l'anglais ou à l'utilisation de tous les outils qu'Internet vous offre ! Il y a aussi certains que nous n'avons pas encore vu *mais* vous avez **google** ou votre *coach* 😁 


### 1. Length 
```js
let myAlphabet = [
  "A",
  "B",
  "C",
  "D",
  "E",
  "F",
  "G",
  "H",
  "I",
  "J",
  "K",
  "L",
  "M",
  "N",
  "O",
  "P",
  "Q",
  "R",
  "S",
  "T",
  "U",
  "V",
  "W",
  "X",
  "Y",
  "Z",
  "$",
  "*",
  "/",
  "-",
  "+",
];
```
- What is the length of the array?
- Write a function called ``myAlphabetLength()`` which **console.log** the length of the array.

### 2. Create an Array
- Declare and initialize an array called ``planets`` with **5 string values**.
- ``console.log`` ***each*** item in the array.
- Also ``console.log`` the index in each iteration.

### 3. Manipulate data types
- Declare and initialize an array called ``someDataTypes``.
- This array must have 4 differents data types (NOT Objects).
- Write and display in your console the ``typeof`` for each iteration.
- Display in your console the ``index`` of each data in your array.

### 4. Empty Array
- Create an empty ``Array``.
- ``console.log`` this empty Array and keep it during all this exercise.
- Add some data in it, the type you want, the theme you want.
- Copy your ``Array``
- ``console.log`` this new ``Array``

### 5. How many letters?
```js
let furnitures = ['Table', 'Chairs','Couch'];
```
- For each item in this array ``console.log`` the letters in each item.

### 6. Which one is a number?

```js
let values1= ["Apple", 1, false, "2"];
let values2 = [`5`, "Fries", 2 , true];
let values3 = ["Mars", "Strawberry", 9];
```
- Delete data types which are not numbers.

### 7. Gemini (optional & hard)
I give you this two arrays :
```js
let studentCoursesA = ['Math', 'English', 'Programming'];
let studentCoursesB = ['Geography', 'Spanish', 'Programming'];
```
- Find a way to compare it and if there any common words, console.log them.


> Exercises Credits : [Kauress](https://dev.to/kauresss/some-js-array-exercises-for-beginners-9j8)
> 
> Edited by Lucas Ielli Sirius

