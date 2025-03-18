# community-provisioners

This is a library of additional provisioners that you can use with either `score-compose` or `score-k8s`.

## For `score-compose`

| File                                          | Type                        | Class   | Params            | Outputs          |
| --------------------------------------------- | --------------------------- | ------- | ----------------- | ---------------- |
| `10-redis-dapr-pubsub.provisioners.yaml`      | `dapr-pubsub`               | (any)   | (none)            | `name`           |
| `10-redis-dapr-state-store.provisioners.yaml` | `dapr-state-store`          | (any)   | (none)            | `name`           |
| `10-dapr-subscription.provisioners.yaml`      | `dapr-subscription`         | (any)   | `pubsub`, `topic` | `name`, `topic`  |
| `10-env.provisioners.yaml`                    | `environment`               | (any)   | (none)            | (none)           |
| `10-hpa.provisioners.yaml`                    | `horizontal-pod-autoscaler` | (any)   | (none)            | (none)           |
| `10-service.provisioners.yaml`                | `service`                   | (any)   | (none)            | `name`           |

## For `score-k8s`

| File                                            | Type                        | Class   | Params                                                                 | Outputs                                 |
| ----------------------------------------------- | --------------------------- | ------- | ---------------------------------------------------------------------- | --------------------------------------- |
| `10-rabbitmq-dapr-pubsub.provisioners.yaml`     | `dapr-pubsub`               | (any)   | (none)                                                                 | `name`                                  |
| `10-redis-dapr-pubsub.provisioners.yaml`        | `dapr-pubsub`               | (any)   | (none)                                                                 | `name`                                  |
| `10-redis-dapr-state-store.provisioners.yaml`   | `dapr-state-store`          | (any)   | (none)                                                                 | `name`                                  |
| `10-dapr-subscription.provisioners.yaml`        | `dapr-subscription`         | (any)   | `pubsub`, `topic`                                                      | `name`, `topic`                         |
| `10-env.provisioners.yaml`                      | `environment`               | (any)   | (none)                                                                 | (none)                                  |
| `10-hpa.provisioners.yaml`                      | `horizontal-pod-autoscaler` | (any)   | `minReplicas`, `maxReplicas`, `defaultTargetCPUUtilizationPercentage`  | (none)                                  |
| `10-redis-helm-template.provisioners.yaml`      | `redis`                     | (any)   | (none)                                                                 | `host`, `port`, `username`, `password`  |
| `10-redis-helm-upgrade.provisioners.yaml`       | `redis`                     | (any)   | (none)                                                                 | `host`, `port`, `username`, `password`  |
| `10-shared-gateway-httproute.provisioners.yaml` | `route`                     | (any)   | `host`, `path`, `port`                                                 | (none)                                  |
| `10-service.provisioners.yaml`                  | `service`                   | (any)   | (none)                                                                 | `name`                                  |

## Examples

See all the examples about how to use them [here](./examples/).
