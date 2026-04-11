# RBAC in Kubernetes

Kubernetes implements RBAC (Role-Based Access Control) to manage access to cluster resources.

It defines what actions a subject can perform on specific resources within a given scope.

## Purpose

RBAC is used to:
- restrict access to cluster resources
- enforce separation of responsibilities
- improve security and auditability

Without RBAC, all users would effectively have admin access.

## Model

Subject → Role / ClusterRole → Permissions → Resources → Scope

- **Subject**: user, group, or service account
- **Role / ClusterRole**: defines permissions
- **Permissions**: actions (verbs)
- **Resources**: objects (pods, services, etc.)
- **Scope**: namespace or cluster-wide

## Key components

- [[role_k8s]] → permissions within a namespace  
- [[cluster_role_k8s]] → permissions at cluster level  
- [[role_binding_k8a]] → attaches a Role to a subject  
- [[cluster_role_binding_k8s]] → attaches a ClusterRole globally  

## Mental model

RBAC does not grant access by default.

You must explicitly:
1. define permissions (Role / ClusterRole)
2. bind them to a subject (Binding)

## Example

```yaml
kind: Role
rules:
- resources: ["pods"]
  verbs: ["get", "list"]
```
This defines read access to pods in a namespace.
It becomes effective only when attached using a [[rolebinding-kubernetes]].

## Related
	•	[[rbac]]
	•	[[authentication]]
	•	[[authorization]]
	•	[[kubernetes verbs]]
	•	[[kubernetes resources]]
	•	[[role-kubernetes]]
	•	[[clusterrole-kubernetes]]
	•	[[rolebinding-kubernetes]]
	•	[[clusterrolebinding-kubernetes]]