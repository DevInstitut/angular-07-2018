# Tableaux - every()
La fonction `every()` permet de tester si tous les éléments d'un tableau vérifient une condition donnée par une fonction en argument.

```js
var nombres = [1, 3, 43, 4, 121, 9, 314, 31];

var estPositif = function(element, index, array) {
	return element > 0;
}

nombres.every(estPositif); // renvoie true
```
