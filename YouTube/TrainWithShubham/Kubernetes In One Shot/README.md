- [YouTube Video Link](https://www.youtube.com/@TrainWithShubham)

# KIND Cluster Setup on Ubuntu Server

- [Kind Installation](https://github.com/LondheShubham153/kubestarter/tree/main/kind-cluster)

- SSH ubuntu server with the following command:

  ```bash
  ssh -i <ssh-key-path> ubuntu@<server-public-ip>
  ```

- Update the ubuntu server:

  ```bash
  sudo apt-get update
  ```

- Install Docker on the ubuntu server:

  ```bash
  sudo apt-get install docker.io
  ```

- Check current user:

  ```bash
  whoami
  ```

- Add the current user to the docker group:

  ```bash
  sudo usermod -aG docker $USER
  ```

- Refresh the group:

  ```bash
  newgrp docker
  ```

- Check docker version:

  ```bash
  docker --version
  ```

- Check kubernetes version:

  ```bash
  kubectl version
  ```

- Check kind version:

  ```bash
  kind --version
  ```

- Create a kind cluster with the following command

  ```bash
  kind create cluster --name <cluster-name> --config <kind-config-file>
  ```

- Check the kind cluster:

  ```bash
  kubectl cluster-info --context kind-<cluster-name>
  ```

- Check the nodes in the kind cluster:

  ```bash
  kubectl get nodes
  ```

- Delete the kind cluster with the following command:

  ```bash
  kind delete cluster --name <cluster-name>
  ```

# MINIKUBE Cluster Setup on Ubuntu Server

- [Minikube Installation](https://github.com/LondheShubham153/kubestarter/blob/main/minikube_installation.md)

- SSH ubuntu server with the following command:

  ```bash
  ssh -i <ssh-key-path> ubuntu@<server-public-ip>
  ```

- Update the ubuntu server:

  ```bash
  sudo apt-get update
  ```

- Install Required Packages

  ```bash
  sudo apt install -y curl wget apt-transport-https
  ```

- Install Docker on the ubuntu server:

  ```bash
  sudo apt-get install docker.io
  ```

- Check current user:

  ```bash
  whoami
  ```

- Add the current user to the docker group:

  ```bash
  sudo usermod -aG docker $USER
  ```

- Refresh the group:

  ```bash
  newgrp docker
  ```

- Check docker version:

  ```bash
  docker --version
  ```

- Enable the Docker service to start on boot:

  ```bash
  sudo systemctl enable --now docker
  ```

- Install Minikube on the ubuntu server:

  ```bash
  curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
  ```

- Make the Minikube binary executable:

  ```bash
  chmod +x minikube
  ```

- Move the Minikube binary to a directory in your PATH 

  ```bash
  sudo mv minikube /usr/local/bin/
  ```

- Check Minikube version:

  ```bash
  minikube version
  ```

- Install kubectl on the ubuntu server:

  ```bash
  curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
  ```

- Make the kubectl binary executable:

  ```bash
  chmod +x kubectl
  ```

- Move the kubectl binary to a directory in your PATH:

  ```bash
  sudo mv kubectl /usr/local/bin/
  ```

- Start Minikube with the Docker driver:

  ```bash
  minikube start --driver=docker --vm=true
  ```

- Check nodes in the Minikube cluster:

  ```bash
  kubectl get nodes
  ```

- Stop Minikube cluster:

  ```bash
  minikube stop
  ```

- Delete Minikube cluster:

  ```bash
  minikube delete
  ```

# Kubeadm Cluster Setup on Ubuntu Server

- [Kubeadm Installation](https://github.com/LondheShubham153/kubestarter/tree/main/Kubeadm_Installation_Scripts_and_Documentation)

# K8s Management

- List kubernetes namespaces:

  ```bash
  kubectl get namespaces
  ```

  Or 

  ```bash
  kubectl get ns
  ```

- List kubernetes pods

  ```bash
  kubectl get pods
  ```

- List kubernetes pods in a specific namespace:

  ```bash   
  kubectl get pods -n <namespace>
  ```

- List kubernetes pods with wide output:

  ```bash
  kubectl get pods -o wide -n <namespace>
  ```

- List kubernetes pods in all namespaces:

  ```bash
  kubectl get pods --all-namespaces
  ```

- Create a kubernetes namespace:

  ```bash
  kubectl create namespace <namespace-name>
  ```

  Or

  ```bash
  kubectl create ns <namespace-name>
  ```

- Delete a kubernetes namespace:

  ```bash
  kubectl delete namespace <namespace-name>
  ```

  Or
  
  ```bash
  kubectl delete ns <namespace-name>
  ```

- Run a kubernetes pod:

  ```bash
  kubectl run <pod-name> --image=<image-name>
  ```

- Run a kubernetes pod in a specific namespace:

  ```bash
  kubectl run <pod-name> --image=<image-name> -n <namespace>
  ```

- Delete a kubernetes pod:

  ```bash
  kubectl delete pod <pod-name>
  ```

- Apply a kubernetes configuration file

  ```bash
  kubectl apply -f <yaml-file>
  ```

- Delete a kubernetes resource using a configuration file:

  ```bash
  kubectl delete -f <yaml-file>
  ```

- Enter into a kubernetes pod:

  ```bash
  kubectl exec -it <pod-name> -n <namespace> --bash
  ```

- Describe a kubernetes pod:

  ```bash
  kubectl describe pod <pod-name> -n <namespace>
  ```

- List kubernetes deployments in a specific namespace:

  ```bash
  kubectl get deployment -n <namespace>
  ```

- Scale a kubernetes deployment:

  ```bash
  kubectl scale deployment/<deployment-name> -n <namespace> --replicas=<replica-count>
  ```

- Update a kubernetes deployment image:

  ```bash
  kubectl set image deployment/<deployment-name> -n <namespace> <container-name>=<new-image>
  ```

- List kubernetes replicasets in a specific namespace:

  ```bash
  kubectl get replicasets -n <namespace>
  ```

  Or

  ```bash
  kubectl get rs -n <namespace>
  ```

- List kubernetes daemonsets in a specific namespace:

  ```bash
  kubectl get daemonsets -n <namespace>
  ```

  Or

  ```bash
  kubectl get ds -n <namespace>
  ```
