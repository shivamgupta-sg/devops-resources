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

## Kubernetes Object Management

- Imperative commands - operates directly on the live objects
  - `kubectl run nginx --image nginx`
  - `kubectl create deployment nginx --image nginx`
  - Simple with single line/step commands
  - Do not provide a template for creating new objects nor is there any audit trail created

- Imperative Object Configration - specify file containg full object definition
  - `kubectl apply -f config1.yaml`
  - `kubectl apply -f config2.yaml`
  - Configuration 