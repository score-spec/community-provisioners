Prerequisites:
- Have `helm` installed locally, this provisioner renders the manifests from the [Bitnami's Redis Helm chart](https://bitnami.com/stack/redis/helm).
- Have `yq` installed locally.

```bash
score-k8s init --provisioners https://raw.githubusercontent.com/score-spec/community-provisioners/refs/heads/main/score-k8s/10-redis-helm-template.provisioners.yaml
# Other option: score-k8s init --provisioners ../../score-k8s/10-redis-helm-template.provisioners.yaml

score-k8s generate score.yaml
```