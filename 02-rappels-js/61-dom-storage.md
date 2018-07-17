# DOM Storage

Le besoin d'aller au-delà de la gestion des cookies pour bénéficier d'un réel stockage coté navigateur Internet.

Par ailleurs, contrairement aux cookies, ces données ne sont pas envoyées au serveur à chaque requête.

Ce stockage permet de conserver
* Des valeurs textuelles,
* Des variables et des objets Javascript,
* Des éléments du DOM.

Le volume maximal est limité suivant les navigateurs.

Pour pouvoir utiliser ce stockage, l'utilisateur doit accepter que la page stocke des informations.

Deux systèmes de stockage différents utilisant la même interface `Storage`.

```js
interface Storage {

  readonly attribute unsigned long length;
  [IndexGetter] DOMString key(in unsigned long index);
  [NameGetter] DOMString getItem(in DOMString key);
  [NameSetter] void setItem(in DOMString key, in DOMString data);
  [NameDeleter] void removeItem(in DOMString key);
  void clear();
  
};
```
## localStorage vs SessionStorage

localStorage  --> Enregistrer des informations qui vont pouvoir être récupérée d'une session à l'autre

```js
localStorage.setItem("contact","{'nom':'françois','prenom':'LEFRANCAIS'}");

var contact = localStorage.getItem("contact");
```

`sessionStorage`  --> Stocker des informations durant la vie de la session.

```js
sessionStorage.setItem("contact","{'nom':'françois','prenom':'LEFRANCAIS'}");

var contact = sessionStorage.getItem("contact");
```

## Storage events

HTML 5 permet d'écouter des événements de mise à jour de données.

```js
if (window.addEventListener) {
  window.addEventListener("storage", handleStorage, false);
} else {
  window.attachEvent("onstorage", handleStorage);
}
```
L'événement permet d'accéder aux informations suivantes :
* `key` : le nom de la clé.
* `oldValue` : l'ancienne valeur.
* `newValue` : la nouvelle valeur.
* `url` : la page qui a provoqué le changement.

