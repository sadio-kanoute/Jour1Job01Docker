# Welcome to Docker

This is a repo for new users getting started with Docker.

You can try it out using the following command.

```
docker run -d -p 8088:80 --name welcome-to-docker docker/welcome-to-docker
```

And open `http://localhost:8088` in your browser.

# Building

Maintainers should see [MAINTAINERS.md](MAINTAINERS.md).

Build and run:

```
docker build -t welcome-to-docker .
docker run -d -p 8088:3000 --name welcome-to-docker welcome-to-docker
```

Open `http://localhost:8088` in your browser.

## Captures d'écran

1. Construction de l'image Docker (`docker build -t welcome-to-docker .`)
   ![Build de l'image](image.png)

2. Lancement du conteneur (`docker run -d -p 8088:3000 --name welcome-to-docker welcome-to-docker`)
   ![Conteneur en cours d'exécution](image-1.png)

3. Vérification du conteneur en cours d'exécution (`docker ps`)
   ![Vérification du conteneur](image-2.png)

4. Consultation des logs du conteneur (`docker logs welcome-to-docker`)
   ![Logs du conteneur](image-3.png)

5. Accès au conteneur et navigation (`docker exec -it welcome-to-docker sh`)
   ![Accès au conteneur](image-4.png)

6. Reconstruction de l'image après modification du code (`docker build -t welcome-to-docker .`)
   ![Reconstruction de l'image](image-5.png)

7. Suppression du conteneur existant (`docker rm -f welcome-to-docker`)
   ![Suppression du conteneur](image-6.png)

8. Lancement du nouveau conteneur avec l'image modifiée (`docker run -d -p 8088:3000 --name welcome-to-docker welcome-to-docker`)
   ![Lancement du nouveau conteneur](image-7.png)

9. Vérification que le nouveau conteneur est actif (`docker ps`)
   ![Vérification du nouveau conteneur](image-8.png)

10. Connexion à Docker Hub (`docker login`)
    ![Connexion Docker Hub](image-9.png)

11. Tag de l'image pour Docker Hub (`docker tag welcome-to-docker kanoutesadio/welcome-to-docker:latest`)
    ![Tag de l'image](image-10.png)

12. Publication de l'image sur Docker Hub (`docker push kanoutesadio/welcome-to-docker:latest`)
    ![Publication sur Docker Hub](image-11.png)

13. Vérification de l'application modifiée dans le navigateur (`http://localhost:8088`)
    ![Application modifiée](image-12.png)
