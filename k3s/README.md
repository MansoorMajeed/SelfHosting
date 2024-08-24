# SelfHosting with k3s - Full Setup

This doc will walk you through setting up a full k3s setup to self hosting your applications and services.

## What we will do

1. Use Git for everything - No manual `kubectl apply` unless absolutely needed
2. ArgoCD for automated deploys
3. Let's Encrypt + Cert manager for certificates
4. MetalLB for load balancing
5. LongHorn for persistent storage
6. Using a NAS for persistent storage
7. Prometheus + Grafana for monitoring


## Where to start?

Start [HERE](./00-hardware.md)