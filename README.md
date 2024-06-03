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
