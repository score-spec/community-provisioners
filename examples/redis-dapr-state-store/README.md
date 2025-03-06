## For `score-compose`
```bash
score-compose init --provisioners https://raw.githubusercontent.com/score-spec/community-provisioners/refs/heads/main/score-compose/10-redis-dapr-state-store.provisioners.yaml
# Other option: score-compose init --provisioners ../../score-compose/10-redis-dapr-state-store.provisioners.yaml

score-compose generate score.yaml
```

## For `score-k8s`
```bash
score-k8s init --provisioners https://raw.githubusercontent.com/score-spec/community-provisioners/refs/heads/main/score-k8s/10-redis-dapr-state-store.provisioners.yaml
# Other option: score-k8s init --provisioners ../../score-k8s/10-redis-dapr-state-store.provisioners.yaml

score-k8s generate score.yaml
```