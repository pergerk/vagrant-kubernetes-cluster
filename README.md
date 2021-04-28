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