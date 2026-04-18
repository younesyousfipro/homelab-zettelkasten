# Kubernetes resources

Resources are the objects managed by the Kubernetes API.

They represent the state of the cluster.

## Common resources

- pods
- deployments
- services
- configmaps
- secrets
- nodes
- namespaces

## Mental model

resources = objects  
verbs = actions

RBAC rule = "which actions on which objects"

## Important distinction

- namespaced resources (pods, deployments, services)
- cluster-wide resources (nodes, namespaces)

This affects whether you use:

- [[role-kubernetes]]
- [[clusterrole-kubernetes]]

## Related

- [[kubernetes-verbs]]
- [[rbac-in-kubernetes]]
- [[role-kubernetes]]
- [[clusterrole-kubernetes]]
