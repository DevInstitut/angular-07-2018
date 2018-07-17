# Fonctions

Déclarée via le mot clé `function`.

Une fonction comporte :
* Un nom.
* Un ou plusieurs arguments entre parenthèses.
* Le corps de la fonction entre `{ }`.

Une fonction peut :
* retourner un résultat de traitement (tout type de données) grâce à l'instruction `return`.

## Nommage
Le nom des fonctions : 
* Doit toujours commencer par une lettre ou $, et ne contenir que des lettres, chiffres, _ ou $
* Est sensible à la casse.

## Exemple de fonction :

```js
function afficheTexte(texte) {
	document.write(texte);
}
```

La fonction de l'exemple :
* Prend un paramètre : `texte`.
* Elle écrit dans le document courant la valeur de la variable `texte`.
* Elle ne retourne rien (pas d'instruction `return`).

## Retour d'une fonction

On ne spécifie pas de type pour les arguments ou pour la valeur retournée.

```js
function maFonction(arg1, …, argn) {
	// corps de la fonction
	…
	// retourne une valeur
	return valeur;
}

maFonction(…);
```

## Variable de type Fonction

Une variable peut être de type fonction.

```js
var maFonction = function(arg1, ..., argn) {
  ...
}

maFonction(...);
```

# Fonction en paramètre
Une fonction peut être passée en paramètre d'une autre.

```js
function maFonction1(arg1) {
  // exécution de la fonction arg1
  arg1();
}

function maFonction2() {
  ...
}

maFonction1(maFonction2);
```

## Fonction anonyme

```js
function maFonction1(arg1, arg2) {
  // exécution de la fonction arg1
  arg1();
  ...
}

// passage en paramètre d'une fonction anonyme
maFonction1(function(){
  ...
}, "param2");
```