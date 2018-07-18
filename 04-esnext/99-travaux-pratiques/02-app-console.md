# #3.2 EvalMe Console App

> Objectif : migrer l'application EvalMe Console vers la syntaxe ES2015+.

## let, const

Remplacer le mot clé `var` par `let` ou `const` suivant les cas.

> Avis personnel : priorité à `const`.

## Template de string

Remplacer les concaténations de chaînes de caractères par des templates de string.

## Arrow function

Remplacer les fonctions anonymes par les fonctions fléchées.

## Promesses

Remplacer l'utilisation de la librairie [`request`](https://github.com/request/request) par la librairie [`request-promise-native`](https://github.com/request/request-promise-native).

Les services doivent à présents renvoyés des promesses à la place de l'utilisation de callbacks.

## Classes

Utiliser des classes pour construire les structures.

Exemple de structure de la classe `Service` :

```js

class Service {
    
    init() {
        
    }
    
    listerSessions() {
        
        // retourne une promesse
    }
    
}
```

