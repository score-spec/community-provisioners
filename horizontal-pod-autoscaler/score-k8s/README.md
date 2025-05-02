```bash
score-k8s init --provisioners https://raw.githubusercontent.com/score-spec/community-provisioners/refs/heads/main/score-k8s/10-hpa.provisioners.yaml
# Other option: score-k8s init --provisioners ./score-k8s/10-hpa.provisioners.yaml

score-k8s generate score.yaml
```