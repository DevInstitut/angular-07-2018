
# Document

Un objet de type `Document` est un objet qui contient des informations sur le document chargé par la fenêtre du navigateur.

Une variable `document`, de type `Document` , est créée automatiquement lors du chargement d'un document par le navigateur.
`document` est rattaché à l'objet `window` : `window.document`.

## Les principales propriétés :
* `document.applets` : retourne la collection d'applets java présente dans le document.
* `document.domain` : indique le nom de domaine du serveur ayant apporté le document.
* `document.images` : retourne la collection d'images du document.
* `document.links` : retourne la collection de liens du document.
* `document.referrer` : indique l'adresse de la page précédente.
* `document.title` : indique le titre du document.

## Les méthodes :
* `close()` : ferme le document en écriture.

* `open()` : ouvre le document en écriture.

* `write()` : écrit dans le document.

* `writeln()` : écrit dans le document et effectue un retour à la ligne.

