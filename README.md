# kubernetes-nodejs
Exemplo prático de um projeto em nodejs, orquestrado com kubernetes

[Leia a apresentação](https://www.slideshare.net/AndrStraube/docker-kubernetes-devops)

* Para utilizar esta imagem com docker, rexecute o comando:
```
docker push straucorp/kubernetes-nodejs:latest
```

* Para utilizar com pubernetes, execute os comandos:
```
git clone https://github.com/astraube/kubernetes-nodejs.git
```
```
cd kubernetes-nodejs
```
```
kubectl apply -f k8s
```