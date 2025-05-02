Prerequisites:
- Have `python` installed, this provisioner is using Python to load the `.env` file.

```bash
touch .env
echo "TEST=test" > .env

score-compose init --provisioners https://raw.githubusercontent.com/score-spec/community-provisioners/refs/heads/main/score-compose/10-env.provisioners.yaml
# Other option: score-compose init --provisioners ../../score-compose/10-env.provisioners.yaml

score-compose generate score.yaml
```