# Nodejs Expressjs API Project Structure
 ![GitHub repo size](https://img.shields.io/github/repo-size/maitraysuthar/rest-api-nodejs-mongodb) [![Codacy Badge](https://api.codacy.com/project/badge/Coverage/b3eb80984adc4671988ffb22d6ad83df)](https://www.codacy.com/manual/maitraysuthar/rest-api-nodejs-mongodb?utm_source=github.com&utm_medium=referral&utm_content=maitraysuthar/rest-api-nodejs-mongodb&utm_campaign=Badge_Coverage) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/b3eb80984adc4671988ffb22d6ad83df)](https://www.codacy.com/manual/maitraysuthar/rest-api-nodejs-mongodb?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=maitraysuthar/rest-api-nodejs-mongodb&amp;utm_campaign=Badge_Grade)  

Projet prêt à l'emploi pour le développement d'API REST avec Node.js, Express et MongoDB 


## Mise en route


Il s'agit d'un squelette d'API de base écrit en JavaScript ES2015. Très utile pour créer des API Web RESTful pour vos plates-formes frontales telles que les frameworks Android, iOS ou JavaScript (Angular, Reactjs, etc.). 

Ce projet s'exécutera sur ** NodeJs ** en utilisant ** MongoDB ** comme base de données. J'avais essayé de maintenir la structure du code facile car tout débutant peut également adopter le flux et commencer à créer une API. Le projet est ouvert pour les suggestions, les rapports de bogues et les demandes d'extraction. 

## Fonctionnalités
-   Authentication basique (Register/Login avec le hashed password)
-   Account confirmation with 4 (Changeable) digit OTP.
-   Email helper prêt à importer et à utiliser. 
-   Jetons JWT, faites des demandes avec un jeton après la connexion avec l'en-tête `Authorization` avec la valeur` Bearer yourToken` où `yourToken` sera renvoyé dans la réponse de connexion. 
-   Structures de réponse prédéfinies avec codes d'état appropriés. 
-   Included CORS.
-    **Book** example with **CRUD** operations.
-   Validations ajouté.
-   Inclus des API collection for Postman.
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

1.  création du nouveau fichier pour copier et coller le fichier, puis le renommer simplement en `.env` 
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
**Note:**  `YOUR_DB_CONNECTION_STRING` sera votre chaîne de connexion MongoDB .

### Creation de nouveaux models

Si vous avez besoin d'ajouter plus de modèles au projet, créez simplement un nouveau fichier dans `/ models /` et utilisez-les dans les contrôleurs. 

### Creation de nouveaux routes

Si vous avez besoin d'ajouter plus de routes au projet, créez simplement un nouveau fichier dans `/ routes /` et ajoutez-le dans `/ routes / api.js`, il sera chargé dynamiquement. 


