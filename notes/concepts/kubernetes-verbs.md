# Kubernetes verbs

Verbs define the actions that can be performed on Kubernetes resources.

They are used in RBAC rules to specify allowed operations.

## Common verbs

- get → read a single resource
- list → read multiple resources
- watch → observe changes in real time
- create → create a resource
- update → modify a resource
- delete → remove a resource

## Mental model

verbs = actions  
resources = objects

RBAC rule = "which actions on which objects"

## Related

- [[kubernetes-resources]]
- [[rbac-in-kubernetes]]
