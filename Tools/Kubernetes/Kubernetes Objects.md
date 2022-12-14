# Kubernetes Objects

## Introduction

- Persistent entity expressed in YAML format
- Represent the desired stateof the cluster
- Describe the following:
  - Containerized applications running in the cluster
  - Resources made available to these applications
  - Policies fir these applications
- Command-line utilityto use the Kubernetes API
- Using client libraries

## Object Spec and Status

- Spec: provided by user and describes the desired state for the object in yaml format
- Status: describes the actual state of the coject in the cluster

---

## Pods

- Single or multiple containers
  - Init containers and App containers
- Storage Resources
  - Shared storage volumes
- Unique Network IP
  - Containers share the Network namespace
- Options governing how to container should run
- Ephemaral and disposable entites
- Kubernetes use controllers to inmplement self healing and scaling
- Pod manifest

### Phases of Pods

- Pending: Accepted by the cluster; Waiting
- Running: running, starting or restarting
- Succeeded
- Failed - All containers terminated; atleast one in failure
- Unknown

### Container States

- Once Pod is assigned to a node by scheduler, kubelet starts creating containers using container runtime
- Check the state of the container - `kubectl describe pod [POD_NAME]`
- Waiting - requried operations
- Running
- Terminated - Successfully completed execution or failed

### Termination of Pods

- Pods having running processes and no longer required, needs to be terminated
- By default, all deletes are graceful with in 30 seconds
- `kubectl delete` commands supports the `--grace-period=<seconds>` option
- Force deletion of a Pod deleted it from the cluster state and etcd immediately

---

## Kubernetes Object Management

- Imperative commands - operates directly on the live objects
  - `kubectl run nginx --image nginx`
  - `kubectl create deployment nginx --image nginx`
  - Simple with single line/step commands
  - Do not provide a template for creating new objects nor is there any audit trail created

- Imperative Object Configration - specify file containg full object definition
  - `kubectl apply -f config1.yaml`
  - `kubectl apply -f config2.yaml`
  - Configuration is simple to understand and can mbe source controlled
  - Reuires additional step of creating YAML file
  
- Declarative Object Configration - user does not define the operations to be taken
  - Create, updatre, and delete operations are automatically detected per-object by kubectl
  - `kubectl diff -f configs/`
  - `kubectl apply -f <directory>/`
  - Better support for operating on directories and automatically detecting operation types
  - Harder to debug and understand results

### Names

- Nane is unique for a type of  resource withing a namespace
- Two different namespace can have a pod with same name
- UID is unique across the whole cluster
- Kubernetes resourcew can have names upto 253 character long
- aloowed characte - digits (0-9), lowercase letters(a-z), hypen(-) and dot(.)

### Namespaces

- `kubectl get namespace` get namespaces of the entire cluster
- **Default Namespaces** created ny kubernetes cluster
  - default: for objects with no specified namespace
  - kube-system: objects created by the kubernetes system
  - kube-public: reserverd for cluster usage. In case if any resource is
  - kube-node-lease: contains lease objects
-While creating a new object, we can either specify the namespace or we we can set context for all subsequent kubectl commands
  - `kubectl run nginx --image=nginx --namespace=<namespace-name>`
  - `kubectl config set-context --current --image=nginx --namespace=<namespace-name>`
- Create a new namespace
  - `kubectl create namespace <namespace-name>`
- Look for pods in a specified namespace
- List objects across all namespaces
- See chich Kubernetes resources are and aren't in a namespace


## Service
- Pods are ephemeral and are recreated frequently
- On creation pod have get a new IP
- We can not use pod IPs which keeps changing for the application to access, so we use servicesto communicate with them
- Services and Pod Lifecycle is not linked so even if the pod is recreated the service IP doesnot get changed make it easy to access the application running on the pod
- It provides a permanent IP address which can be used to communicate with Pods
- Helps in load balancing 