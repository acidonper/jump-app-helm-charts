# Jump App CI/CD Chart

## Introduction

*Jump App CI/CD* chart deploys Jump App's microservices CI/CD stuff based on Tekton in order to download source code, test, build, deploy and promote microservices in Jum App. The following object will be managed by this chart:

- ServiceAccounts
- RoleBindings
- BuildConfig
- Tasks and Conditions
- Pipelines and PipelinesRun
- TriggerBindings and TriggerTemplates
- EventListeners and Routes

## Install

- Install Helm Chart

```$bash
helm install jump-app-cicd-1 . --namespace jump-app-cicd --create-namespace
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
helm install jump-app-test-1 . --dry-run --debug --namespace test-dev --create-namespace
```

- Render templates Locally

```$bash
helm template . --debug
```

## Author Information

Asier Cidon @Red Hat

asier.cidon@gmail.com
