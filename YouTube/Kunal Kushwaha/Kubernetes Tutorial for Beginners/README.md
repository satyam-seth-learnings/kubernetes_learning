- [YouTube Video Link](https://youtu.be/KVBON1lA9N8?si=UR_0OuOCc5PJpuC1)

- [Blog](https://www.techwithkunal.com/blog/getting-started-with-kubernetes)

- [Notes](https://github.com/kunal-kushwaha/DevOps-Bootcamp/blob/main/Kubernetes/Kubernetes%20-%201.pdf)

- Start [minikube](https://minikube.sigs.k8s.io/docs/)

    ```sh
    minikube start
    ```

- Check [minikube](https://minikube.sigs.k8s.io/docs/) status

    ```sh
    minikube status
    ```

- Get pods status

    ```sh
    kubectl get pods
    ```

- Get all info

    ```sh
    kubectl get all
    ```

- Access kubernetes dashboard

    ```sh
    minikube dashboard
    ``` 

- Check docker environment variables

    ```sh
    minikube docker-env
    ```

- List docker containers

    ```sh
    docker container ls
    ```

- SSH in minikube

    ```sh
    minikube ssh
    ```

- List running docker contaienrs
    
    ```sh
    docker ps
    ```

- Check k8s config

    ```sh
    kubectl config view
    ```

- Check k8s current context

    ```sh
    kubectl config current-context
    ```

- Delete a pod

    ```sh
    kubectl delete pod <pod-name>
    ```

- List all deployements

    ```sh
    kubectl get deployments
    ```

- Delete a deployment

    ```sh
    kubectl delete deployments <deployment-name>
    ```

- Create pod from a file

    ```sh
    kubectl create -f pod.yaml
    ```
