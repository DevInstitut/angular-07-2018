# Server-Sent Event

Permet à un serveur d'envoyer des informations (push) vers des clients (navigateurs).

Une API Javascript permet de récupérer les informations envoyées.

Le serveur doit implémenter SSE (Server-Sent Events).

```js
var source = new EventSource("/server/");

source.onmessage = function(event) {
    // traitement de la réception du message
};
```
