# Kubernetes Cluster Architecture

## Management of the nodes

- Node is created seperately
- Node validation is done by checking health of the node
- K8s keeps checking the invalid node to see whether it become valid
- `kubectl get nodes`