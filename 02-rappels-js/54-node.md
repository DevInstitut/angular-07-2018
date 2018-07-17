# Node

## Propriétés principales :
* childNodes : liste des nœuds enfant

* parentNode : le nœud parent

* nextSibling : le prochain nœud

* previousSibling : le nœud précédent

* firstChild : premier nœud enfant

* lastChild : dernier nœud enfant

* nodeName : nom du nœud

* nodeValue : valeur du nœud

## Méthodes principales :
* appendChild(node) : ajoute un nœud enfant en dernière position

* removeChild(node) : retire un nœud enfant

* insertBefore(new, ref) : ajoute un nœud juste avant le nœud de référence

* replaceChild(new, old) : remplace l'ancien nœud par le nouveau

* cloneNode(bool) : retourne un clone du nœud

* hasAttributes() : indique si le nœud a des attributs

* hasChildNodes() : indique si le nœud a des fils

Remarques : 
Argument de cloneNode() : true pour une copie incluant les fils

## Exemple

```js
var texte = document.createTextNode('hello world');
var titre = document.createElement('h1');
titre.appendChild(texte);		// Crée la balise <h1> complète

var body = document.getElementsByTagName('body').item(0);
body.insertBefore(titre,null);	// Ajoute le <h1> au <body>
			
var ul = document.createElement('ul');
var li = document.createElement('li');
li.appendChild(document.createTextNode('1er élément'));
ul.appendChild(li);		// Ajoute le <li> dans le <ul>

body.appendChild(ul);		// Ajoute le <ul> au <body>
		
var li2 = li.cloneNode(true);	// Clone <li>1er élément</li>
var li2Texte = document.createTextNode('2nd élément');
```
