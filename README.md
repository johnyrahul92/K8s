# K8s

# Master 
1. Api Server - Acts as cluster gateway
2. Scheduler - Schedules the deployemnts,services etc
3. Control Manager - Checks the status and try to achive the desired set
4. etcd - Kind of persistence layer which hold the statistics

# Worker
1. Require Docker engine
2. Require kubelet process 
3. Will have kube proxy

kubectl get po -A

# Configurations

kubectl apply -f <filepath> - ( Create deployement/service etc using the configuration file. This act as upadte as well)
kubectl delete -f <filepath> - ( Delete deployemnt/service etc from the configuration file)

# Deployement
kubectl create deployment nginx-depl --image=nginx  (Create deployement minimilistic config)
kubectl create deployment mongo-depl --image=mongo

kubectl get deployment  - (List deployments)

kubectl edit deployment nginx-depl  - ( Get the deplyment yaml)

kubectl delete deployment mongo-depl  -( To remove the deployment and its futher downstream items like replicaset and pods)


# Pod
kubectl describe pod <podname>  - (Get the steps of pod creation)
kubectl logs <podname> - (Get logs of pod)

kubectl get pod - (To list the pods)
kubectl get pod -o wide - (To list the pods with wider details)

# Replicset is handled by kubernets
kubectl get replicaset


# Get logs of pod
kubectl logs <podname>
kubectl logs -f <podname> - (Rolling logs)

# get bash or sh inside container
kubectl exec -it <podname> -- bin/bash


# Service 
kubectl describe service <servicename>
kubectl get service
kubectl delete service <servicename>