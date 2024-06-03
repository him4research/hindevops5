# hindevops5
Devops By Himanshu 
# Pod details === https://kubernetes.io/docs/concepts/workloads/pods/
Run Pod by command - kubectl apply -f pod.yaml 

Kubeclt get all ------------- get all the objects of k8s. 

To see the IP of pod ------- kubectl get pod -o wide   Till now get the IP but not able to access it. Via IP:port As pods are not allowed to connect outside cluster directly. 

# Getting inside the container ------
kubeclt exec nginx(podname)  ls 

kubeclt exec nginx(podname) sh          ----to go inside shell 

# Service in Kubernetis 
If u are running docker k8s on windows first do port forward -----

kubectl port-forward service/fleetman-webapp 30080:80

Also It is internet facing so we have to use NodePort service. 

In nodePort service NodePOrt is between 30000 to 32767

targetport is contianer port 

port is service port or clusterIp Port

If we want to use service for internal cluster not for internet use Cluster IP

To run on internet ---- http://localhost:30080/


# Labels 
kubectl get po --show-labels         shows all pods with labels 

Modify by show specific lable release=0 --------- kubectl get po --show-labels -l release=0 

# add another pod queue
First we will add lable 

Put label in pod as  app: queue    {{{ use selector in service as app:webapp     }}}{{ Deploy image  richardchesterwood/k8s-fleetman-queue}}
(( running on port 8161 is the admin console ))
((user and pass (admis/admin)))
(( expose nordport on 30010 ))

Also add seprate service for it. AFter running service, 

kubectl port-forward svc/fleetman-queue 30010:8161

#localhost:30010


