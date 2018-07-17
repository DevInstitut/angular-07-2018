# Tableau - reduce()

La fonction `reduce()` applique une fonction qui est un *accumulateur* et qui traite chaque valeur d'une liste (de la gauche vers la droite) afin de la réduire à une seule valeur.

```js
var nombres = [1, 3, 43, 4, 121, 9, 314, 31];

var additionner = function(previousValue, currentValue) {
	return previousValue + currentValue;
}

nombres.reduce(additionner); // renvoie le résultat de 1+3+43+4+121+9+314+31
```
