# Nodejs Expressjs API Project Structure
 [![GitHub license](https://img.shields.io/github/license/maitraysuthar/rest-api-nodejs-mongodb.svg)](https://github.com/maitraysuthar/rest-api-nodejs-mongodb/blob/master/LICENSE)  ![GitHub repo size](https://img.shields.io/github/repo-size/maitraysuthar/rest-api-nodejs-mongodb) [![Codacy Badge](https://api.codacy.com/project/badge/Coverage/b3eb80984adc4671988ffb22d6ad83df)](https://www.codacy.com/manual/maitraysuthar/rest-api-nodejs-mongodb?utm_source=github.com&utm_medium=referral&utm_content=maitraysuthar/rest-api-nodejs-mongodb&utm_campaign=Badge_Coverage) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/b3eb80984adc4671988ffb22d6ad83df)](https://www.codacy.com/manual/maitraysuthar/rest-api-nodejs-mongodb?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=maitraysuthar/rest-api-nodejs-mongodb&amp;utm_campaign=Badge_Grade) ![Travis (.com)](https://img.shields.io/travis/com/maitraysuthar/rest-api-nodejs-mongodb)

Projet prêt à l'emploi pour le développement d'API REST avec Node.js, Express et MongoDB 


## Mise en route


Il s'agit d'un squelette d'API de base écrit en JavaScript ES2015. Très utile pour créer des API Web RESTful pour vos plates-formes frontales telles que les frameworks Android, iOS ou JavaScript (Angular, Reactjs, etc.). 

Ce projet s'exécutera sur ** NodeJs ** en utilisant ** MongoDB ** comme base de données. J'avais essayé de maintenir la structure du code facile car tout débutant peut également adopter le flux et commencer à créer une API. Le projet est ouvert pour les suggestions, les rapports de bogues et les demandes d'extraction. 

## Fonctionnalités
-   Basic Authentication (Register/Login with hashed password)
-   Account confirmation with 4 (Changeable) digit OTP.
-   Email helper ready just import and use.
-   JWT Tokens, make requests with a token after login with `Authorization` header with value `Bearer yourToken` where `yourToken` will be returned in Login response.
-   Pre-defined response structures with proper status codes.
-   Included CORS.
-    **Book** example with **CRUD** operations.
-   Validations added.
-   Included API collection for Postman.
-   Light-weight project.
-   Test cases with [Mocha](https://mochajs.org/) and [Chai](https://www.chaijs.com/).
-   Code coverage with [Istanbuljs (nyc)](https://istanbul.js.org/).
-   Included CI (Continuous Integration) with [Travis CI](https://travis-ci.org).
-   Linting with [Eslint](https://eslint.org/).

## Logiciels requis

-   Node.js **10+**
-   MongoDB **3.6+** (Recommended **4+**)

## Comment installer 

### Utilisation du Git (recommended)

1.  Clonage du projet du github. Change "myproject" to your project name.

```bash
git clone https://github.com/hamdi-garfi/starter-app-node-mongo.git ./myproject
```

### Utilisation du téléchargement manuel ZIP 

1.  Télécharger le repository
2.  Décomprésser le dossier

### Installer les dépendances npm après l'installation (Git ou téléchargement manuel) 

```bash
cd myproject
npm install
```

### Setting up environments

1.  Create a new file by copying and pasting the file and then renaming it to just `.env`
    ```bash
    cp .env.example .env
    ```
2.  Le fichier `.env` est déjà ignoré, vous ne validez donc jamais vos informations d'identification.
3. Modifiez les valeurs du fichier en fonction de votre environnement. Commentaires utiles ajoutés au fichier `.env` pour comprendre les constantes. 

## Structure du projet
```sh
.
├── app.js
├── package.json
├── bin
│   └── www
├── controllers
│   ├── AuthController.js
│   └── BookController.js
├── models
│   ├── BookModel.js
│   └── UserModel.js
├── routes
│   ├── api.js
│   ├── auth.js
│   └── book.js
├── middlewares
│   ├── jwt.js
├── helpers
│   ├── apiResponse.js
│   ├── constants.js
│   ├── mailer.js
│   └── utility.js
├── test
│   ├── testConfig.js
│   ├── auth.js
│   └── book.js
└── public
    ├── index.html
    └── stylesheets
        └── style.css
```
 

### Exécuter le serveur d'API localement 

```bash
npm run dev
```

Vous saurez que le serveur est en cours d'exécution en vérifiant la sortie de la commande `npm run dev` 

```bash
Connected to mongodb:YOUR_DB_CONNECTION_STRING
App is running ...

Press CTRL + C to stop the process.
```
**Note:**  `YOUR_DB_CONNECTION_STRING` will be your MongoDB connection string.

### Creating new models

If you need to add more models to the project just create a new file in `/models/` and use them in the controllers.

### Creating new routes

If you need to add more routes to the project just create a new file in `/routes/` and add it in `/routes/api.js` it will be loaded dynamically.


