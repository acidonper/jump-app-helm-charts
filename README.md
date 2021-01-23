# Jump App Charts

## Introduction

_Jump App Charts_ repository includes a set of Helm charts to deploy and configure Jump App microservices and their CI/CD stuff in order to be possible to test, build, deploy and promote this microservices based application.

## Package helm repositories

- Generate helm packages

```$bash
helm package ./charts/jump-app-cicd
helm package ./charts/jump-app-micros
```

- Save files

```$bash
mv jump-app-*.tgz /tmp
```

- Checkout rh-pages branch and add new packages

```$bash
git checkout gh-pages
rm jump-app-*
mv /tmp/jump-app-cicd-0.1.0.tgz /tmp/jump-app-micros-0.1.0.tgz .
```

- Generate index file and push changes

```$bash
helm repo index . --url https://acidonper.github.io/jump-app-helm-charts
git add -A
git commit -m "Added new charts"
ggpush
```

## Author Information

Asier Cidon

asier.cidon@gmail.com
