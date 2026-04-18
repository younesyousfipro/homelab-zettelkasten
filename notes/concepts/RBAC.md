# RBAC

RBAC (Role-Based Access Control) is a method used to control access to resources based on roles assigned to users.

## Goal

Control **who can do what on which resources**

## Core model

Subject → Role → Permissions → Resources

## Key idea

Access is not granted directly to users, but through roles.

## Why RBAC exists

### Without RBAC

- everyone has admin-level access
- high risk of accidental deletion or misconfiguration
- secrets and sensitive data are exposed
- no separation of responsibilities
- difficult to audit actions
- increased security risks

### With RBAC

- controlled and explicit access
- safer operations and reduced blast radius
- clear separation of responsibilities (dev, ops, admin)
- improved auditability
- enforcement of the [[least-privilege-principle]]
- better alignment with real-world team structures

## Related

- [[authentication]]
- [[authorization]]
- [[least-privilege-principle]]
- [[rbac-in-kubernetes]]
- [[rbac-in-devops]]
