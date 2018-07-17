# Tableaux - map()

La fonction `map()` crée un nouveau tableau composé des images des éléments d'un tableau par une fonction donnée en argument.

```js

var nombres = [1, 3, 43, 4, 121, 9, 314, 31];

function multiplierPar2(element, index, array) {
	return element*2;
}

nombres.map(multiplierPar2); // renvoie [2, 6, 86, 8, 242, 628, 62]
```
