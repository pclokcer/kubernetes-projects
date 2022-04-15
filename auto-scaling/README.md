#### AUTOSCALING
````shell
kubectl apply -f metric-server.yaml
kubectl apply -f auto-scaling.yaml
````

You can check metric-server running after install metric-server 
````shell
kubectl -n kube-system get pods
````

Run this command for test
````shell
kubectl run -i --tty load-generator --rm --image=busybox --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- http://php-apache; done"
````
