# RBAC usage in teams

RBAC is used to separate responsibilities across roles in a system.

## Developers

- deploy applications
- read logs
- access only their namespace

## QA / Test

- read resources
- test deployments

## DevOps / Platform

- manage infrastructure
- manage deployments
- manage namespaces

## Admin

- full access to the system

## Goal

- enforce separation of responsibilities
- reduce risk
- improve security

## Related

- [[rbac]]
- [[least-privilege-principle]]