<!-- 1. Les boucles
Le super guide de la MDN sur le concept des boucles:
https://developer.mozilla.org/fr/docs/Web/JavaScript/Guide/Boucles_et_itération
La boucle for
Une boucle permet de performer une action tant que son cycle d'itérations n'est pas rempli par sa condition.
function populateArray(number) {
    let array = [];
    for(let i = 0; i <= number; i++) {
        array.push(i);
    }
    console.log(array)
}
populateArray(100);


On peut lire cette fonction de telle manière:
"Pour la variable number attribuée à 100 et tant que la valeur de i est plus petite ou égale à la valeur de number, on ajoute la valeur de i à array
Il existe d'autres types de boucles, le do-while (faire, tant que), while (tant que), et le forEach (pour chaque élément).

La boucle do...while
Celle ci exécute une action tant que sa condition n'est pas remplie. Elle ne s'auto incrémente pas cependant contrairement à la boucle for qui possède une auto incrémentation en paramètre de fonction.
Syntaxe :
let number = 0;
do {
    arrayy.push(number)
    } 
    while (number <= 100);
    console.log(arrayy)


La boucle while
Encore plus minimaliste, la boucle while part du principe que tant que sa condition n'est pas remplie elle exécute le bout de code donné. De la même façon que do...while, la boucle while n'auto incrémente pas sa condition, il faut le spécifier. L'utilité de ces boucles réside dans le fait que l'on peut leur passer comme condition true / false, contrairement à la boucle for qui ne vérifie que des valeurs numériques.
let number = 0
while (number <= 100){
    arrayy.push(number;)
    number++;
}
console.log(arrayy)



La méthode forEach
Contrairement à ses congénères ci dessus, la méthode forEach ne peut s'appliquer qu'aux tableaux. Il s'agit ici de créer une boucle qui va exécuter une fonction pour chaque éléments du tableau donné. Il n'y a pas de condition à remplir contrairement aux précédentes versions. Elle est destinée uniquement à apporter une modification/ une opération pour chaque éléments du tableau. Par exemple, dans le cas où vous voudriez créer des éléments HTML de manière dynamique, nous pourrions dire que pour tous les éléments titre d'un objet, contenu dans un tableau, je génère un titre h2 dans mon code HTML.
let siriusTeamArray = ["Jeremy", "Christophe", "Julie", "Thomas", "Laetitia", "Laura"];
siriusTeamArray.forEach(element => 
                        console.log(`Salut ${element}`)
); -->