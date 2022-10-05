### emptyDir volume type

- Stores data on the node on which the pod is running
- Empty when pod starts
- Data in the volume is removed when pod is removed from the node

### hostPath volume type

- Mounts a file or directory from the host node's filesystem into the pod
- File or directory on the hostmachine will last even if the pod is removed or recreated
- If directory is not present on the pod then it will be created
