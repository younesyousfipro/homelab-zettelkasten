# k3s

k3s is a lightweight Kubernetes distribution designed for resourec-constrainted environments, like my homelab.

It provides a fully functional Kubernetes cluster with reduced complexity.

## Key differences with Kubernetes

### 1. Simplicity

k3s:

- single binary
- simple install (curl script)
- minimal configuration

k8s:

- multiple components (kubelet, api-server, etc.)
- more complex setup

---

### 2. Resource usage

k3s:

- low CPU / RAM usage
- suitable for small machines (like homelab nodes)

k8s:

- higher requirements

---

### 3. Embedded components

k3s includes:

- container runtime (containerd)
- networking (flannel by default)
- ingress controller (Traefik)
- lightweight database (SQLite by default)

k8s:

- requires external setup for these components

---

### 4. Database

k3s:

- SQLite (default)
- can use external DB (etcd, MySQL, PostgreSQL)

k8s:

- etcd only (default and standard)

---

### 5. Use cases

k3s:

- homelab
- edge computing
- IoT
- development environments

k8s:

- production clusters
- large-scale systems

---

## What stays the same

k3s is still Kubernetes.

We use:

- `kubectl`
- same API
- same manifests
- same concepts (pods, services, ingress, RBAC)

## Example

In my homelab:

- control plane → k3s server
- workers → k3s agents

Same Kubernetes behavior, simpler setup.

## Related

- [[kubernetes-ingress]]
- [[rbac-in-kubernetes]]
- [[traefik]]