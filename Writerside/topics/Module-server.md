# Module Server

<note type="info">Le module **Server** de NationsAPI permet d'interagir avec les serveurs de NationsGlory pour récupérer des informations comme le planning, le nombre de joueurs connectés, ou les détails des hôtels de vente (HDV).</note>

---

## Description

Le module **Server** regroupe des méthodes pour interagir avec des données spécifiques aux serveurs, offrant des fonctionnalités utiles pour les administrateurs et les joueurs.

---

## Méthodes Disponibles

### `getPlanning(server, month, year)`

Récupère le planning d'un serveur pour un mois et une année spécifiques.

#### Paramètres
- `server` *(string, requis)* : Le nom du serveur.
- `month` *(number, optionnel)* : Le mois (1-12).
- `year` *(number, optionnel)* : L'année.

#### Exemple
```javascript
api.server.getPlanning('Server1', 1, 2025)
  .then(planning => console.log('Planning :', planning))
  .catch(err => console.error('Erreur :', err));
```

---

### `getPlayersCount()`

Récupère le nombre de joueurs actuellement connectés sur le serveur.

#### Exemple {id="exemple_2"}
```javascript
api.server.getPlayersCount()
  .then(count => console.log('Nombre de joueurs connectés :', count))
  .catch(err => console.error('Erreur :', err));
```

---

### `getHDV(server)`

Récupère les informations sur les hôtels de vente (HDV) d'un serveur spécifique.

#### Paramètres {id="param-tres_1"}
- `server` *(string, requis)* : Le nom du serveur.

#### Exemple {id="exemple_1"}
```javascript
api.server.getHDV('Server1')
  .then(hdv => console.log('Hôtel de vente :', hdv))
  .catch(err => console.error('Erreur :', err));
```