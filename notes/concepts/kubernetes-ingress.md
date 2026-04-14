# Kubernetes ingress

Ingress is a Kubernetes resource used to expose HTTP and HTTPS services to the outside world.

It defines routing rules based on hostnames and paths.

## Mental model

Think of Ingress as a **smart receptionist** or **reverse proxy** in front of your cluster.

Instead of exposing each service separately, you have **one entry point** that decides:

- which app to send the request to
- based on the domain or URL

## Problem it solves

By default, Kubernetes services are exposed using:

- ClusterIP → internal only
- NodePort → exposed but low-level
- LoadBalancer → cloud dependent

Ingress provides:

- centralized HTTP routing
- cleaner external access
- domain-based routing

## How it works

Client → Ingress → Service → Pod

Ingress acts as an entry point that routes traffic to services based on rules.

Step by step:
	1.	client sends request (browser, curl)
	2.	request hits the ingress endpoint
	3.	ingress checks rules (host / path)
	4.	forwards request to the correct service
	5.	service routes to a pod

## Example (conceptual)

```yaml
apiVersion: networking.k8s.io/v1
kind: Ingress
spec:
  rules:
  - host: my-app.local
    http:
      paths:
      - path: /
        backend:
          service:
            name: my-service
            port:
              number: 80
```

## Important

Ingress is only a configuration object.

It does nothing by itself.

It requires an [[ingress-controller]] to function.

Ingress = configuration (what should happen)
Ingress controller = execution (makes it happen)

## Use cases

•	expose web applications
•	route multiple services behind one IP
•	handle TLS (HTTPS)
•	domain-based routing

## Related

•	[[kubernetes]]
•	[[ingress-controller]]
•	[[rbac-in-kubernetes]]