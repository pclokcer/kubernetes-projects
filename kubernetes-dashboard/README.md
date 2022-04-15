### KUBERNETES DASHBOARD
````shell
kubectl apply -f kubernetes-dashboard.yaml
kubectl apply -f create-service-account.yaml
kubectl apply -f create-cluster-role.yaml
kubectl proxy
````

You need to generate token for login. Below Run command
````shell
kubectl -n kubernetes-dashboard get secret $(kubectl -n kubernetes-dashboard get sa/admin-user -o jsonpath="{.secrets[0].name}") -o go-template="{{.data.token | base64decode}}"
````

You can now go ````http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/````