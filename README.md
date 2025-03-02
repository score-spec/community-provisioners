# community-provisioners

This is a library of additional provisioners that you can use with either `score-compose` or `score-k8s` accordingly.

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

## Examples

See all the examples about how to use them [here](./examples/).