# Module NabotInstance

<note type="info">Le module **NabotInstance** de NationsAPI permet de gérer des instances dédiées de bots en héritant des fonctionnalités du module **Nabot**.</note>

---

## Description

Le module **NabotInstance** est une classe générée dynamiquement à partir du module **Nabot**. Elle est conçue pour gérer des sessions spécifiques de bots, tout en permettant une initialisation automatique des sessions.

<p>Ce module hérite de toutes les méthodes disponibles dans le module **Nabot**. Consultez la <a href="Module-Nabot.md">Documentation</a> plus de détails.</p>

---

## Méthodes Disponibles

Les méthodes du module **NabotInstance** incluent toutes les fonctionnalités de la classe **Nabot**, notamment :

- `initialize()` : Initialise automatiquement une session si elle n'existe pas.
- `sendMessage(data)` : Envoie un message via le bot actif.
- `getSessionUid()` : Récupère l'UID de la session active.
- `setSessionUid(sessionUid)` : Définit l'UID d'une session existante.
- `createSession()` : Crée une nouvelle session de bot.

<p>Pour plus d'informations sur ces méthodes, veuillez consulter la <a href="Module-Nabot.md">Documentation</a> .</p>

---

## Exemple d’Utilisation

Voici un exemple montrant comment utiliser une instance de bot dédiée avec **NabotInstance** :

```javascript
const NationsAPI = require('nationsapi');
const api = new NationsAPI('VOTRE_API_TOKEN');

const nabotInstance = new api.nabotInstance();

nabotInstance.sendMessage('Bonjour tout le monde !')
  .then(response => console.log('Message envoyé :', response))
  .catch(err => console.error('Erreur :', err));
```
