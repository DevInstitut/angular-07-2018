# for...in

L'instruction `for...in` permet le parcours d'un tableau ou des propriétés d'un objet.

```js
for(variable in unObjet){
  //Instructions;
}
```

Chaque itération affecte à la variable le nom de la propriété suivante de l'objet :

```js
var obj = new Object();
obj.name = "toto";
obj.surname = "titi";

var i = 0;
for( i in obj) {
  alert('obj[' + i + '] = ' + obj[i]);
}
```

