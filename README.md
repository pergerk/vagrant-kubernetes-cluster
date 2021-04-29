# up cluster 
```sh
vagrant box add general/ubuntu1604
```
```sh
vagrant up --no-parallel
```
```sh
export KUBECONFIG=$(pwd)/kubernetes-setup/.kube-config
```

Get dashboard token for kubectl proxy
```sh
kubectl -n kubernetes-dashboard describe secret $(kubectl -n kubernetes-dashboard get secret | grep admin-user | awk '{print $1}')
```

Dashboard url
```
http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/#/login
```
