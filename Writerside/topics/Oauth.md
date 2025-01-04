# Module OAuth

<note type="info">Le module **OAuth** de NationsAPI permet de gérer les services d'authentification et de vérifier les tokens pour interagir en toute sécurité avec l'API de NationsGlory.</note>

---

## Description

Le module **OAuth** regroupe des méthodes pour créer, mettre à jour, supprimer des services OAuth, ainsi que pour vérifier l'état des tokens. Ce module est essentiel pour les intégrations nécessitant une gestion sécurisée des autorisations.

---

## Méthodes Disponibles

### `createService(name, redirectUri)`

Crée un nouveau service OAuth.

#### Paramètres {id="param-tres_1"}
- `name` *(string, requis)* : Le nom du service.
- `redirectUri` *(string, optionnel)* : L'URI de redirection associée au service.

#### Exemple {id="exemple_1"}
```javascript
api.oauth.createService('MyService', 'https://example.com/callback')
  .then(response => console.log('Service créé :', response))
  .catch(err => console.error('Erreur :', err));
```

---

### `deleteService()`

Supprime un service OAuth existant.

#### Exemple {id="exemple_2"}
```javascript
api.oauth.deleteService()
  .then(response => console.log('Service supprimé'))
  .catch(err => console.error('Erreur :', err));
```

---

### `checkAccessToken(access_token, client_secret)`

Vérifie la validité d'un token d'accès.

#### Paramètres {id="param-tres_2"}
- `access_token` *(string, requis)* : Le token à vérifier.
- `client_secret` *(string, requis)* : Le secret client associé.

#### Exemple {id="exemple_3"}
```javascript
api.oauth.checkAccessToken('myAccessToken', 'myClientSecret')
  .then(isValid => console.log('Token valide :', isValid))
  .catch(err => console.error('Erreur :', err));
```

---

### `patchService(redirectUri, contact, name)`

Met à jour les informations d'un service OAuth existant.

#### Paramètres
- `redirectUri` *(string, optionnel)* : L'URI de redirection mise à jour.
- `contact` *(string, optionnel)* : Le contact associé au service.
- `name` *(string, optionnel)* : Le nouveau nom du service.

#### Exemple
```javascript
api.oauth.patchService('https://new-redirect.com', 'contact@example.com', 'UpdatedService')
  .then(response => console.log('Service mis à jour :', response))
  .catch(err => console.error('Erreur :', err));
```