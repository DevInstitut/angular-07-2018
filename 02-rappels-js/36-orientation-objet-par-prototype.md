# Orientation objet par prototype

Un objet est extensible et modifiable à l'exécution
* Objets complètement dynamiques : ajout de méthodes et propriétés à la volée.
* Permet d'étendre les objets natifs prédéfinis du langage.

On utilise le mot clé `new` pour créer un nouvel objet.

```js
function chien(nom) {
	this.nom = nom;
	this.aboyer = function (){
		return 'Ouaf !!';
	}
}

var Medor = new chien('Médor');
alert(Medor.nom);		// Médor
alert(Medor.aboyer());	// Ouaf !!
```

Accéder à l'objet courant à l'intérieur d'une de ses fonctions :
* Utilisation du mot clé `this`.

Les objets en Javascript peuvent être vus comme des tableaux associatifs

```js
function chien(nom) {
	this.nom = nom;
}

var Medor = new chien('Médor');
alert(Medor.nom);
alert(Medor["nom"]);
```