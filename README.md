# Helm POC

Helm chart setup for a simple nginx deployment.

Based on good work of Aman Jaiswal and Bibin Wilson: https://devopscube.com/create-helm-chart/

## Usage

To verify the chart setup:

```bash
helm lint ./nginx-chart/.
```

To test run install:

```bash
helm install --dry-run frontend  nginx-chart
```

To install default development environment:

```bash
helm install frontend nginx-chart
```

To upgrade

```bash
helm upgrade frontend nginx-chart
```

To rollback

```bash
helm rollback frontend
```

To uninstall

```bash
helm uninstall frontend
```

To install with production environment:

```bash
helm install frontend nginx-chart --values ./env/prod-values.yaml
```
