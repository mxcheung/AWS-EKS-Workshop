# Launching an EKS Cluster

https://github.com/ACloudGuru-Resources/Course_EKS-Basics


# create user and access key

```
aws iam create-user --user-name k8-admin

aws iam attach-user-policy \
    --policy-arn arn:aws:iam::aws:policy/AdministratorAccess \
    --user-name k8-admin

aws iam create-access-key \
    --user-name k8-admin
```

```
{
    "AccessKey": {
        "UserName": "k8-admin",
        "AccessKeyId": "AKIAU2HR67XXXXXXX",
        "Status": "Active",
        "SecretAccessKey": "FGb6lXCbKBXXXXXXXXXXXXXXXXX",
        "CreateDate": "2024-01-10T06:15:43+00:00"
    }
}
```

# EC2 install aws + kubectl +  eksctl

```
aws --version
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
which aws
sudo ./aws/install --bin-dir /usr/bin --install-dir /usr/bin/aws-cli --update
aws --version
curl -o kubectl https://amazon-eks.s3.us-west-2.amazonaws.com/1.16.8/2020-04-16/bin/linux/amd64/kubectl
chmod +x ./kubectl
mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$PATH:$HOME/bin
kubectl version --short --client
curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
sudo mv /tmp/eksctl /usr/bin
eksctl version
```

# AWS configure
```
[ec2-user@ip-10-0-1-58 ~]$ aws configure
AWS Access Key ID [None]: AKIAU2HR6xxxxx
AWS Secret Access Key [None]: FGb6lXCbKBYsUK+5xxxxxx
Default region name [None]: us-east-1
Default output format [None]: 
```


# Provision EKS cluster

```
eksctl create cluster --name dev --region us-east-1 --nodegroup-name standard-workers --node-type t3.medium --nodes 3 --nodes-min 1 --nodes-max 4 --managed
```




#Create a Deployment on Your EKS Cluster

```
sudo yum install -y git
git clone https://github.com/ACloudGuru-Resources/Course_EKS-Basics
cd Course_EKS-Basics
kubectl apply -f ./nginx-svc.yaml
kubectl get service
kubectl apply -f ./nginx-deployment.yaml
kubectl get deployment
kubectl get pod
kubectl get rs
kubectl get node
```
