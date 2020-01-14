# Kubernetes

<img src="https://github.com/kubernetes/kubernetes/raw/master/logo/logo.png" width="100">

----

O Kubernetes (K8s ou kube) é um sistema de código aberto para automatizar a implantação, dimensionamento e gerenciamento de aplicativos em contêiner. Ele agrupa contêineres que compõem um aplicativo em unidades lógicas para facilitar o gerenciamento e a descoberta

----

## Para começar a usar o Kubernetes

Aprenda sobre os [conceitos básicos do kubernetes](https://www.slideshare.net/AndrStraube/docker-kubernetes-devops)

Leia a documentação [kubernetes.io](kubernetes.io)

Veja o [tutorial interativo](https://kubernetes.io/docs/tutorials/kubernetes-basics/)

Faça um curso gratuito sobre [microsserviços escaláveis ​​com o Kubernetes](https://www.udacity.com/course/scalable-microservices-with-kubernetes--ud615)

# kubernetes + NodeJs
Este projeto é um exemplo prático de orquestração de containers com [Kubernetes](https://kubernetes.io/) para projetos em [NodeJs](https://nodejs.org).

# Etapas para conectar no cluster k82
### Obter credenciais do cluster k82
* GCP
```
gcloud container clusters get-credentials [cluster-name] --zone [zone] --project [project]
```
* GCP Datatalks test
```
gcloud container clusters get-credentials standard-cluster-1 --zone us-central1-a --project datatalks-265115
```
* Azure
```
az aks get-credentials -g [resource-group] -n [cluster-name]
```

* Verificar conexão com o cluster
```
kubectl cluster-info
```
##

### kubernetes dashboard
* [kubernetes-dashboard](https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/) 
```
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.0.0-beta8/aio/deploy/recommended.yaml
```

##

* Para utilizar esta imagem com o docker, execute o comando:
```
docker push straucorp/kubernetes-nodejs:latest
```

### Executar aplicação
```
git clone https://github.com/astraube/kubernetes-nodejs.git

cd kubernetes-nodejs

# deploy
kubectl apply -f k8s

# obter endereço de IP externo
kubectl get services
```

