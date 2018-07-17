# Tableaux

En javascript, les tableaux sont de type `Array`.

Création d'un tableau :
```js
var unTableau = new Array();
var unAutreTableau = ['Element0','Element1',…];
var autreTableau = new Array('Element0', 'Element1', …);
```
Accéder aux éléments d'un tableau :
`unTableau[index]`.

Premier élément à index 0.

Les propriétés :
* `unTableau.length` : nombre d'éléments.

Les méthodes :
* `unTableau.push(valeur, …)` : ajoute les éléments à la fin du tableau.

* `unTableau.unshift(valeur, …)` : ajoute les éléments au début du tableau.

* `unTableau.pop()` : enlève le dernier élément du tableau.

* `unTableau.shift()` : enlève le premier élément du tableau.

* `unTableau.join(séparateur)` : assemble les éléments du tableau pour en faire une chaîne.

* `unTableau.reverse()` : inverse l'ordre des éléments.

* `unTableau.sort([fonction])` : trie les éléments du tableau.

* `unTableau.concat(tableau1, …)` : concatène des tableaux.


```js
var unTableau = new Array('Element0', 'Element1', …);

var i = 0;

for(i = 0; i < unTableau.length; i++){
	alert(unTableau[i]);
}
```