- Apply namespaces

    ```bash
    kubectl apply -f namespaces.yml
    ```

- Apply deployment

    ```bash
    kubectl apply -f deployment.yml
    ```

- Apply service

    ```bash
    kubectl apply -f service.yml
    ```

- Forward the port

    ```bash
    kubectl port-forward service/notes-app-service -n notes-app 8000:8000 --address=0.0.0.0
    ```
