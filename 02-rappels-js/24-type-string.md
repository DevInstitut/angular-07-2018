# Type String

String est le type des chaînes de caractères.

Création d'une chaîne :
```js
var uneChaine = "Formation ajax"; //uneChaine est de type String
var uneAutreChaine : 'Formation ajax';
var autreChaine = new String("Formation ajax");
```
Propriété :
* `uneChaine.length` : longueur de la chaîne.

Les méthodes utiles :

* `uneChaine.indexOf(chaine)` : position d'une chaîne dans `uneChaine`.

* `uneChaine.indexOf(chaine)` : position d'une chaîne dans uneChaine.

* `uneChaine.replace(texte, nouveauTexte)` : recherche / remplace.

* `uneChaine.substring(indexDébut, indexFin)` : renvoi une portion de la chaîne.

* `uneChaine.split(chaineSeparateur)` : transforme une chaîne en tableau en coupant aux occurrences du séparateur spécifié.

* `uneChaine.toLowerCase()` : passe toute la chaîne en minuscule.

* `uneChaine.toUpperCase()` : passe toute la chaîne en majuscule.

* `uneChaine.big()` : formate la chaîne avec la balise `<big>`.

* `uneChaine.small()` : formate la chaîne avec la balise `<small>`.

* `uneChaine.link(url)` : formate la chaîne pour en faire un lien.

* `unChaine.anchor(name)`: formate la chaîne pour en faire une ancre.


Une chaîne de caractère est délimitée par des `"` ou des `'`.

Pour y insérer des caractères spéciaux :
* `\b` : retour en arrière
* `f` : saut de page
* `\n` : saut de ligne
* `\r` : retour chariot
* `\t` : tabulation

Pour y insérer des `"` , des `'` ou des `\`, utiliser le caractère d'échappement `\`. 
Exemple : 
```js
var a = 'l\'histoire'; // a vaut l'histoire
var b = "\"Bonjour\" dit-il"; // b vaut "Bonjour" dit-il
``` 

