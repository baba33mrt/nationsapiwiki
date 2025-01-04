# Module NgIsland

<note type="info">Le module **NgIsland** de NationsAPI permet de récupérer des informations sur les îles disponibles dans un serveur de NationsGlory.</note>

---

## Description

Le module **NgIsland** propose une méthode pour lister toutes les îles disponibles avec la possibilité de paginer les résultats.

---

## Méthodes Disponibles

### `getAllIslands(page)`

Récupère la liste des îles avec une pagination optionnelle.

#### Paramètres
- `page` *(number, optionnel)* : Le numéro de la page à récupérer (par défaut : `1`).

#### Exemple
```javascript
api.ngisland.getAllIslands(1)
  .then(islands => console.log('Liste des îles :', islands))
  .catch(err => console.error('Erreur :', err));
```
