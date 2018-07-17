# Tableaux - some()

La fonction `some()` teste si certains éléments du tableau passent le test implémenté par la fonction fournie.

```js
var nombres = [1, 3, 43, 4, 121, 9, 314, 31];

var estEgalAUn = function(element, index, array) {
	return element == 1;
}

nombres.some(estEgalAUn); // renvoie true
```
