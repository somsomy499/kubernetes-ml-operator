# K8s ML Operator ☸️

Kubernetes operator for managing ML workloads with GPU-aware scheduling.

## Features

- **GPU Scheduling**: Automatic GPU allocation and sharing
- **Auto-scaling**: HPA based on inference queue depth
- **Model Serving**: Rollout, canary, A/B deployments
- **Experiment Tracking**: K8s-native experiment CRDs

## Quick Start

```yaml
apiVersion: ml.example.com/v1
kind: ModelDeployment
metadata:
  name: my-model
spec:
  model: gpt-4o-adapter
  replicas: 3
  resources:
    gpu: 2
  scaling:
    minReplicas: 1
    maxReplicas: 10
    targetQueueDepth: 100
```

## License

Apache 2.0