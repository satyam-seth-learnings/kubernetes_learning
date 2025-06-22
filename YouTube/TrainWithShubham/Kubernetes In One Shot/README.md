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

