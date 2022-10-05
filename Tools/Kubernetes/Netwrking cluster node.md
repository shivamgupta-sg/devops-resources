## Netowking configuration on cluster nodes

### Kubernetes Networking Model

- Every Pod get its own IP address
- Port allocation, naming, service discovery, load balancing, application configuration, and pod migration
- Less cunbersome porting of apps from VMs to Containers
- Some fundamental points
  - pods on a host can communiocate with all pods on all hosts without NAT
  - agents on a host ccan communicate with all pods on that host
  - IP that a container sees for itself, is the same IP that other see it as 


### Networking concepts

1. Highly-coupled container-to-container communications
   - Containers within a Pod share their network namespaces
   - Containers within a Pod must coordinate port usage

2. Pod-to-Pod Communications
   - Pods can communicate without proxies or translations

3. Pod-to-Service communications
   - Service abstration provides a way to group pods under a common access policy
   - kube-proxy process programs iptables rules to trap access to service IPs and redirect them to the correct backends

4. External-to-internal communications
   - NodePort, LoadBalancer and ExternalName services

### Implementing the networking Model

- Number of ways in which Kubernetes network model can be implemented
- Calico
  - highly scalable networking and network policy solution for both linux and Windows
  - assigns IP addressess, programs routing table and distribute routes
  - Supports using the Border Gateway Protocol (BGP) for sharing routing information
- Flannel
  - simple overlay network, created by CoreOS
  - routes pod traffic using static per-node CIDRs
  - Pods will be assigned one IP address in this overlay network
  -  