Helm charts for microservice

# How to use the base helm chart?
The base helm chart is a common chart for micro-service which is running on kubernetes  
platform or going to be running on it, it has covered the basic objects creation definition,
so it can be consumed as a "parent" chart.
Steps to add it as dependency in your chat:
1. Add https://akjamie.github.io/helm-charts to your helm repo.
```shell
helm repo add akjamie https://akjamie.github.io/helm-charts

helm repo search akjamie
NAME                    CHART VERSION   APP VERSION     DESCRIPTION                
akjamie/base            0.1.2           1.0.0           A Helm chart for Kubernetes
akjamie/order-service   0.1.2           1.0.0           A Helm chart for Kubernetes
```
2. Add dependency in your Chart.yaml
```yaml
apiVersion: v2
name: test-service
description: A Helm chart for Kubernetes
type: application
version: 0.0.1
appVersion: "1.0.0"

dependencies:
  - name: base
    version: 0.1.3
    repository: akjamie/base
```
