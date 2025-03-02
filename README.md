# community-provisioners

This is additional provisioners that you can use with either `score-compose` or `score-k8s` accordingly.

For example, you can use the `dapr-state-store` by importing it like this:
```bash
score-compose init \
    --provisioners https://raw.githubusercontent.com/score-spec/community-provisioners/refs/heads/main/score-compose/10-redis-dapr-state-store.provisioners.yaml
```
Or:
```bash
score-compose init \
    --provisioners oci://ghcr.io/score-spec/score-compose-community-provisioners:latest#10-redis-dapr-state-store.provisioners.yaml
```

## For `score-compose`

| Type                        | Class   | Params  | Outputs |
| --------------------------- | ------- | ------- | ------- |
| `dapr-state-store`          | `redis` | (none)  | `name`  |
| `environment`               | (any)   | (none)  | (none)  |
| `horizontal-pod-autoscaler` | (any)   | (none)  | (none)  |
| `service`                   | (any)   | (none)  | `name`  |

## For `score-k8s`

| Type                        | Class   | Params                                                                 | Outputs |
| --------------------------- | ------- | ---------------------------------------------------------------------- | ------- |
| `dapr-state-store`          | `redis` | (none)                                                                 | `name`  |
| `environment`               | (any)   | (none)                                                                 | (none)  |
| `horizontal-pod-autoscaler` | (any)   | `minReplicas`, `maxReplicas`, `defaultTargetCPUUtilizationPercentage`  | (none)  |
| `service`                   | (any)   | (none)                                                                 | `name`  |
