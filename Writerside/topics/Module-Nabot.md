# Module Nabot

<note type="info">Le module **Nabot** de NationsAPI permet de gérer les sessions et d’envoyer des messages en utilisant une instance de bot.</note>

---

## Description

Le module **Nabot** propose une interface pour créer et gérer des sessions de bot ainsi que pour envoyer des messages via celles-ci. Les sessions sont initialisées automatiquement si elles n’existent pas.

---

## Méthodes Disponibles

### `initialize()`

Initialise une session si elle n'est pas encore créée.

#### Exemple {id="exemple_1"}
```javascript
await api.nabot.initialize();
console.log('Session initialisée');
```

---

### `sendMessage(data)`

Envoie un message à l'aide du bot actif.

#### Paramètres {id="param-tres_1"}
- `data` *(string, requis)* : Le message à envoyer.

#### Exemple {id="exemple_2"}
```javascript
api.nabot.sendMessage('Bonjour à tous !')
  .then(response => console.log('Message envoyé :', response))
  .catch(err => console.error('Erreur :', err));
```

---

### `getSessionUid()`

Récupère l'UID de la session active.

#### Exemple {id="exemple_3"}
```javascript
api.nabot.getSessionUid()
  .then(uid => console.log('UID de la session :', uid))
  .catch(err => console.error('Erreur :', err));
```

---

### `setSessionUid(sessionUid)`

Définit manuellement l'UID d'une session existante.

#### Paramètres
- `sessionUid` *(number, requis)* : L'UID de la session.

#### Exemple {id="exemple_4"}
```javascript
api.nabot.setSessionUid(12345);
console.log('UID de session défini.');
```

---

### `createSession()`

Crée une nouvelle session de bot et retourne l'UID associé.

#### Exemple
```javascript
api.nabot.createSession()
  .then(uid => console.log('Nouvelle session créée avec UID :', uid))
  .catch(err => console.error('Erreur :', err));
```
