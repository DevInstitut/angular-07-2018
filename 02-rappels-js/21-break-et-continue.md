# break et continue

Interrompre une boucle à tout moment : `break`.

```js
for (i=1; true ; i++) {
	if (i>10) break;
	// arrête la boucle au bout de 10 itérations
}
```

Passer immédiatement à l'itération suivante : `continue`.

```js
for (i=1;i<11 ; i++) {
	if (i % 2) continue; // i impair
	document.write(i +"</br>");
}
```
