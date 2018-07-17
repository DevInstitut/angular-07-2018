# Encapsulation

## Propriétés publiques

```js
function Chien (){
	this.nom = "Nom publique";
	this.aboyer = function () {
		return "Ouaf !!";
	}
}
```

## Propriétés privées

```js
function Chien (){
	var nom = "Nom privé";
	var aboyer = function () {
		return "Ouaf !!";
	}
}
```

## Méthodes privilégiées

* Peuvent accéder aux propriétés privées tout en étant elles-mêmes d'accès public

```js
function Chien (){
	var nom = "Nom privé";
	this.aboyer = function () {
		return nom + " dit : Ouaf !!";
	}
}
```
