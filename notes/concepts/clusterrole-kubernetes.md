# ClusterRole (Kubernetes)

A ClusterRole defines permissions across the entire cluster.

Unlike a [[role-kubernetes]], it is not limited to a single namespace.

## Use cases

- access to cluster-wide resources (nodes, namespaces)
- shared roles across multiple namespaces

## Example

```bash
kubectl create clusterrole pod-reader \
  --verb=get,list \
  --resource=pods
```

## Scope

    •	applies to the entire cluster
    •	can be used with a [[clusterrolebinding-kubernetes]] or a [[rolebinding-kubernetes]]

## Related

    •	[[rbac-in-kubernetes]]
    •	[[clusterrolebinding-kubernetes]]
    •	[[role-kubernetes]]
