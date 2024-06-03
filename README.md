# hindevops5
Devops By Himanshu 
# Pod details === https://kubernetes.io/docs/concepts/workloads/pods/
Run Pod by command - kubectl apply -f pod.yaml 

Kubeclt get all ------------- get all the objects of k8s. 

To see the IP of pod ------- kubectl get pod -o wide   Till now get the IP but not able to access it. Via IP:port As pods are not allowed to connect outside cluster directly. 

# Getting inside the container ------
kubeclt exec nginx(podname)  ls 

kubeclt exec nginx(podname) sh          ----to go inside shell 

