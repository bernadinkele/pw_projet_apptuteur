# 📘 Projet AppTuteur (Symfony + Docker)

Ce projet contient l'application **AppTuteur**, exécutée à l'aide de
**Docker**, **Symfony**, et **MySQL**.

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

## 🗄️ 4. Base de données : réinitialisation & migrations

Supprimer la base existante :

``` bash
symfony console doctrine:database:drop --force
```

Créer une migration :

``` bash
symfony console make:migration
```

Exécuter les migrations :

``` bash
symfony console doctrine:migrations:migrate
```

## ▶️ 5. **Démarrer le serveur Symfony après les migrations**
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

Se connecter avec l'email et le mot de passe du tuteur créé juste avant.

------------------------------------------------------------------------
### App Preview

|              Home             |            Cart           |             Chat          |
| :----------------------------------: | :----------------------------------: | :----------------------------------: |
| <img src="https://github.com/bernadinkele/pw_projet_apptuteur/blob/main/captures/dashboard_2.png" width="350"> | <img src="https://github.com/bernadinkele/flash_food/blob/main/screenshoots/4.png" width="350"> | <img src="https://github.com/bernadinkele/flash_food/blob/main/screenshoots/5.png" width="350"> |


## 👥 Contributeurs

-   **KELE Berndin**
-   **Yoro**

------------------------------------------------------------------------

## 📄 Licence

Projet réservé à un usage académique / pédagogique.
