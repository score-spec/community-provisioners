## For `score-compose`
```bash
score-compose init --provisioners ../../score-compose/10-service.provisioners.yaml

score-compose generate score.yaml score-dep.yaml
```

## For `score-k8s`
```bash
score-k8s init --provisioners ../../score-k8s/10-service.provisioners.yaml

score-k8s generate score.yaml score-dep.yaml
```