# Installation

<note type="info">Cette page explique comment installer et configurer <b> NationsApi</b> dans votre projet Node.js.</note>

---

## Prérequis

<p>Avant d’installer <b>NationsAPI</b>, assurez-vous que les éléments suivants sont en place :</p>

- **Node.js** (version 14 ou supérieure) installé sur votre machine.
- Un gestionnaire de paquets comme **npm** (fourni avec Node.js) ou **yarn**.
- Un accès à un token API valide fourni par **NationsGlory**.

---

## Installation via npm

Pour ajouter **NationsAPI** à votre projet, exécutez simplement la commande suivante dans votre terminal :

```bash
npm install @baba33mrt/nationsapi@latest
```

### Vérification de l’installation

Une fois installé, vous pouvez vérifier que **NationsAPI** est bien ajouté à votre projet en consultant votre fichier `package.json` ou en exécutant :

```bash
npm list nationsapi
```

---

## Installation via yarn

Si vous utilisez **yarn**, vous pouvez installer la bibliothèque avec la commande suivante :

```bash
yarn add nationsapi
```

---

## Configuration Initiale

Après l’installation, configurez **NationsAPI** dans votre projet :

### Importation de la bibliothèque

Ajoutez **NationsAPI** à votre fichier de projet principal :

```javascript
const NationsAPI = require('nationsapi');
```

### Initialisation de l’API

Créez une instance de **NationsAPI** avec votre token API personnel :

```javascript
const api = new NationsAPI('VOTRE_TOKEN_API');
```

---

## Mise à Jour

Pour mettre à jour **NationsAPI** vers la dernière version, utilisez :

### Avec npm

```bash
npm update nationsapi
```

### Avec yarn

```bash
yarn upgrade nationsapi
```

---
<note type="tip">Si vous avez des questions ou des problèmes, consultez la <a href="https://publicapi.nationsglory.fr/">documentation officielle de NationsGlory</a> ou ouvrez une issue sur notre <a href="https://github.com/baba33mrt/NationsAPI/issues">dépôt GitHub</a>.</note>

