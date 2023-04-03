Kubernetes - K8s

Cluster

(2 type od server)
 
1.Worker Node

2.Master Node
----------------------------------------------
Pod = 1 or more Containers
Deployment = same Pods for Auto Scaling
Service = access to Deployment with : ClusterIP / NodePort / LoadBalancer / ExternalName
Nodes = Servers
Cluster = a collection of nodes
----------------------------------------------


=================================
kubernetes in AWS


*   awscli = for command in aws  :
apt install python3-pip
pip3 install awscli --upgrade

*   kubectl = for control cluster  :
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

**   change premmisin =  chmod +x kubectl

*  eksctl = for create cluster  :
curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /*name of dir*



for use from any user = echo "export PATH=$PATH://" >> /etc/bash.bashrc


=============================
for connect to AWS

export AWS_ACCESS_KEY_ID=
export AWS_SECRET_ACCESS_KEY=
export AWS_DEFAULT_REGION=

=============================

For Create Cluster:
eksctl create cluster --name (*NAME)

--------------------------------------------
For Delete Cluster:
eksctl delete cluster --name (*NAME)

--------------------------------------------
For Create FileCluster:
mycluster.yml
eksctl create cluster -f mycluster.yml

--------------------------------------------
For Delete FileCluster:
eksctl delete cluster -f mycluster.yml




==================================
Command:


eksctl version
eksctl create cluster
eksctl delete cluster

eksctl create cluster -f mycluster.ymal
eksctl delete cluster -f mycluster.ymal

kubectl version
kubectl version --client
kubectl cluster-info
kubectl get nodes
kubectl get pods
kubectl run (*name pod*) --generator=run-pod/v1 --image=nginx:latest --port=80
kubectl port-forward (*name*) 1234:80
kubectl describe pods (*name*)
kubectl delete pods (*name*)
kubectl logs (*name*)
kubectl exec (*name) date
kubectl exec -it (*name*) bash
kubectl apply -f myfile.yml
kubectl delete -f myfile.yml



