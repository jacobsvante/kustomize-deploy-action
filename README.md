<!-- action-docs-description -->

## Description

Deploy to Kubernetes cluster using a Kustomize config

<!-- action-docs-description -->

<!-- action-docs-inputs -->

## Inputs

| parameter                      | description                                                                                                                                                                                       | required | default         |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- | --------------- |
| kubeconfig                     | Contents of the cluster's kubeconfig                                                                                                                                                              | `true`   |                 |
| kustomization-dir              | Path to the kustomize directory to apply / deploy (e.g. `kustomize/overlays/production`)                                                                                                          | `true`   |                 |
| image-tag                      | Docker image tag to deploy (e.g. `0.9.14`)                                                                                                                                                        | `true`   |                 |
| docker-server                  | Docker server (e.g. `docker.io`)                                                                                                                                                                  | `true`   |                 |
| docker-repo                    | Docker repository (e.g. `my-org/my-app`)                                                                                                                                                          | `true`   |                 |
| docker-username                | Docker user (e.g. `my-username`)                                                                                                                                                                  | `true`   |                 |
| docker-password                | Docker password (e.g. `abc123`)                                                                                                                                                                   | `true`   |                 |
| pre-deploy-delete-job-selector | Delete jobs with `status.successful=1` and the given label (e.g. `autodelete-successful-on-deploy=yes`), before doing the deploy. Useful for cleaning up completed db migration jobs and similar. | `false`  |                 |
| kustomization-base-dir         | Path to base kustomize directory                                                                                                                                                                  | `true`   | kustomize/base  |
| age-secret-key                 | Secret key to decrypt deploy secrets with (e.g. `AGE-SECRET-KEY-123456`)                                                                                                                          | `false`  |                 |
| encrypted-filename             | Filename/subpath inside `kustomization-dir` to a file with age encrypted secrets to decrypt                                                                                                       | `true`   | secrets.env     |
| decrypted-filename             | Filename/subpath inside `kustomization-dir` to which the age encrypted secrets will be decrypted to                                                                                               | `true`   | secrets.env.dec |
| create-k8s-namespace           | Create Kubernetes namespace if it does not exist                                                                                                                                                  | `true`   | true            |
| create-image-pull-secret       | Create an image pull secret named "rg.`$region`.scw.cloud", to be referenced in `imagePullSecrets` in a k8s deployment/job                                                                        | `true`   | true            |
| kubectl                        | Version of kubectl                                                                                                                                                                                | `true`   | latest          |
| kubectl-dry-run                | Used to set `kubectl` option `--dry-run` Valid values are `none` (default), `client` and `server`.                                                                                                | `true`   | none            |

<!-- action-docs-inputs -->

<!-- action-docs-outputs -->

<!-- action-docs-outputs -->

<!-- action-docs-runs -->

## Runs

This action is a `composite` action.

<!-- action-docs-runs -->
