how install kubernetes on  AWS

we need 3 things:

1.awscli for command
2.kubectl for control cluster
3.eksctl for create new cluster

firts of all we open server in ec2 on UBUNTU

install AWScli:

1. sudo apt-get update
2. sudo apt install python3-pip
3. pip3 install awscli

now us make a new dir kubernetes:
(/home/ubuntu/kubernetes/)

now we donwload kubectl and eksctl into kubernetes dir

go this site:
https://docs.aws.amazon.com/eks/latest/userguide/getting-started.html

and start command:
1. curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /home/ubuntu/kubernetes/


now we install kubectl:
go to this site:
https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/

now we add primeshion:

1. chmod +x kubectl

for us all user 
1. sudo su
2. echo "export PATH=$PATH:/home/ubuntu/kubernetes/" >> /etc/bash.bashrc
3. logoff and login 

now we check version
1. eksctl version
2. kubectl version --client


now we make aws configure with us credentials:

export AWS_ACCESS_KEY_ID=(your number)
export AWS_SECRET_ACCESS_KEY=(your number)

now we can check if this work

1. aws s3 ls
and this show us bucket

good luck
