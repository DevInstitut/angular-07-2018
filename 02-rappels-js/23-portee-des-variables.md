# Portée des variables

Les variables peuvent être `globales` ou `locales`.

Une variable globale :
* Est accessible et modifiable à n'importe quel endroit du programme.
* Est rattachée à l'objet dit `objet global`.

## Exemple

```js
a = 1;

function test() {
	alert(a);	// affiche 1
	a++;
}

test();
alert(a);	// affiche 2
```

## Variable globale
  
Lorsqu'une variable est déclarée en dehors d'une fonction, elle est de portée globale.

```js
i = 2; // variable globale.

function test() {  
  document.write("Valeurs de i : " + i); 
} 
```

## Variable locale

Une variable locale :
* se déclare, dans un bloc de code donné, en utilisant le mot clé `var`.
* a une portée limitée au bloc de code dans lequel elle est déclarée.

Attention : si omission du mot clé `var`, la variable sera globale, même si elle déclarée dans un bloc de code !


