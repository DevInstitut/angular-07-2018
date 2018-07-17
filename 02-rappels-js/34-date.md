# Date

Créer une date :

```js
var uneDate = new Date();
```

Les méthodes :

* `uneDate.getDate()` : retourne le jour du mois (1 à 31).
* `uneDate.getMonth()` : retourne le mois (0 à 11).
* `uneDate.getFullYear()` : retourne l'année depuis 1900.
* `uneDate.getHours()` : retourne l'heure (0 à 23).
* `uneDate.getMinutes()` : retourne les minutes (0 à 59).
* `uneDate.getSeconds()` : retourne les secondes (0 à 59).
* `uneDate.getTime()` : retourne le nombre de millisecondes depuis le 1er janvier 1970, utilisé pour comparer des dates.

Toutes les méthodes `get` ont leur équivalent pour fixer les valeurs : `set`.
Exemple : `uneDate.setDate(jour)` fixe le jour du mois.