# Opérateur `in`

L'opérateur `in` renvoie `true` si la propriété spécifiée se trouve dans l'objet spécifié.

```js
// Tableaux
arbres = new Array("séquoia", "laurier", "cèdre", "chêne", "érable");
0 in arbres         // renvoie true, index 0 du tableau
6 in arbres         // renvoie false, index 6 du tableau
"laurier" in arbres // renvoie false
"length" in arbres  // renvoie true

// Objets prédéfinis
"PI" in Math         // renvoie true
maChaine = new String("corail");
"length" in maChaine // renvoie true
```
