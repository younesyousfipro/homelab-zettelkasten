# Ingress controller

An Ingress controller is a component that implements the rules defined in Kubernetes Ingress resources.

It watches the cluster and configures a reverse proxy accordingly.

## Role

Ingress resource = configuration  
Ingress controller = execution

Without a controller, an Ingress has no effect.

## How it works

1. watches Ingress resources
2. reads routing rules
3. configures a reverse proxy (nginx, traefik, etc.)
4. routes traffic to services

## Architecture

Client → Ingress Controller → Service → Pod

## Common controllers

- Traefik
- NGINX Ingress Controller
- HAProxy
- Istio (gateway model)

## Example

In k3s:

- Traefik is installed by default
- acts as the ingress controller

## Key idea

Ingress is declarative  
Ingress controller is the runtime

## Related

- [[kubernetes-ingress]]
- [[kubernetes]]
- [[linux-access-control]]