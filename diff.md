# Diff from upstream

1. Update dependencies to use kcp kubernetes
2. `go mod vendor` so we can use vendored tooling, instead of published
3. update tools: `make update-codegen`
4. Add changes into the code

## Development:

1. Scale down existing cert-manager in the cluster
`kubectl scale deployment -n cert-manager cert-manager --replicas=0`
2. Get kubeconfig for virtualWorkspace
`go run ./cmd/controller/ --kubeconfig /.kcp/cert-manager.kubeconfig`
