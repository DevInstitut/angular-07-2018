# Tableaux - Approche Impérative

Soit le tableau suivant :

```js
var nombres = [1, 3, 43, 4, 121, 9, 314, 31];
```

Supposons que nous souhaitons avoir un tableau dont les nombres sont supérieurs à 10.

```js
// approche impérative

var supDix = [];
for (var i=0; i<nombres.length; i++) {
    if (nombres[i] > 10) {
    supDix.push(nombres[i]);
    }
}
```

