Prerequisites:
- Have `helm` install locally, this provisioner installs the Bitnami Redis Helm chart.
- Have access to a cluster where the Helm chart will be installed.
    - If you don't have one, you can deploy a `Kind` cluster locally by running this script: `../../scripts/setup-kind-cluster.sh`.

```bash
score-k8s init --provisioners ../../score-k8s/10-redis-helm.provisioners.yaml

export NAMESPACE=default

score-k8s generate score.yaml

kubectl apply -f manifests.yaml -n ${NAMESPACE}
```