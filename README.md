### Kubernetes Test
````
kubectl apply -f mongo-secret.yaml
kubectl apply -f mongo-configmap.yaml
kubectl apply -f mongo.yaml
kubectl apply -f mongo-express.yaml
````

You can reach ````http://localhost:8081````

#### PORTAINER SETUP
````
kubectl apply -f portainer.yaml
````

You can reach to portainer ````http://localhost:30777````


#### AUTOSCALING
````
kubectl apply -f metric-server.yaml
````
````
kubectl apply -f auto-scaling.yaml
````
