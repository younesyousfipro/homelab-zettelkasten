# RoleBinding (Kubernetes)

A RoleBinding associates a Role with a subject (user, group, or service account) within a specific namespace.

It grants the permissions defined in the Role to the subject.

A RoleBinding does not define permissions by itself. It only links a subject to an existing [[role-kubernetes]].

## Scope

- applies to a single namespace
- does not grant cluster-wide access

## Subjects

A RoleBinding can target:
- a user
- a group
- a service account

## Example

```bash
kubectl create rolebinding read-pods \
  --role=pod-reader \
  --user=dev-user
  ```

This binds the pod-reader Role to the user dev-user in the current namespace.

## Mental model

subject → RoleBinding → Role → permissions → resources

Related
	•	[[role-kubernetes]]
	•	[[clusterrolebinding-kubernetes]]
	•	[[rbac in kubernetes]]
	•	[[kubernetes verbs]]
	•	[[kubernetes resources]]