# Tableau - filter()

La fonction `filter()` crée et retourne un nouveau tableau contenant tous les éléments du tableau d'origine pour lesquels la fonction callback retourne true.

```js
var nombres = [1, 3, 43, 4, 121, 9, 314, 31];

var estEgalAUn = function(element, index, array) {
	return element == 1;
}

nombres.filter(estEgalAUn); // renvoie [1]
```
