# Digital Earth Flux Example

Infrastructure as code for the modern Digital Earth

## Overview

Flux is used for continuous integration/continuous deployment
of Kubernetes resources (also known as GitOps, because it uses
Git to store and manage the configuration).

## Initialisation

First create a GitHub Personal Access Token with repo read, write
and admin, and export it like:

`export GITHUB_TOKEN=YOURTOKENGOESHERE`

Next, run the below command, with the `--path` changed to the cluster
you want to deploy.

```bash
flux bootstrap github \
  --owner=YOURGITHUBORGHERE \
  --repository=de-flux \
  --branch=main \
  --read-write-key \
  --path=clusters/staging 
```
