# community-provisioners

This is a library of additional provisioners that you can use with either `score-compose` or `score-k8s`.

## For `score-compose`

| File                                          | Type                        | Class   | Params  | Outputs |
| --------------------------------------------- | --------------------------- | ------- | ------- | ------- |
| `10-redis-dapr-state-store.provisioners.yaml` | `dapr-state-store`          | `redis` | (none)  | `name`  |
| `10-env.provisioners.yaml`                    | `environment`               | (any)   | (none)  | (none)  |
| `10-hpa.provisioners.yaml`                    | `horizontal-pod-autoscaler` | (any)   | (none)  | (none)  |
| `10-service.provisioners.yaml`                | `service`                   | (any)   | (none)  | `name`  |

## For `score-k8s`

| File                                          | Type                        | Class   | Params                                                                 | Outputs                                 |
| --------------------------------------------- | --------------------------- | ------- | ---------------------------------------------------------------------- | --------------------------------------- |
| `10-redis-dapr-state-store.provisioners.yaml` | `dapr-state-store`          | `redis` | (none)                                                                 | `name`                                  |
| `10-env.provisioners.yaml`                    | `environment`               | (any)   | (none)                                                                 | (none)                                  |
| `10-hpa.provisioners.yaml`                    | `horizontal-pod-autoscaler` | (any)   | `minReplicas`, `maxReplicas`, `defaultTargetCPUUtilizationPercentage`  | (none)                                  |
| `10-redis-helm.provisioners.yaml`             | `redis`                     | (any)   | (none)                                                                 | `host`, `port`, `username`, `password`  |
| `10-service.provisioners.yaml`                | `service`                   | (any)   | (none)                                                                 | `name`                                  |

## Examples

See all the examples about how to use them [here](./examples/).