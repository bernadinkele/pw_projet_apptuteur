# 📘 Projet AppTuteur (Symfony + Docker)

Ce projet contient l'application **AppTuteur**, exécutée à l'aide de
**Docker**, **Symfony**, et **MySQL**.


Cette application permettra à un tuteur : se connecter,se déconnecter,de gérer les étudiants qu’il suit,de planifier des visites,de rédiger un compte-rendu,de visualiser l’historique.

##  Installation du projet
 - Avoir docker installé et allumé
------------------------------------------------------------------------

## 🚀 1. Installation du projet

Cloner le projet principal :

``` bash
git clone https://github.com/bernadinkele/pw_projet_apptuteur.git
```
Acceder au dossier du projet:

``` bash
cd pw_projet_apptuteur
```

Cloner ensuite le projet Symfony dans le dossier :

``` bash
git clone https://github.com/bernadinkele/apptuteur.git
```

------------------------------------------------------------------------

## 🐳 2. Lancer l'environnement Docker

Arrêter tous les conteneurs existants :

``` bash
docker compose down
```

Construire et lancer les conteneurs :

``` bash
docker compose up --build -d
```

(Relancer si nécessaire)

``` bash
docker compose up -d
```

------------------------------------------------------------------------

## 🧰 3. Installation des dépendances Symfony

Entrer dans le conteneur PHP :

``` bash
docker exec -it symfony_app bash
```

Ensuite :

``` bash
cd apptuteur
composer install
```

------------------------------------------------------------------------

## 🗄️ 4. Base de données

Accéder à votre base de données via :

👉 **http://localhost:8081/**


## ▶️ 5. **Démarrer le serveur Symfony **
Exécuter depuis votre machine :
```bash
symfony serve:start
```
------------------------------------------------------------------------

## 🧪 6. Créer un tuteur via l'API

Accéder à l'interface :

👉 **http://localhost:8000/api**

Créer un tuteur via **POST /api/tuteurs** avec au minimum :

``` json
{
    "nom": "Durand",
    "prenom": "Alice",
    "email": "alice.durand@example.com",
    "telephone": "0601020304"
}
```

------------------------------------------------------------------------

## 🔐 7. Connexion à l'espace /login

Accéder à :

👉 **http://localhost:8000/login**

Se connecter avec l'email: alice.durand@example.com et n'importe quel mot de passe (on a pas ajouter de mot de passe)

------------------------------------------------------------------------
### captures des pages

|             DASHBOARD             |           LOGIN         |             VISITES          |
| :----------------------------------: | :----------------------------------: | :----------------------------------: |
| <img src="https://github.com/bernadinkele/pw_projet_apptuteur/blob/main/captures/dashboard_2.png" width="400"> | <img src="https://github.com/bernadinkele/pw_projet_apptuteur/blob/main/captures/login.png" width="400"> | <img src="https://github.com/bernadinkele/pw_projet_apptuteur/blob/main/captures/visites_2.png" width="400"> |

|            ETUDIANTS            |           AJOUT ETUDIANT        |             MODIFICATION ETUDIANT          |
| :----------------------------------: | :----------------------------------: | :----------------------------------: |
| <img src="https://github.com/bernadinkele/pw_projet_apptuteur/blob/main/captures/etudiants.png" width="400"> | <img src="https://github.com/bernadinkele/pw_projet_apptuteur/blob/main/captures/ajout_etudiant.png" width="400"> | <img src="https://github.com/bernadinkele/pw_projet_apptuteur/blob/main/captures/modif_etudiant.png" width="400"> |

|            AJOUT VISITE           |           AJOUT ETUDIANT        |             Dashboard          |
| :----------------------------------: | :----------------------------------: | :----------------------------------: |
| <img src="https://github.com/bernadinkele/pw_projet_apptuteur/blob/main/captures/ajouter_visites.png" width="400"> | <img src="https://github.com/bernadinkele/pw_projet_apptuteur/blob/main/captures/ajout_etudiant.png" width="400"> | <img src="https://github.com/bernadinkele/pw_projet_apptuteur/blob/main/captures/Capture%20d'%C3%A9cran%202025-12-11%20142528.png" width="400"> |


## 👥 Contributeurs

-   **KELE Berndin**
-   **MAMADOU YERO SALL**

------------------------------------------------------------------------

## 📄 Licence

Projet réservé à un usage académique / pédagogique.
