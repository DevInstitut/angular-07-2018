# Cookies

Permettent de stocker de l'information sur le poste de l'internaute :
* Sous forme clé = valeur.
* Les valeurs ne doivent pas contenir d'espace ni de caractères spéciaux.
* Un cookie est associé à un domaine donné. Seul celui-ci peut lire un cookie qui lui est associé.

Les cookies sont gérés via la propriété `cookie` de l'objet `document`.


## Créer un cookie

On crée la chaîne qui va contenir l'ensemble des couples clé=valeur à enregistrer (un couple = un cookie).

Les couples clé=valeur sont séparés par des `;`.

On l'affecte à `document.cookie`.

```js
//Chaine descriptive du cookie, contient deux cookies
monCookie = "toto=" + escape("une valeur test.") + ";titi=25";

//Création du cookie
document.cookie = monCookie;
```
Penser à utiliser la fonction escape() pour encoder les caractères spéciaux.

Il est possible de préciser :
* Une date d'expiration du cookie (clé `expires`). Si la date n'est pas spécifiée le cookie est détruit à la fermeture du navigateur.

```js
expires = objet Date configuré à la bonne date
```

* Un domaine (clé `domain`). Il est possible de créer 20 cookies par domaine.

```js
domain=le domaine
```


## Lire un cookie :
* Il faut récupérer la chaîne dans `document.cookie` qui contient tous les cookies.
* Vérifier l'existence du cookie désiré dans la chaîne.
* L'extraire avec des fonctions telles que `indexOf` et `substring`.

