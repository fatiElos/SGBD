Pré-requis: MYSQL et PHPMYADMIN
Pour utiliser l'interface, il faut suivre les étapes suivantes:

1/ Se connecter à MySql sur le terminale UBUNTU

2/ Créer une base de données avec la ligne de commande suivante:
CREATE DATABASE parking;

3/ On se positionne sur cette base grâce à la commande suivante:
use parking;

4/ Lancer les fichiers de création de la base de données grâce à la commande suivante:
source sql/create.sql;

Remarque: Si ce n'est pas la première fois que vous créez cette base de données,
Il faut d'abord faire la commande suivante:
source sql/drop.sql;

5/ Lancer les fichiers d'insertion des données de tests:
source sql/insert.sql;

6/ Sur le fichier connexion.php dans le répertoire src/, il faut modifier les informations sur cette ligne:
$link = new mysqli("localhost", "root", "1234", "parking");
Les modifications sont les suivantes:
"root" ----> Votre nom d'utilisateur MySql
"1234" ----> Votre mot de passe MYSQL

7/ Il faut copier les fichiers dans le répertoire src dans le répertoire /var/www/html/:
sudo cp src/* /var/www/html/

Remarque: Durant le projet, on a crée un Makefile qui copie le contenu à chaque fois

8/ Sur votre navigateur, tapez localhost dans la barre de recherche et vous avez accès
à l'interface
