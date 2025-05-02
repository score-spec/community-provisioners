```bash
score-compose init --provisioners https://raw.githubusercontent.com/score-spec/community-provisioners/refs/heads/main/score-compose/10-hpa.provisioners.yaml
# Other option: score-compose init --provisioners ./score-compose/10-hpa.provisioners.yaml

score-compose generate score.yaml
```