# Kubernetes Cluster Architecture

## Management of the nodes

- Node is created seperately
- Node validation is done by checking health of the node
- K8s keeps checking the invalid node to see whether it become valid
- `kubectl get nodes`


## Basic Architecture
![kubernetes architecture](https://ibb.co/5hVPYZp)

- Master - Slave architecture
- Master manages all workers
- Actual works are done by workers
- Master aand Worker node makes one unified machine
- Kubelets are the front end of the worker nodes, every communication in and out of the worker node is handled by kubelet
- Master node is important, to make a cluster high availability we use multiple master nodes as if master node fails we can lose the access to the cluster also

**Master Node Components**
- API Server - all communication is done using the APIs, api server handles all the api calls of the master node, Entrypoint of K8s Cluster
- etcd - K8s backing store
- Scheduler - ensures pod placements
- Controller - keeps track of whats happening in the cluster

**Worker Node Components**
- Kubelet
- Kube-Proxy
- Container-Runtime