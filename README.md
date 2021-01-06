# AWS-EKS-Workshop
AWS-EKS-Workshop

# Objectives
- Explore AWS EKS Kubernetes
- Create Kubernetes Cluster via Cloud 9

# Test the cluster
```
cheungm:~/environment $ kubectl get nodes # if we see our 3 nodes, we know we have authenticated correctly
NAME                                                STATUS   ROLES    AGE    VERSION
ip-192-168-25-194.ap-southeast-2.compute.internal   Ready    <none>   102s   v1.17.12-eks-7684af
ip-192-168-61-7.ap-southeast-2.compute.internal     Ready    <none>   103s   v1.17.12-eks-7684af
ip-192-168-91-194.ap-southeast-2.compute.internal   Ready    <none>   100s   v1.17.12-eks-7684af
```
# Beginner - DEPLOY THE KUBERNETES DASHBOARD

https://a06aed0e9db7464f81dd39ce1bb65866.vfs.cloud9.ap-southeast-2.amazonaws.com/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/?_c9_id=livepreview1&_c9_host=https://ap-southeast-2.console.aws.amazon.com#/namespace?namespace=default

# Links

https://www.eksworkshop.com/
