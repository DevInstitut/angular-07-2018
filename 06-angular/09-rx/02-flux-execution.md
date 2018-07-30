# Contrôle du flux d'exécution


```js
import { Observable, fromEvent } from 'rxjs'
// opérateur filter
import { filter } from 'rxjs/operators';

// opérateur map
import { map } from 'rxjs/operators';

const input$ = fromEvent(document.querySelector('input'), 'input');

// filtrer les saisies de moins de 3 caractères
input$
    .pipe(
        filter(event => event.target.value.length > 2),
        map(event => event.target.value)
    ).subscribe(value => console.log(value));
```

En savoir plus sur les opérateurs : https://www.learnrxjs.io/operators/.

