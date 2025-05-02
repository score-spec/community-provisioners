Prerequisites:
- Have `python` installed, this provisioner is using Python to load the `.env` file.

```bash
touch .env
echo "TEST=test" > .env

score-k8s init --provisioners https://raw.githubusercontent.com/score-spec/community-provisioners/refs/heads/main/score-k8s/10-env.provisioners.yaml
# Other option: score-k8s init --provisioners ../../score-k8s/10-env.provisioners.yaml

score-k8s generate score.yaml
```