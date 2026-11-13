# MyApp – httpd on OpenShift

![OpenShift](https://img.shields.io/badge/OpenShift-EE0000?logo=redhatopenshift&logoColor=white) ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white) ![Apache](https://img.shields.io/badge/Apache_httpd-D22128?logo=apache&logoColor=white)

> OpenShift manifests for an httpd Deployment exposed via ClusterIP and NodePort Services.

## Overview

Deploys **Apache httpd** from the OpenShift internal registry (CRC) as a Deployment, and exposes it with both a ClusterIP and a NodePort Service.

## Tech Stack

- **OpenShift**
- **Kubernetes**
- **Apache httpd**

## Repository Structure

```text
deploment.yml
myapp/deployment.yml
myapp/svc-np.yml
myapp/svc.yml
```

## Getting Started

```bash
git clone https://github.com/Gamal-Mohammad/myapp.git
cd myapp
```

### Deploy to OpenShift

| File | Kind | Name |
|---|---|---|
| `deploment.yml` | Deployment | `httpd-lb-deploy` |
| `myapp/deployment.yml` | Deployment | `httpd-lb-deploy` |
| `myapp/svc-np.yml` | Service | `svc-np` |
| `myapp/svc.yml` | Service | `httpd` |

```bash
oc apply -f deploment.yml
oc apply -f myapp/deployment.yml
oc apply -f myapp/svc-np.yml
oc apply -f myapp/svc.yml
oc get pods,svc
```

## Author

**Gamal Mohammad**

[![GitHub](https://img.shields.io/badge/GitHub-Gamal--Mohammad-181717?logo=github)](https://github.com/Gamal-Mohammad)
