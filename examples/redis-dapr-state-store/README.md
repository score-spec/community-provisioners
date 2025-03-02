## For `score-compose`
```bash
score-compose init --provisioners ../../score-compose/10-redis-dapr-state-store.provisioners.yaml

score-compose generate score.yaml
```

## For `score-k8s`
```bash
score-k8s init --provisioners ../../score-k8s/10-redis-dapr-state-store.provisioners.yaml

score-k8s generate score.yaml
```