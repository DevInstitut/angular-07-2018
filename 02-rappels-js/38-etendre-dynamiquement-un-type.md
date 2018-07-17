# Etendre dynamiquement un type

Utilisation de la propriété `prototype`.

Pour ajouter une propriété à tous les objets d'un type donné :

```js
Fonction.prototype.unePropriete = uneValeur;
```

Pour ajouter une méthode à tous les objets d'un type donné :
```js
function uneMethode() {
	…
}

Fonction.prototype.uneMethode = uneMethode;
```

Ou avec une méthode anonyme :
```js
Fonction.prototype.uneMethode = function() { 
	… 
}
```

