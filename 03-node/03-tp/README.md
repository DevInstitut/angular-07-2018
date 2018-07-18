# TP #2 - NPM & Node

## Objectif

L'objectif est de réaliser une application console permettant d'administrer les entités d'EvalMe.

L'application console aura la forme suivante :

```
** EvalMe - Console Administration **

1. Stagiaire
2. Classe
3. Duel
4. Examen
5. Quizz
6. ...

Choisir une entité : ...
```

Chaque choix conduit à un sous-menu propre à l'entité.

L'application va être réalisée à l'aide de NodeJS.

## Initialisation

* Récupérer le projet `evalme-console`.

* Visualiser le fichier `package.json`. Que fera la commande `npm start` ?

* Exécuter la commande `npm start`. Tester le menu de l'application.

* Visualiser le code de démarrage. Comprenez-vous tout ?

## Nouveau module

* Créer un nouveau répertoire représentant votre entité.

Exemple d'architecture à terme :

```
/evalme-console
    index.js
    /concours
    /stagiaire
    /quizz
    /...
```

* Créer y un fichier `index.js`.

```
/evalme-console
    index.js
    /concours
        index.js
```

* Y ajouter le code suivant :

```js

var TITRE = 'ENTITE';

var demarrer = function(rl, sortir) {
    lg('*** ' + TITRE + ' ***');
};

module.exports = {
    titre : TITRE,
    demarrer : demarrer
}
```

* Ajouter votre module à la liste des modules de l'application (fichier `index.js` situé à la racine du projet).

* Vérifier que votre module est intégré grâce à `npm start`.

## Menu Lister

Nous souhaitons dans cette rubrique, afficher la liste de vos entités situées en base de données.

Il nous faudra pour cela effectuer une requête HTTP depuis notre application NodeJS.

### Requête HTTP

Il y a plusieurs techniques permettant de récupérer des données via HTTP.

L'article suivant en donne un aperçu des techniques permettant d'effectuer une requête HTTP dans l'environnement Node : https://www.twilio.com/blog/2017/08/http-requests-in-node-js.html.

Nous allons utiliser la librairie `Request` (https://github.com/request/request).

Expérimentons l'usage de cette librairie.

* Installer la librairie via NPM

```
npm install --save request
```

Visualiser l'impact dans le fichier `package.json`.


* Créer un fichier : `exemples/exemple-request-json.js` avec le contenu suivant :

```js
// importation de la librairie request
// recherche par défaut dans le répertoire node_modules
var request = require('request')

// Envoie de la requête http
request('https://jsonplaceholder.typicode.com/posts', { json: true }, function(err, res, body) {
    if (err) { return console.log('Erreur', err); }

    // body contient les données récupérées
    console.log('Ok', body);
});
```
* Tester le script `node exemples/exemple-request-json.js`.

### Service

* Ajouter à votre module un fichier `service.js`.

```
/evalme-console
    index.js
    /concours
        index.js
        service.js
```

`index.js` : le point d'entrée de votre module, composant qui intéragit avec l'utilisateur.
`service.js` : composant qui récupère les données distantes

* Compléter le fichier `service.js` :

```js

exports.lister = function (callback) {
    
    var uneListe = [{ nom : 'Hugues'}];

    // transmission de la réponse grâce à la technique du callback
    callback(uneListe);

};
```

* Créer un fichier `exemples/exemple-service.js` avec le code suivant :

```js
var service = require('../VOTREMODULE/service')

// exemple d'utilisation de la liste.
service.lister(function(uneListe) {
    console.log(uneListe[0].nom);
});
```

* Exécuter le fichier `exemples/exemple-service.js`:

```
node exemples/exemple-service.js
```

Vérifier l'affichage :

```
Hugues
```

* Compléter le fichier `service.js` en suivant les instructions en commentaires.


### Menu Lister

Implémenter le menu suivant pour votre entité :

```
*** ENTITE ***
1. Lister les xxxx
```

Afficher les données de manière élégante (pas le JSON en brut ;-)).

> **Bravo ! Effectuer votre première Pull Request !**


## Menu créer

Implémenter un menu créer pour votre entité.

> **Bravo ! Effectuer votre seconde Pull Request !**