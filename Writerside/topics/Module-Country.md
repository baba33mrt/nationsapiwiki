# Module Country

<note type="info">Le module **Country** de NationsAPI permet d’interagir avec les informations des nations dans un serveur de NationsGlory, y compris les notations hebdomadaires et les détails des pays.</note>

---

## Description

Le module **Country** offre des méthodes pour récupérer des informations détaillées sur les nations, les notations hebdomadaires et pour convertir les drapeaux des pays en format binaire.

---

## Méthodes Disponibles

### `getNotations({ server, week, country })`

Récupère les notations hebdomadaires pour une nation donnée sur un serveur.

#### Paramètres {id="param-tres_1"}
- `server` *(string, requis)* : Le nom du serveur.
- `week` *(number, optionnel)* : La semaine pour laquelle récupérer les notations (par défaut, la semaine précédente).
- `country` *(string, optionnel)* : Le nom de la nation (par défaut, toutes les nations).

#### Exemple {id="exemple_1"}
```javascript
api.country.getNotations({ server: 'Server1', week: 10, country: 'France' })
  .then(notations => console.log('Notations :', notations))
  .catch(err => console.error('Erreur :', err));
```

---

### `get(server, country)`

Récupère les informations détaillées d’une nation spécifique sur un serveur donné.

#### Paramètres {id="param-tres_2"}
- `server` *(string, requis)* : Le nom du serveur.
- `country` *(string, requis)* : Le nom de la nation.

#### Exemple {id="exemple_2"}
```javascript
api.country.get('Server1', 'France')
  .then(countryInfo => console.log('Informations sur le pays :', countryInfo))
  .catch(err => console.error('Erreur :', err));
```

---

### `convertFlagToBuffer(flag)`

Convertit une image de drapeau encodée en base64 en un format binaire (buffer).

#### Paramètres {id="param-tres_3"}
- `flag` *(string, requis)* : Le drapeau encodé en base64.

#### Exemple {id="exemple_3"}
```javascript
const base64Flag = 'data:image/png;base64,...';
const buffer = api.country.convertFlagToBuffer(base64Flag);
console.log('Buffer du drapeau :', buffer);
```
