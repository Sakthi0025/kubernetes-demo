
# Kubernetes Nginx Deployment and Services

This repository contains Kubernetes YAML files to deploy an Nginx application and expose it using different Kubernetes Service types.

## Files

- deployment.yaml – Nginx Deployment with multiple replicas  
- svc.yaml – Base Service definition  
- clusterip.yaml – ClusterIP Service (internal access)  
- nodeport.yaml – NodePort Service (external access)  
- lb.yaml – LoadBalancer Service  

## Prerequisites

- Kubernetes cluster (Kind / Minikube / Cloud)
- kubectl installed
- Docker (for Kind or Minikube)

## Deploy Application

Apply the Deployment:
kubectl apply -f deployment.yaml

Verify Pods:

kubectl get pods


## Expose the Application

### ClusterIP Service


kubectl apply -f clusterip.yaml
kubectl get svc


### NodePort Service

kubectl apply -f nodeport.yaml
kubectl get svc

Access:


http://<Node-IP>:<NodePort>


### LoadBalancer Service

kubectl apply -f lb.yaml
kubectl get svc
```

Note: LoadBalancer requires a cloud provider or MetalLB when using Kind.

## Verify Resources

```bash
kubectl get deployments
kubectl get pods
kubectl get services
```

## Cleanup

```bash
kubectl delete -f deployment.yaml
kubectl delete -f clusterip.yaml
kubectl delete -f nodeport.yaml
kubectl delete -f lb.yaml
```

## Author

Kubernetes Deployment and Service practice project

```

If you want, I can:
- Make it **shorter**
- Add **screenshots steps**
- Customize it for **GitHub interview projects**
```
