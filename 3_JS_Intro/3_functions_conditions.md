<!-- omit in toc -->
# Les fonctions et les conditions
<!-- omit in toc -->
## Table des matières
- [Les fonctions (functions)](#les-fonctions-functions)

## Les fonctions (functions)

Une fonction est un ensemble d'instructions menant à la réalisation d'une tâche. Par exemple je souhaite afficher mon prénom dans la console avec un petit message de bienvenue adapté lors de ma connexion. On peut imaginer une fonction telle que celle-ci :

```js
function helloWhenConnected(name) { 
    let name = name;
    console.log(`Salut ${name}`); // Concaténation avec des backticks
    console.log("Salut " + name); // Concaténation avec le symbole +
}; 
 
helloWhenConnected("Lucas");
``` 
 
Résultat dans la console : ``Salut Lucas``

Une fonction contient un constructeur ``()`` qui peut recevoir un ou plusieurs paramètres comme dans l'exemple ci-dessus ``(name)`` et les instructions à executer englobées via ``{}``, grâce à ces éléments on devine donc que la fonction est en fait de ``type objet``. On la définit sous plusieurs formes, elle est déclarée à l'aide du mot-clé ``function``. Nous verrons plus tard qu'il est également possible de la déclarer sous forme d'une constante à l'aide ce que l'on appelle ``arrow function`` qui est un standard **ECMAscript6**. 

Une fonction peut retourner une valeur, on peut par exemple l'utiliser pour réaliser des opérations : 

```js
function multiply(a, b){ 
    return a * b; 
}; 
console.log(multiply(2, 4));

``` 
Output console : ``8``

<!-- HAS BEEN STOPPED

Dans ce bout de code on appelle la fonction à l'aide de son nom suivit de son constructeur comprenant les deux paramètres que j'ai décidé de lui attribuer (2 et 4). Vous le comprendrez, les paramètres défini lors de la construction de la fonction sont en réalité une valeur abstraite destinée à être remplacée par une donnée. Cette donnée est intégré lors de l'appel à la fonction. Pour lancer une fonction il faut en effet faire appel à elle, pour ce faire vous l'avez constaté il suffit d'indiquer le nom de la fonction désirée suivie de son constructeur () et du point virgule. 

// Exemple d'appel de fonction: 
multiplication(2,4); 

 
 

Observez la fonction helloWhenConnected et la fonction multiplication, n'y-a-t-il pas une différence dans la synthaxe? Le mot clé return apparaît dans la seconde fonction. Sans lui le résultat de l'opération ne serait tout simplement pas retourné à l'écran.  -->