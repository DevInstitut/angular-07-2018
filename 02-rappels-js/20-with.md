# with

L'instruction with définit un **objet de référence** pour le bloc d'instruction qui suit. 

```js
with(objet) {
  //Instructions;
}
```

Il est ensuite utilisé comme référence implicite

```js
with (Math) {
  x = 2;
  y = 10;

  resultat = pow(x, y);
 //sans "with" resultat = Math.pow(x, y)
}
```

