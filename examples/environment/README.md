Prerequisites:
- Have `python` installed, this provisioner is using Python to load the `.env` file.

## For `score-compose`
```bash
touch .env
echo "TEST=test" > .env

score-compose init --provisioners https://raw.githubusercontent.com/score-spec/community-provisioners/refs/heads/main/score-compose/10-env.provisioners.yaml
# Other option: score-compose init --provisioners ../../score-compose/10-env.provisioners.yaml

score-compose generate score.yaml
```

## For `score-k8s`
```bash
touch .env
echo "TEST=test" > .env

score-k8s init --provisioners https://raw.githubusercontent.com/score-spec/community-provisioners/refs/heads/main/score-k8s/10-env.provisioners.yaml
# Other option: score-k8s init --provisioners ../../score-k8s/10-env.provisioners.yaml

score-k8s generate score.yaml
```