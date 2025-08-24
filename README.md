# otel-profiling-test

This allows easy testing of Opentelemetry profiling based on example from here:

https://github.com/grafana/pyroscope/tree/main/examples/grafana-alloy-auto-instrumentation/ebpf-otel 

This repository deploys ArgoCD and a collection of apps to deploy necessary resources.

To use this repository

```
$ kubectl apply -k argocd

# Wait for services to be deployed
$ kubectl port-forward svc/grafana-service 3000:3000

# Access http://localhost:3000 from browser and view profiling info from k8s hosts
```
