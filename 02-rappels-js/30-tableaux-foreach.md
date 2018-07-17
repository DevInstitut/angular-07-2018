# Tableaux - forEach()
La fonction `forEach()` : permet d'exécuter une fonction donnée sur chaque élément du tableau.

```js
var nombres = [1, 3, 43, 4, 121, 9, 314, 31];

function afficher(element, index, array) {
	console.log(element);
}

nombres.forEach(afficher);

// ou

nombres.forEach(function(element){
	console.log(element);
});
```
