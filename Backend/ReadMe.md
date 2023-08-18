# Backend API - Sophie Bluel

Ce repo contient le code backend de l'architecte Sophie Bluel. 

## Lancement du backend

Après avoir récupéré le REPO executez la commande `npm install` pour installer les dépendances du projet

Une fois les dépendances installées lancez le projet avec la commande `npm start`

Compte de test pour Sophie Bluel

```
email: sophie.bluel@test.tld

password: S0phie 
```
Lien pour voir la
[documentation Swagger](http://localhost:5678/api-docs/)

Pour lire la documentation, utiliser Chrome ou Firefox






Carolines-MBP:Backend caroline$ npm install

added 325 packages, and audited 326 packages in 6s

27 packages are looking for funding
  run `npm fund` for details

15 vulnerabilities (7 moderate, 7 high, 1 critical)

To address issues that do not require attention, run:
  npm audit fix

To address all issues possible (including breaking changes), run:
  npm audit fix --force

Some issues need review, and may require choosing
a different dependency.

Run `npm audit` for details.
Carolines-MBP:Backend caroline$ npm start

> dwf-projet6-backend@0.0.1 start
> node server

Listening on port 5678
Executing (default): CREATE TABLE IF NOT EXISTS `users` (`id` INTEGER PRIMARY KEY AUTOINCREMENT, `email` VARCHAR(255) NOT NULL UNIQUE, `password` VARCHAR(255) NOT NULL);
Executing (default): PRAGMA INDEX_LIST(`users`)
Executing (default): PRAGMA INDEX_INFO(`sqlite_autoindex_users_1`)
Executing (default): CREATE TABLE IF NOT EXISTS `categories` (`id` INTEGER PRIMARY KEY AUTOINCREMENT, `name` VARCHAR(255) NOT NULL UNIQUE);
Executing (default): PRAGMA INDEX_LIST(`categories`)
Executing (default): PRAGMA INDEX_INFO(`sqlite_autoindex_categories_1`)
Executing (default): CREATE TABLE IF NOT EXISTS `works` (`id` INTEGER PRIMARY KEY AUTOINCREMENT, `title` VARCHAR(255) NOT NULL, `imageUrl` VARCHAR(255) NOT NULL, `categoryId` INTEGER REFERENCES `categories` (`id`) ON DELETE SET NULL ON UPDATE CASCADE, `userId` INTEGER REFERENCES `users` (`id`) ON DELETE SET NULL ON UPDATE CASCADE);
Executing (default): PRAGMA INDEX_LIST(`works`)
db is ready

