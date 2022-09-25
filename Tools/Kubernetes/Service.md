# Services

## Needs of Services

- Kubernetes Pods are mortal, they don't heal
- Controllers create and destroys pods dynamically
- How to keep track of the IP address to connect to access the application
- Multiple tier appilcation


## What is Service?

- Service provides an abstraction for a set of pods and a policy to access them
- Service are Kubernetes API resource , defined in a namespace


## Types of service 

- Cluster IP:
  - Expose the service within the cluster
  - Maps any incoming port to a target port

- NodePort:
  - 
- LoadBalancer
- ExternalName