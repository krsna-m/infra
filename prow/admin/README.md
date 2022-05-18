# Admin

Prow is deployed [onto GKE](https://console.cloud.google.com/kubernetes/list/overview?project=knative-tests) with the following clusters:

- Prow (control plane cluster, the default prow cluster)
    - Prow itself, core configs, and plugins
- Prow-Build
    - Where most of the jobs are ran for testing, etc.
- Prow-Trusted
    - Small cluster that runs sensitive prow jobs and holds important secrets.

These are also the [Boskos projects (01-100)](https://console.cloud.google.com/kubernetes/list/overview?project=knative-boskos-01) that run e2e tests.

## Summary of current directory

- `deployment-definitions` are the collection of deployment definitions for the different Prow clusters that Prow uses (listed above).
