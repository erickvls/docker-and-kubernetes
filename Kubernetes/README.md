This repository was created for self learning purpose.
- References:
   -  https://www.youtube.com/watch?v=1xo-0gCVhTU&list=PLCOzDPP_yQKiVcDr2ywEsfki6ZPKXpeoC&index=5&ab_channel=JamesQuigley
   - https://www.youtube.com/watch?v=d6WC5n9G_sM&ab_channel=freeCodeCamp.org
   - https://www.youtube.com/watch?v=y_vy9NVeCzo&ab_channel=CloudWithRaj

## #  Kubernetes

### What is it?
 - It is an open source system for automating deployment, scaling, and management of containerized applications.

### Runing local
 - Install kubectl
 - Install minikube

### Kubernetes Vocab
 - Node: It is an instance of a computer, running kubernetes
    - Kubelet
    - Communicates with master
    - Runs pods
 - Pod
    - Runs 1+ containers
    - Exists on a node
 - Services
    - Handles requests: Either coming from inside the cluster (one node to another), or from outside.
    - Usually a load balancer
- Deployment
    - Defines desired state

![recap kubernetes](../imgs/k8s-recap.png)


![kubernetes-overview](../imgs/k8s-deployment.png)


## Deployment file explanation
![kubernetes-deployment](../imgs/k8s-code.png)