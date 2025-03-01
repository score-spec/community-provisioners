## For `score-compose`
```bash
touch .env
echo "TEST=test" > .env

score-compose init --provisioners ../../score-compose/00-env.provisioners.yaml

score-compose generate score.yaml
```

## For `score-k8s`
```bash
touch .env
echo "TEST=test" > .env

score-k8s init --provisioners ../../score-k8s/00-env.provisioners.yaml

score-k8s generate score.yaml
```