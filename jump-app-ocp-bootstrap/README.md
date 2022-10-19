# Jump App Openshift Cluster Bootstrap

This Helm chart tries to collect the diferent Openshift objects to install and configure all components required to run Jump App.

## Introduction

*Jump App Openshift Cluster Bootstrap* chart deploys the following elements:

- Catalog Sources
- Subscriptions

## Install

- Install Helm Chart

```$bash
helm install jump-app-ocp-bootstrap . 
```

- Install Helm Chart applying objects in kubernetes

```$bash
helm template . --debug | oc apply -f -
```

## Local Tests

- Lint

```$bash
helm lint
```

- Dry run installations

```$bash
helm install jump-app-ocp-bootstrap . --dry-run --debug
```

- Render templates Locally

```$bash
helm template . --debug
```

## Author Information

Asier Cidon

asier.cidon@gmail.com
