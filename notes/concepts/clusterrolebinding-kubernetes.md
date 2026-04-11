# ClusterRoleBinding (Kubernetes)

A ClusterRoleBinding associates a ClusterRole with a subject (user, group, or service account) across the entire cluster.

It grants cluster-wide permissions.

A ClusterRoleBinding does not define permissions by itself. It links a subject to a [[clusterrole-kubernetes]].

## Scope

- applies to the entire cluster
- not limited to a namespace

## Example

```bash
kubectl create clusterrolebinding admin-binding \
  --clusterrole=cluster-admin \
  --user=admin-user
  ```

  ## Related

  	•	[[clusterrole-kubernetes]]
	•	[[rolebinding-kubernetes]]
	•	[[rbac-in-kubernetes]]
