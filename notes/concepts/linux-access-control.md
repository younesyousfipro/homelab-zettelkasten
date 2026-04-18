# Linux access control

Linux access control defines how permissions are managed on files and directories.

It determines **who can access what, and how**.

## Core model

subject → ownership → permissions → resource

## Key components

- ownership (user + group)
- permissions (read, write, execute)
- execution context (process user)

## Key idea

Access is attached to each resource, not managed through centralized roles.

## Comparison with RBAC

Linux:

subject → user/group → permissions → resource

RBAC:

subject → role → permissions → resource

## Related

- [[rbac]]
- [[rbac-in-devops]]
- [[least-privilege-principle]]
- [[linux-file-permissions]]
- [[linux-octal-permissions]]
- [[linux-users-and-groups]]
- [[sudo]]
- [[dac]]
