# AJAX

AJAX = Asynchronous JavaScript and XML.

Mécanisme qui permet de mettre à jour une page de la page avec des données provenant d'un serveur sans avoir à recharger l'intégralité de la page courante.

AJAX est basé sur :
* L'objet `XMLHttpRequest` qui permet d'effectuer des échanges asynchrones avec un serveur.
* JavaScript/DOM pour récupérer les résultats et mettre à jour l'affichage de la page.
* CSS pour mettre en forme des éléments.
* XML comme format d'échange des données.


## Exemple XMLHttpRequest

```js
var xmlhttp;
if (window.XMLHttpRequest) {
  xmlhttp=new XMLHttpRequest(); // IE7+, Firefox, Chrome, Opera, Safari
} else {
  xmlhttp=new ActiveXObject("Microsoft.XMLHTTP"); // IE6, IE5
}

xmlhttp.open("POST","/formulaire",true);
xmlhttp.setRequestHeader("Content-type","application/x-www-form-urlencoded");
xmlhttp.send("nom=Francois&prenom=Miller");

xmlhttp.onreadystatechange=function(){
  if (xmlhttp.readyState==4 && xmlhttp.status==200){
	document.getElementById("maDiv").innerHTML=xmlhttp.responseText;
	document.getElementById("maDiv").innerHTML=xmlhttp.responseXML;
  }
}
```