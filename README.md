###### In this project, we want to deploy a stack in which all aspects of DevOps pipelines are handled. We are going to deploy our microservices alongside a GitLab instance on our K8S cluster.
# Problem
## Step 1
Deploy all of your microservices using the K8S Deployment resource. Change service type from NodePort to ClusterIP.

Create a ConfigMap for all of the microservices. Inject the configmap as Env variables.

## Step 2
Deploy Gitlab on your cluster. (Dockerized Gitlab, not on K8S)

## Step 3
Deploy Nginx Ingress and expose it using the NodePort service type.

## Step 4
Buy an ir Domain and resolve it to your cluster using CloudFlare.

----
# Solution
## Step 0
0- Install K8s on your nodes using kubespray

wiki: https://www.linuxtechi.com/install-kubernetes-using-kubespray/

## Step 1
1- In yout master node (w/ root) clone project06 git repository and create your services (microservices should be ClusterIP)
```
kubectl apply -f shop/shop-service.yml 
```