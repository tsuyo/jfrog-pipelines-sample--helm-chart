# JFrog Pipelines Sample: Helm Chart

Sources for [Deploying to Kubernetes in Pipelines](https://www.jfrog.com/confluence/display/JFROG/Deploying+to+Kubernetes+in+Pipelines)

## Prerequisites

- Integrations
  - tsuyo_github: GitHub
  - artifactory: Artifactory
- Repos 
  - sample-helm-local (helm/local)
  - sample-helm (helm/virtual)
    - includes: sample-helm-local
- K8s docker-registry secrets (see [Pull an Image from a Private Registry](https://kubernetes.io/docs/tasks/configure-pod-container/pull-image-private-registry/))
  - name: regcred, namespace: app
  ```
  $ kubectl create secret -n app docker-registry regcred --docker-server=<your-registry-server> --docker-username=<your-name> --docker-password=<your-pword> --docker-email=<your-email>
  ```