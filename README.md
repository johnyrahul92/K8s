# K8s

kubectl get po -A
kubectl get nodes  // to get the nodes
kubectl get pod // to get the nodes
kubectl get service // to get the service


# Deployement
kubectl create deployment nginx-depl --image=nginx  (Create deployement minimilistic config)
kubectl create deployment mongo-depl --image=mongo

kubectl get deployment  - (List deployments)

kubectl edit deployment nginx-depl  - ( Get the deplyment yaml)

kubectl delete deployment mongo-depl  -( To remove the deployment and its futher downstream items like replicaset and pods)


# Replicset is handled by kubernets
kubectl get replicaset

# Get the steps of pod creation
kubectl describe pod <podname>
# Get logs of pod
kubectl logs <podname>

# get bash or sh inside container
kubectl exec -it <podname> --bin/bash