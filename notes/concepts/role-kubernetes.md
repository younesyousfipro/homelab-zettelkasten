# Role (Kubernetes)

A Role defines permissions within a single namespace.

It specifies which actions (verbs) are allowed on which resources.

## Example

```bash
kubectl create role pod-reader \
  --verb=get,list \
  --resource=pods
```
## Scope

	•	applies to a single namespace
	•	must be attached using a [[rolebinding-kubernetes]]

## Related

	•	[[rbac-in-kubernetes]]
	•	[[rolebinding-kubernetes]]
	•	[[kubernetes-verbs]]
	•	[[kubernetes-resources]]