# Running Local Kubernetes

##### Requirement:

- [Kubectl](https://kubernetes.io/docs/taskvvs/tools/)
- [Docker desktop](https://www.docker.com/products/docker-desktop/)
- [Helm](https://helm.sh)

##### Setup:

1. `kubectl create namespace ingress-nginx`

2. `helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx`

3. `helm repo update`

4. `helm install ingress-controller ingress-nginx/ingress-nginx --namespace ingress-nginx`

5. `kubectl apply -f .`

##### Connections:

[ContentWriting Microservice](https://github.com/TrackPackers/ContentWritingService) - /contentwriter  
[newPostsFeed Microservice](https://github.com/TrackPackers/newPostsFeed) - /newpostsfeed

##### Errors:

If you get the error along the lines: 'Already exists'. You can restart with removing the helm repo:

```bash
helm repo remove ingress-nginx
kubectl delete ns ingress-nginx
```
