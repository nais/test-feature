# feature

Minimal, harmless Fasit feature for smoke-testing Fasit releases and deployments.

The chart intentionally renders no Kubernetes resources. Installing it only creates
the Helm release metadata, which is enough to test Fasit chart ingestion, rollout,
and deploy plumbing without touching workloads, RBAC, networking, or services.

## Release

Every push to `main` packages and pushes the Helm chart to:

```text
oci://europe-north1-docker.pkg.dev/nais-io/nais/feature/feature
```

No container image is built, so releases should be fast.

## Local checks

```sh
helm lint charts
helm template feature charts
```
