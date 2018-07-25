# TP #5.7 - RxJS

## Migration Promise => Observable

Modifier les services de l'application pour utiliser le type `Observable` à la place de `Promise`.

Exemple de signature :

```ts
@Injectable()
export class StagiaireService {

  constructor() { }

  lister():Observable<Collegue[]>  {
    ...
  }

}

```
