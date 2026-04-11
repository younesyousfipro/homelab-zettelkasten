# RBAC example Kubernetes

Grant a developer permissions to manage pods in a namespace.

## Role
- resources: pods
- verbs: get, list, create, delete

## Binding
- subject → Role

## Related
- [[role-kubernetes]]
- [[rolebinding-kubernetes]]
- [[rbac in kubernetes]]