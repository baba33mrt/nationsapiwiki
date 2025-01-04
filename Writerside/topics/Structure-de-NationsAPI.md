# Structure de NationsAPI

<note type="info">Cette page décrit la structure modulaire de **NationsAPI**, organisée en catégories logiques pour simplifier l’interaction avec l’API de NationsGlory.</note>

---

## Vue d’ensemble

**NationsAPI** est organisée en plusieurs modules, chacun regroupant des méthodes spécifiques pour traiter un type particulier de données ou effectuer des actions ciblées. Cette structure modulaire permet de maintenir une clarté et une logique dans l’utilisation de la bibliothèque.

Voici un aperçu des principaux modules de **NationsAPI** :

```
NationsAPI
├── oauth           // Méthodes pour l'authentification OAuth
├── server          // Méthodes pour interagir avec les serveurs
├── country         // Méthodes pour gérer les pays (nations)
├── user            // Méthodes pour manipuler les données des joueurs
├── ngisland        // Méthodes spécifiques à NgIsland
├── nabot           // Méthodes pour créer une instance Nabit préconfigurée
├── nabotInstance   // Méthodes pour gérer les instances de Nabot
└── webhooks        // Méthodes pour configurer et gérer les webhooks
```

---

## Modules Disponibles

### **oauth**
Permet la gestion des authentifications OAuth.

### **server**
Regroupe les méthodes permettant de récupérer les informationsdes serveurs.

### **country**
Regroupe les méthodes permettant de récupérer les informations des pays.

### **user**
Regroupe les méthodes permettant de récupérer les informations des joueurs.

### **ngisland**
Regroupe les méthodes permettant de récupérer les informations des îles de NgIsland.

### **nabot**
Permet de créer une instance de Nabot préconfigurée.

### **nabotInstance**
Permet de gérer les instances de Nabot.

### **webhooks**
Permet la configuration et la gestion des webhooks pour recevoir des notifications en temps réel.

