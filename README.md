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

# Beginner - Deploy microservices

http://a544c5bc4230442f8bfb55beb2e5f4a7-1253917647.ap-southeast-2.elb.amazonaws.com/

# Beginner - Deploy with Helm

5a06198459764066b46df97c97a4a08-697491835.ap-southeast-2.elb.amazonaws.com

```
cheungm:~/environment/ecsdemo-nodejs (master) $ kubectl get pods -l app.kubernetes.io/name=nginx
NAME                                 READY   STATUS    RESTARTS   AGE
mywebserver-nginx-854fc7f7bc-8h5jm   1/1     Running   0          63s
cheungm:~/environment/ecsdemo-nodejs (master) $ kubectl get service mywebserver-nginx -o wide
NAME                TYPE           CLUSTER-IP     EXTERNAL-IP                                                                   PORT(S)        AGE   SELECTOR
mywebserver-nginx   LoadBalancer   10.100.76.68   a5a06198459764066b46df97c97a4a08-697491835.ap-southeast-2.elb.amazonaws.com   80:30621/TCP   75s   app.kubernetes.io/instance=mywebserver,app.kubernetes.io/name=nginx
cheungm:~/environment/ecsdemo-nodejs (master) $ helm list
NAME            NAMESPACE       REVISION        UPDATED                                 STATUS          CHART           APP VERSION
mywebserver     default         1               2021-01-06 12:27:06.506648549 +0000 UTC deployed        nginx-8.2.4     1.19.6     
cheungm:~/environment/ecsdemo-nodejs (master) $ helm uninstall mywebserver
release "mywebserver" uninstalled
```
# Links

https://www.eksworkshop.com/

