# Multi Docker Container and Kubernetes

The complex directory has 3 subdirectories; client, server and worker those are the container created on the previusly multi docker container project. Now it is time to create that project in kubernetes. The k8s directory has all the configuration files.

# Kubernetes
To use kubernetes you need to install *kubectl* and if you will run it locally then minikube it is also necessary.

## Kubectl Ubuntu installation
  ```shell
  sudo snap install kubectl --classic
    kubectl version
    kubectl cluster-info
```

if you are intending to run a Kubernetes cluster on your laptop (locally), you will need a tool like minikube to be installed first and then re-run the commands stated above.

If kubectl cluster-info returns the url response but you can’t access your cluster, to check whether it is configured properly, use:
```shell
kubectl cluster-info dump
```
More installation about [Install and Set Up Kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-with-snap-on-ubuntu "Install and Set Up Kubectl"), and to [install minikube](https://kubernetes.io/docs/tasks/tools/install-minikube/ "install minikube")

## Docker compose
There is a docker-compose.yml file to create all the containers in docker, just run the command `docker-compose up` inside the complex directory.

To see all the docker compose containers use the command `docker-compose ps` and to stop all the docker compose containers use the command `docker-compose down`
