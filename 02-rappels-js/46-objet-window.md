# Objet Window

Dans une page web, l'objet Global est l'objet `window`.

Une variable globale peut donc être référencée par : `window.[variable]`.

```js
maVariable = 19; // déclaration d'une variable globale sans le mot clé 'var'

window.maVariable; // vaut 19

```

Un objet de type `Window` est un objet qui contient des informations sur une fenêtre de navigateur.

Une variable `window`, de type `Window`, est créée automatiquement à l'ouverture du navigateur.

Elle contient des informations sur la fenêtre courante.

## Principales propriétés

* `window.closed` : spécifie si une fenêtre est fermée.
* `window.defaultStatus`  : l'affichage par défaut dans la barre de statut du navigateur.
* `window.document` : le document actuel.
* `window.opener` : la fenêtre parent pour une fenêtre ouverte avec la méthode open().
* `window.location` : contient les informations sur l'URL courante.
* `window.history` : Contient les informations sur l'historique des URLs visitées.
* `window.innerHeight` et `window.innerWidth` : Spécifie les dimensions de la zone de contenue.
* `window.navigator` : Contient des informations sur le navigateur utilisé.

`window` est l'objet Global, on peut donc omettre son nom quand on accède à ses attributs.


```js
// Le code suivant
window.document.write('test');
window.location = 'mapage.html';

// peut s'écrire
document.write('test');
location = 'mapage.html';
```

## Les méthodes :

* `window.moveTo()` : déplace la fenêtre vers un point spécifié.

* `window.close()` : ferme la fenêtre.

* `window.resizeBy()` : redimensionne la fenêtre d'un certain rapport.

* `window.resizeTo()` : redimensionne la fenêtre.


La méthode `window.open(url, nom, attributs)` ouvre une nouvelle fenêtre (popup) :

```js
window.open("fichier.htm","fenetre1","width=310,height=400");
```

* `url` : L'url de la page que doit afficher la nouvelle fenêtre.
* `nom` : Le nom de la nouvelle fenêtre.
* `attributs` : La liste des attributs qui définissent la fenêtre.
* `width` : La largeur en pixel.
* `height` : La hauteur en pixel.
* `location` : 1 ou 0. Affiche ou non la barre d'url.
* `status` : 1 ou 0. Affiche ou non la barre de statut.
* `scrollbars` : 1 ou 0. Affiche ou non les barres de scroll.
* `resizable` : 1 ou 0. Permet ou non de redimensionner la fenêtre.

Rappel : `window` est l'objet Global, on peut donc omettre son nom quand on accède à ses méthodes.

```js
window.open("fichier.htm","fenetre1","width=310,height=400");
```

Peut s'écrire :
```js
open("fichier.htm","fenetre1","width=310,height=400");
```

Pour agir sur une fenêtre ouverte avec open(), on conserve la valeur renvoyée par cette fonction.
```js
var maPopup = open("fichier.htm","fenetre1","width=310,height=400");
maPopup.close();
```
