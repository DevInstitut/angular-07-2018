
# Exceptions

Exceptions : `try / catch / finally` et `throw`

L'instruction throw est utilisée pour « lancer » une exception.

```js
throw expression;
```

En javascript, une exception peut-être de n'importe quel type.

```js
throw "erreur202"; //Une chaîne de caractères

throw 400; // Un nombre

throw null; //La valeur null

```


L'instruction `try` permet de capturer une exception lancée dans le bloc de code qui suit.

Si une exception est lancée, l'instruction catch la saisira.
* L'instruction catch stockera l'exception dans la variable précisée.
* Permet de spécifier un code pour gérer le cas d'exception.

```js
/*Si x est inférieur à 0, l'exception erreur est lancée dans try.*/
try {
  if (x>0) {
    resultat = Math.sqrt(x);
  } else {
    throw "erreur";
  };
}
catch (ex) { //ex stocke erreur
  alert('Opération Impossible');
}
```

Le bloc `finally` est exécuté quoi qu'il arrive.

Si aucune exception n'est levée, il est exécuté après le bloc `try`.

Si une exception est levée, il est exécuté après le bloc `catch`.

```js
try {
  OuvertureFichier(); // attache une ressource
  EcritureFichier(donnee);
} catch {
  CaptureErreur();
} finally {
   FermetureFichier(); //ferme la ressource
}
```

