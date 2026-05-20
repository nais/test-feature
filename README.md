# test-feature

Minimal, harmless Fasit test feature. Creates a single ConfigMap with a
configurable `message` value — useful for verifying Fasit end-to-end.

## Release

Every push to `main` packages, and pushes the Helm chart, then
deploys via Fasit (ci-nais first, then all tenant environments).
