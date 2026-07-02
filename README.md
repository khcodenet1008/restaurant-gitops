# Restaurant GitOps

Simple GitOps overlay repo for the 4-service restaurant system.

## What It Deploys

- MySQL
- Kafka
- `gateway-service`
- `menu-service`
- `order-service`
- `payment-service`

## Overlays

- `overlays/dev`
- `overlays/demo`
- `overlays/istio-dev`

## Quick Start

```bash
kubectl apply -k restaurant-gitops/overlays/dev
```

Istio demo:

```bash
istioctl install --set profile=demo -y
kubectl apply -k restaurant-gitops/overlays/istio-dev
```
