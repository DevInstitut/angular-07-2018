# TP #5.3 - Services

## Front - Gérer les URLs backend

Notre application front va communiquer avec l'application back pour récupérer les données.

Il va falloir gérer 2 urls backend :
* `http://localhost:port` en mode développement
* `http://adresseheroku` en mode production

Vous pouvez pour cela utiliser le module environment `src/environments/environment`.

Vous configurez le fichier `src/environments/environment.ts` pour le mode développement. Exemple :

```ts

export const environment = {
  production: false,
  
  // ajout d'une URL backend en mode développement
  backendUrl: 'http://localhost:port'
};


```

Vous configurez le fichier `src/environments/environment.prod.ts` pour le mode production. Exemple :

```ts

export const environment = {
  production: true,
  
  // ajout d'une URL backend en mode développement
  backendUrl: 'http://adresseheroku'
};


```

A l'utilisation, :

```ts
import {environment} from '../../environments/environment';


// en développement, URL_BACKEND = 'http://localhost:port'
// en mode production, URL_BACKEND = 'http://adresseheroku'
const URL_BACKEND = environment.backendUrl;


```

## Front - Service `StagiaireService`

* Générer un service `Stagiaire`

```
ng g service services/Stagiaire
```

* Compléter le service `Stagiaire` pour consommer les services backend :

```ts
@Injectable()
export class StagiaireService {

  constructor() { }

  listerStagiaires():Promise<Stagiaire[]>  {
    // récupérer la liste des collègues côté serveur
  }

}
```

* Mettre à jour l'application pour récupérer les stagiaires depuis une application backend.
