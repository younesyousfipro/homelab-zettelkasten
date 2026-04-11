# Role (Kubernetes)

Defines permissions within a single namespace.

A Role specifies which actions (verbs) are allowed on which resources.

## Example

```bash
kubectl create role pod-reader \
  --verb=get,list \
  --resource=pods
```

## Related
- [[rbac in kubernetes]]
- [[rolebinding-kubernetes]]