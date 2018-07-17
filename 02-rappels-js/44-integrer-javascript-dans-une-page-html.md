# Intégrer Javascript dans une page html

Le code JavaScript est intégré dans la page HTML via la balise `<script>`.

On précise via son attribut `type` que le langage de script utilisé est `text/javascript`;

La balise `<script>` peut figurer à n'importe quel endroit du document.


Trois utilisations différentes de la balise `<script>` :
* Le code javascript est écrit dans des valeurs d'attributs HTML.
* Le code javascript est écrit directement à l'intérieur de la balise.
* Le code est écrit dans des fichiers externes (généralement pourvus de l'extension .js) liés au document via l'attribut 'src' de la balise.


## Le code javascript est écrit dans des valeurs d'attributs HTML

```html
<a onclick="lancerFonction()">Bouton</a>
```

## Balise Script

Utilisation de la balise `<script>` directement dans la page HTML.

```html
<script type="text/javascript">
	alert('Bonjour');
</script>
```
Cette syntaxe permet :

* d'éviter les erreurs d'interprétation de caractères tels que < ou >;
* d'être valide entre le code HTML, XHTML et XML.

## Fichier externes

```javascript
<script type="text/javascript" src="monJS.js"></script>
```

* une balise `<script>` par fichier à lier.
* la balise de fermeture est obligatoire

Dans le fichier externe, la balise `<script>` est inutile :

Exemple  de contenu du fichier monJS.js :

```js
alert('Bonjour');
```


## Quelle intégration choisir ?

* Privilégier l'externalisation de scripts pour :
  * Mutualiser le code et faciliter la maintenance.
  * Constituer des bibliothèques de fonctions réutilisables.

* Privilégier les scripts internes si :
  * Peu de code, peu de fonctions.
  * Code très spécifique au contexte de la page.
