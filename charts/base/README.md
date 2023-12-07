# base
Helm base chart for microservice.

# Kubernetes kinds supported as listed in below:

|Kind|Supported| Remark                        | 
|---|:---:|-------------------------------| 
|Role|Y|                               | 
|Role Binding|Y|                               | 
|Cluster Role| TBC |                               | 
|Cluster Role Binding | TBC|                               | 
|Deployment| Y |                               |
|Service|Y|                               |
|Ingress|Y|                               |
|Service Account|Y|                               |
|Persistent Volume Claim|Y| Support multiple PVC creation |
|Istio gateway| TBC||
|Virtual Service|TBC||
|Destination Rule|TBC||

# How to apply it in your services
Add it to chart dependency.
Configure your own values overrides.
Use helm template/install/uninstall to test it.
