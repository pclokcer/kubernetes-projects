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

Run this command for test
````
kubectl run -i --tty load-generator --rm --image=busybox --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- http://php-apache; done"
````
