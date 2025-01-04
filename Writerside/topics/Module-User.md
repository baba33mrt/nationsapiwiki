# Module User

<note type="info">Le module **User** de NationsAPI permet de récupérer des informations sur un utilisateur spécifique dans un serveur de NationsGlory.</note>

---

## Description

Le module **User** propose une méthode simple pour obtenir les détails d’un utilisateur à partir de son nom d’utilisateur.

---

## Méthodes Disponibles

### `get(username)`

Récupère les informations d’un utilisateur spécifique.

#### Paramètres
- `username` *(string, requis)* : Le nom d’utilisateur.

#### Exemple
```javascript
api.user.get('PlayerName')
  .then(userInfo => console.log('Informations sur l’utilisateur :', userInfo))
  .catch(err => console.error('Erreur :', err));
```
