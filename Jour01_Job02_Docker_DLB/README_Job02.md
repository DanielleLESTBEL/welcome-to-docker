# Jour1_Job02_Docker_DLB
Welcome to Docker - Part 2 // Cas pratique
--------------------------------------------
**1)** Ouverture de Visual studio, du dossier DOCKER puis du Terminal depuis lequel je vais travailler.  
![openVSCode_ _terminal_01](https://github.com/user-attachments/assets/c0216f85-892f-40f2-8b21-e21d77f24830)


**2)** Créer l’image docker (à récupérer depuis https://github.com/docker/welcome-to-docker). Il faut que le fichier dockerfile soit pris en compte.

**3)** Lancer l’image docker que vous venez de créer puis lancer un container (avec cette image).

**4)** Vérifiez que le container est bien lancé. Exécutez d’autres commandes de bases, faites dans le Job01 (Jour01).

**5)** Accéder au container pour visualiser le résultat.

**6)** Retournez dans Visual Studio et coder quelques lignes dans votre projet.

**7)** Vérifiez le résultat faites en sorte que vos modifications soient prises en compte dans votre image docker et votre container.

**8)** Comprenez ce qu’il faut faire pour que ce soit pris en compte.

**9)** Publier sur votre compte docker une image docker, et rendez-la disponible à un membre de votre promo.

**10)** Récupérer une image docker d’un membre de votre promo et refaire les tests et modifications sur celle-ci (citez l’auteur
de l’image d’origine dans la page).

**11)** Publier sur votre Docker l’image modifié du membre de votre promo.



## **Commandes de base :**

**1)** docker --version \
![docker --version_Jour1_exo01_cmd01](https://github.com/user-attachments/assets/73216fc3-534e-447b-b722-fb86ab497f83)

**2)** docker info \
![docker info_Jour01_exo01_cmd02a](https://github.com/user-attachments/assets/28a1fa64-a82f-4301-bee6-099e11d9aa27)
![docker info_Jour01_exo01_cmd02b](https://github.com/user-attachments/assets/2fd296df-6429-44ae-99ef-51fe30b21886)
![docker info_Jour01_exo01_cmd02c](https://github.com/user-attachments/assets/279f0860-503b-4c26-b918-a3715401394f)


**3)** docker ps \
![docker ps_Jour01_exo01_cmd03](https://github.com/user-attachments/assets/c9db6d9e-6639-4707-8f5a-c61126a97106)


**4)** docker images \
![docker images_Jour01_exo01_cmd04](https://github.com/user-attachments/assets/1b56ea8c-1c30-45eb-91e2-44e29c3f23da)


**5)** docker run \
![docker run_Jour01_exo01_cmd05](https://github.com/user-attachments/assets/dbfd2801-6cf3-445a-a7dd-7e36c0a18350)


**6)** docker stop \
![docker stop_Jour01_exo01_cmd06a](https://github.com/user-attachments/assets/050eea0e-f200-4052-b1ba-d74d60748718)
![docker stop_Jour01_exo01_cmd06b](https://github.com/user-attachments/assets/b7249016-3321-4fd5-886b-03d2ddbbfe1f)

--------------------------------------------
--------------------------------------------
## **Récupérer l’image Docker**

**7)** docker pull \
![docker pull_Jour01_exo01_cmd07a](https://github.com/user-attachments/assets/37aea537-9b43-4ef8-878a-1153424aea8f)
![docker pull_Jour01_exo01_cmd07b](https://github.com/user-attachments/assets/3e953dc5-f9a9-4827-b91b-61ad8a344800)


**8)** docker images \
![docker images_Jour01_exo01_cmd08](https://github.com/user-attachments/assets/7b2910de-89fb-439c-8fbd-981cb092b615)

--------------------------------------------
--------------------------------------------
## **Construisez le container Docker**

**9)** docker run -it --rm -p xxxx:80 “nom de l'image”   [Remplacer xxxx par un port valide comme **8080**]  

![docker pull   images_Jour01_exo01_cmd09](https://github.com/user-attachments/assets/f2f90188-db9d-4f2d-a6ee-773781658df7)

![docker run_Jour01_exo01_cmd09(fonctionnel)a](https://github.com/user-attachments/assets/09f962cb-3d46-42fb-bbcc-be947148bf2f)

![docker run_Jour01_exo01_cmd09(fonctionnel)b](https://github.com/user-attachments/assets/3b946439-ffe7-440a-898e-53ca698c54ea)

![docker run_Jour01_exo01_cmd09(fonctionnel)c](https://github.com/user-attachments/assets/cd701f69-99db-411e-a213-d331c34b9014)

Eteindre Laragon s'il est ouvert. \
![Le container fonctionne_cmd09](https://github.com/user-attachments/assets/27c8010d-e697-4e21-8405-a9cf18ec78e4)

Vérification dans un navigateur : \
![Congrats first container](https://github.com/user-attachments/assets/34871e5b-0e08-42f0-9ebe-1d6500513764)


--------------------------------------------
--------------------------------------------
## **Arrêter le container**

**10)** docker stop 78532aeefb3e (78532aeefb3e = id du container) \
![image](https://github.com/user-attachments/assets/0d6e57b3-2092-47c3-b419-930baddbc5c6)

![Arrêt du container_cmd10](https://github.com/user-attachments/assets/75e7ab50-4a3c-4f77-a15a-29d7fe656e8c)


--------------------------------------------
--------------------------------------------
## **Supprimer le container**

**11)** docker rm <nom du container> // ATTENTION si container créé avec l'entrée -rm ALORS LE CONTAINER EST SUPPRIME DIRECTEMENT DES FERMETURE DU TERMINAL OU ARRET DU CONTAINER.   

![Suppression du container_cmd11](https://github.com/user-attachments/assets/97807960-1336-4cae-9fd7-5ad2b2385e63)

--------------------------------------------
--------------------------------------------
## **Supprimer une image Docker**

**12)** docker rmi <nom de l'image OU n° id de l'image>

--------------------------------------------
--------------------------------------------
## **Donner un exemple de ligne de commande pour ces actions pour supprimer :**

**13)** Un conteneur spécifique   
docker rm <id/nom du container>

**14)** Plusieurs conteneurs
docker rm container1 container2

**15)** Tous les conteneurs arrêtés
docker container prune

**16)** Forcer la suppression d'un conteneur actif : 
docker container prune -f

**17)** Une image spécifique : 
docker rmi <id : nom de l'image>

**18)** Plusieurs images :
docker rmi image1 image2

**19)** Toutes les images inutilisées :
docker image prune

**20)** Toutes les images non utilisées :
docker image prune -a

**21)** Forcer la suppression d'une image :
docker rmi -f <id : nom de l'image>

**22)** Quelle erreur est présente dans les commandes données ci-dessus, donner la correction :
Une faute d'orthographe peut-être ? "Quel erreur" doit être corrigé en "quelle erreur".



