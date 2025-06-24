- Build the docker image

    ```bash
    docker build -t <username>/notes-app-k8s:latest .
    ```

- Login to docker hub

    ```bash
    docker login -u <username> -p <password>
    ```

- Push the docker image to docker hub

    ```bash
    docker push <username>/notes-app-k8s:latest
    ```

