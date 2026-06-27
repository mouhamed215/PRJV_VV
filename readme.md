# Projet Java - Gestion des utilisateurs

Ce projet Java gère des utilisateurs avec un modèle, un DAO, un service et une application console.

## Base de données MySQL

1. Démarrez MySQL ou XAMPP.
2. Ouvrez `phpMyAdmin` ou un terminal MySQL.
3. Exécutez le script SQL : `database/create_userdb.sql`.

## Configuration de la base de données

Le fichier `src/main/java/com/example/usermanagement/util/DatabaseConnection.java` utilise les paramètres suivants :

- URL : `jdbc:mysql://localhost:3306/userdb?useSSL=false&serverTimezone=UTC`
- Utilisateur : `root`
- Mot de passe : `` (vide)

> Adaptez ces valeurs si votre installation MySQL utilise d'autres identifiants.

## Structure du projet

- `src/main/java/com/example/usermanagement/model` : classe `User`
- `src/main/java/com/example/usermanagement/dao` : interface `UserDao` et implémentation `UserDaoImpl`
- `src/main/java/com/example/usermanagement/service` : interface `UserService` et implémentation `UserServiceImpl`
- `src/main/java/com/example/usermanagement/app` : classe principale `Main`
- `src/main/java/com/example/usermanagement/util` : connexion à la base de données

## Commandes Maven

- Construire le projet : `mvn compile`
- Exécuter l'application : `mvn exec:java`

## Fonctionnalités

- Lister tous les utilisateurs
- Ajouter un utilisateur
- Modifier un utilisateur
- Supprimer un utilisateur
- Rechercher les utilisateurs par nom ou prénom
- Authentifier un utilisateur par login et mot de passe
