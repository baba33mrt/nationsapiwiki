# Module Webhooks

<note type="info">Le module **Webhooks** de NationsAPI permet de gérer des webhooks pour recevoir des notifications en temps réel sur divers événements liés aux nations.</note>

---

## Description

Le module **Webhooks** propose des méthodes pour créer, enregistrer, gérer et supprimer des webhooks, afin de suivre des événements comme la création ou la dissolution de nations, ou le changement de leader.

---

## Méthodes Disponibles

### `createCountry(url)`

Crée un webhook pour suivre les événements de création de nations.

#### Paramètres {id="param-tres_1"}
- `url` *(string, requis)* : L'URL où envoyer les notifications.

#### Exemple {id="exemple_1"}
```javascript
api.webhooks.createCountry('https://example.com/webhook')
  .then(response => console.log('Webhook créé :', response))
  .catch(err => console.error('Erreur :', err));
```

---

### `disbandCountry(url)`

Crée un webhook pour suivre les événements de dissolution de nations.

#### Paramètres {id="param-tres_2"}
- `url` *(string, requis)* : L'URL où envoyer les notifications.

#### Exemple {id="exemple_2"}
```javascript
api.webhooks.disbandCountry('https://example.com/webhook')
  .then(response => console.log('Webhook créé :', response))
  .catch(err => console.error('Erreur :', err));
```

---

### `changeLeader(url)`

Crée un webhook pour suivre les événements de changement de leader d'une nation.

#### Paramètres {id="param-tres_3"}
- `url` *(string, requis)* : L'URL où envoyer les notifications.

#### Exemple {id="exemple_3"}
```javascript
api.webhooks.changeLeader('https://example.com/webhook')
  .then(response => console.log('Webhook créé :', response))
  .catch(err => console.error('Erreur :', err));
```

---

### `getWebhook(webhookId)`

Récupère les détails d'un webhook spécifique.

#### Paramètres {id="param-tres_4"}
- `webhookId` *(number, requis)* : L'identifiant du webhook.

#### Exemple {id="exemple_4"}
```javascript
api.webhooks.getWebhook(12345)
  .then(webhook => console.log('Détails du webhook :', webhook))
  .catch(err => console.error('Erreur :', err));
```

---

### `getAllWebhooks()`

Récupère la liste de tous les webhooks enregistrés.

#### Exemple {id="exemple_5"}
```javascript
api.webhooks.getAllWebhooks()
  .then(webhooks => console.log('Liste des webhooks :', webhooks))
  .catch(err => console.error('Erreur :', err));
```

---

### `removeWebhook(webhookId)`

Supprime un webhook spécifique.

#### Paramètres
- `webhookId` *(number, requis)* : L'identifiant du webhook.

#### Exemple
```javascript
api.webhooks.removeWebhook(12345)
  .then(response => console.log('Webhook supprimé :', response))
  .catch(err => console.error('Erreur :', err));
```
