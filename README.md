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
| docker-repo                    | Docker repository/image to deploy, if any (e.g. `my-org/my-app`)                                                                                                                                  | `false`  |                 |
| docker-tag                     | Docker image tag to deploy, if any (e.g. `0.9.14`)                                                                                                                                                | `false`  |                 |
| docker-server                  | Docker server, if any (e.g. `docker.io`)                                                                                                                                                          | `false`  |                 |
| docker-username                | Docker user, if any (e.g. `my-username`)                                                                                                                                                          | `false`  |                 |
| docker-password                | Docker password, if any (e.g. `abc123`)                                                                                                                                                           | `false`  |                 |
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
