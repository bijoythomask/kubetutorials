# Setting up Kubernetes on docket-desktop Windows 10

## Configure the Resourses
    Memory :  4- 8 GB
    Core : 2-4
    Harddisk : 60 -120 GB
## Configure Dashboard
    * kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/master/src/deploy/alternative/kubernetes-dashboard.yaml
    * kubectl create -f https://raw.githubusercontent.com/kubernetes/heapster/master/deploy/kube-config/influxdb/influxdb.yaml
    * kubectl create -f https://raw.githubusercontent.com/kubernetes/heapster/master/deploy/kube-config/influxdb/heapster.yaml
    * kubectl apply -f https://raw.githubusercontent.com/bijoythomask/kubetutorials/master/dashboard/service.yaml

## Configure Ingress

    helm install stable/nginx-ingress --name ingress-nginx --namespace ingress-nginx