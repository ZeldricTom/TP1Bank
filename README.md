# BankETS - Système bancaire client-serveur

## Vue d'ensemble

Ce projet fait partie du cours INF111 - Programmation orientée objet à l'ÉTS. Il consiste à développer un système bancaire simple en utilisant une architecture client-serveur. Le système permet aux utilisateurs de créer des comptes bancaires, de gérer des économies, et d'effectuer des transactions basiques.

### Structure du projet

Le projet est divisé en deux parties :
- **TP1** : Implémentation en mode console de la logique bancaire côté serveur, y compris la gestion des comptes bancaires et le traitement des commandes client via une connexion socket.
- **TP2** : Introduction d'une interface graphique et ajout de fonctionnalités supplémentaires.

## Prérequis

- [IntelliJ IDEA](https://www.jetbrains.com/idea/download/) ou tout autre IDE Java
- [Git](https://git-scm.com/downloads)
- Java 8 ou supérieur

## Installation

1. Cloner le dépôt :
    ```bash
    git clone https://github.com/votre-utilisateur/TP1Bank.git
    cd TP1Bank
    ```

2. Ouvrir le projet dans IntelliJ IDEA.
3. Compiler le projet pour installer les dépendances et compiler le code.

### Lancer le serveur

Pour démarrer le serveur :
1. Ouvrir le projet `BankServer`.
2. Exécuter le fichier `Main.java` dans le module `BankServer`.
3. Le serveur écoutera les connexions sur le port `8888`.

### Lancer le client

Pour démarrer un client :
1. Ouvrir le projet `BankClient`.
2. Exécuter le fichier `Main.java` dans le module `BankClient`.
3. Le client affichera des invites pour entrer des commandes afin d'interagir avec le serveur.

### Fonctionnalités

- **Création de comptes** : Créer un nouveau compte bancaire avec un identifiant unique et un NIP.
- **Compte épargne** : Ajouter des fonctionnalités de compte épargne avec des taux d'intérêt fixes.
- **Sélection de comptes** : Basculer entre un compte-chèque et un compte épargne pour les opérations.
- **Multithreading** : Le serveur supporte plusieurs connexions simultanées de clients.
- **Interface par commande** : Le client envoie des commandes au serveur (ex. `NOUVEAU`, `DEPOT`, `RETRAIT`, `HIST`) pour gérer les comptes et effectuer des transactions.

### Commandes

- `NOUVEAU <compte>:<nip>` : Créer un nouveau compte.
- `CONNECT <compte>:<nip>` : Se connecter à un compte existant.
- `DEPOT <montant>` : Déposer de l'argent sur le compte sélectionné.
- `RETRAIT <montant>` : Retirer de l'argent du compte sélectionné.
- `SELECT <cheque|epargne>` : Sélectionner entre le compte-chèque et le compte épargne.
- `HIST` : Consulter l'historique des transactions du compte sélectionné.
- `EXIT` : Se déconnecter du serveur.

### Multithreading & Concurrence

- Le serveur utilise le multithreading pour gérer plusieurs connexions de clients simultanément.
- Les sessions inactives sont automatiquement fermées après 30 secondes d'inactivité.

## Licence

Ce projet est sous licence MIT.
