# Jour1_Job03_Docker_DLB
Welcome to Docker - Part 3 // Jouer avec Super Mario
--------------------------------------------
#### **1)** Récupération de l'image “pengbai/supermario” depuis le Docker Desktop :    

Dans la barre de recherche du Desktop, écrire ou coller le nom de l'image à chercher et cliquer sur le bouton "pull" pour la récupérer dans mon Desktop.  

L'image est maintenant présente dans mon Docker Desktop.  

![alt text](Screenshots/job03_search_mario_pengbai_docker_step01.png)  
![alt text](Screenshots/job03_search_mario_pengbai_docker_step02.png)  

J'aurais également pu récupérer l'image depuis le Terminal de VSCode avec la commande :  

docker pull pengbai/docker-supermario  



#### **2)** Lancer un container avec cette image et lui assigner le port 8600 (en considérant que l’image est configurée sur le port 8080 et en conservant l'accès à l’invite de commande).  

* Etape 1 : Ouvrir VSCode et taper les commandes suivantes dans le Terminal.  

__Commande *pour travailler dans le dossier correspondant à l'exercice*__ :
cd Jour01_Job03_Docker_DLB  




__Commande *pour ouvrir (connecter) mon docker depuis VSCode*__ : 
docker login  

![alt text](Screenshots/job03_docker_login_vsc_step04.PNG)

* Lancer l'image dans un container. Trouver les deux méthodes **avec des ports différents** pour le faire (invite de commande et ???). 

Méthode 1 :  
Je vais d'abord utiliser l'invite de commande et nommer le container **mario-container**. Je vais le faire fonctionner sur le port 8600:8080.
Je vais ensuite vérifier que le container est activé. 

Commandes :  
docker run -d -p8600:8080 --name mario-container pengbai/docker-supermario  
*puis*  
docker ps  


* Quand la commande est validée, observer ce qui s’est passé dans votre fenêtre au-dessus.  


Méthode 2 :
Je passe par le Docker Desktop pour effectuer toutes les opérations.


* Lancer une autre image de super mario sur un port différent.  


Ouvrir votre explorateur et trouver le moyen d’accéder au container
construit
● Accéder et jouer un peu dans votre explorateur internet (faites des
captures du jeux en cours “3 au moins”)

retourner dans le terminal de docker desktop
● Arrêter votre container par son ID (2 manière de trouver l’ID)
● observer quand vous avez validé votre commande ce qui c’est
passé dans votre fenêtre au dessus

● Supprimer le container (2 manières)
● observer quand vous avez validé votre commande ce qui c’est
passé dans votre fenêtre au dessus

● Placez vous sur le menu à gauche dans images
● supprimer l’image docker de super mario (2 manières)
● observer quand vous avez validé votre commande ce qui c’est
passé dans votre fenêtre au dessus