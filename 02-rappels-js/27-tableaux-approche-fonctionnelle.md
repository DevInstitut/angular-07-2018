# Tableaux - Approche fonctionnelle
```js
// approche fonctionnelle

var isSupDix = function(element) {
  return element > 10;
}
var supDix = nombres.filter(isSupDix);

```

Depuis ES5 (IE9+), les tableaux se sont enrichis de fonctions :

* `every()` : teste si tous les éléments d'un tableau vérifient une condition donnée par une fonction en argument.

* `some()` : teste si certains éléments du tableau passent le test implémenté par la fonction fournie.

* `forEach()` : permet d'exécuter une fonction donnée sur chaque élément du tableau.

* `map()` : crée un nouveau tableau composé des images des éléments d'un tableau par une fonction donnée en argument.

* `filter()` : crée et retourne un nouveau tableau contenant tous les éléments du tableau d'origine pour lesquels la fonction callback retourne true.

* `reduce()` : applique une fonction qui est un « accumulateur » et qui traite chaque valeur d'une liste (de la gauche vers la droite) afin de la réduire à une seule valeur.


