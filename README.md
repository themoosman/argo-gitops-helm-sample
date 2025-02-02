# argo-gitops-helm-sample

## Overview
A sample Helm-based GitOps project for OpenShift utilizing the Red Hat OpenShift GitOps operator.

## Installation - Standalone Argo

### Setup Argo

```bash
# Log in to the cluster with cluster-admin

# cd to git source location, eg
cd ~/git/argo-gitops-helm-sample

# Install OpenShift GitOps Operator
oc apply -k setup/argocd

# wait for the Operator to install
```

### Setup GitOps Application

```bash
oc apply -f argocd/local-cluster/application.yaml
```

After the Argo Application is created, the helm chart will run and configure the cluster with the resources in the chart.