```bash
score-compose init --provisioners https://raw.githubusercontent.com/score-spec/community-provisioners/refs/heads/main/score-compose/10-redis-dapr-state-store.provisioners.yaml
# Other option: score-compose init --provisioners ./score-compose/10-redis-dapr-state-store.provisioners.yaml

score-compose generate score.yaml
```