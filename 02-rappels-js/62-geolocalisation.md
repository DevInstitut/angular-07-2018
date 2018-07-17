# Géolocalisation

* Pour faciliter le positionnement des utilisateurs, une nouvelle API est apparue.
* Celle-ci permet d'accéder à la position connue par le navigateur internet.
* La méthode de détermination est à la discrétion du navigateur...
* L'utilisateur a le droit de refuser de partager sa localisation
* Pour des raison évidentes de protection de la vie privée, il ne doit pas y avoir de solution de contournement !
* C'est une API par callback qui utilise l'objet `geolocation`.

```js
navigator.geolocation.getCurrentPosition(
  function(position) { …	}, 
  function(error) {…}
);
```
Quelques propriétés :
* `coords.latitude`
* `coords.longitude`
* `coords.altitude`
* ...