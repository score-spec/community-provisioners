# community-provisioners

Thoughts:
- Tags:
    - `implementation`: `score-compose`|`score-k8s`
    - `provisioner type`: `template`|`python`|`helm`|`terraform`|`microcks-cli`
    - `resource type`: `environment`|`dapr-pubsub`|`redis`
- Display the `description`, `expected_outputs` and `supported_params`
- Maybe we don't want the default provisioners in the Hub, just the community ones?
- Add a comment header for each provisioner file where we could add more metadata? Like for other information not easy to supply/retrieve in addition to the ones above? Examples:
  - `valkey` falvor for `redis`
  - `rabbitmq` or `postgres` or `redis` for `dapr-state-store` or `dapr-pub-sub`
- Is the README required? Could we generate the command generically? And maybe if requirement/prerequisites, we could add a comment header for metadata?

TODOs:
- Multiple provisioners files:
    - redis
    - dapr-pub-sub
- CI
- OCI image
- New README/Score
  - route
  - redis
  - dapr-subscription
  - dapr-pubsub

This is a library of additional provisioners that you can use with either `score-compose` or `score-k8s`.

## For `score-compose`

| File | Type | Class | Params | Outputs | Description
| ---- | ---- | ----- | ------ | ------- | -----------
| 10-redis-dapr-pubsub.provisioners.yaml      | `dapr-pubsub`               | (any)   | (none)            | `name`           | Generates a Dapr PubSub `Component` pointing to a Redis `Service`.
| 10-redis-dapr-state-store.provisioners.yaml | `dapr-state-store`          | (any)   | (none)            | `name`           | Generates a Dapr StateStore `Component` pointing to a Redis `Service`.
| 10-dapr-subscription.provisioners.yaml      | `dapr-subscription`         | (any)   | `pubsub`, `topic` | `name`, `topic`  | Generates a Dapr `Subscription` on a given Topic and `PubSub`.
| 10-env.provisioners.yaml                    | `environment`               | (any)   | (none)            | (none)           | Loads environment variables from a local `.env` file.
| 10-hpa.provisioners.yaml                    | `horizontal-pod-autoscaler` | (any)   | (none)            | (none)           | Generates an empty object because HPA is not supported in Docker Compose.
| 10-service.provisioners.yaml                | `service`                   | (any)   | (none)            | `name`           | Outputs the name of the Workload dependency if it exists in the list of Workloads.

## For `score-k8s`

| File | Type | Class | Params | Outputs | Description
| ---- | ---- | ----- | ------ | ------- | -----------
| 10-rabbitmq-dapr-pubsub.provisioners.yaml     | `dapr-pubsub`               | (any)   | (none)                                                                 | `name`                                  | Generates a Dapr PubSub `Component` pointing to a RabbitMQ `StatefulSet`.
| 10-redis-dapr-pubsub.provisioners.yaml        | `dapr-pubsub`               | (any)   | (none)                                                                 | `name`                                  | Generates a Dapr PubSub `Component` pointing to a Redis `StatefulSet`.
| 10-redis-dapr-state-store.provisioners.yaml   | `dapr-state-store`          | (any)   | (none)                                                                 | `name`                                  | Generates a Dapr StateStore `Component` pointing to a Redis `StatefulSet`.
| 10-dapr-subscription.provisioners.yaml        | `dapr-subscription`         | (any)   | `pubsub`, `topic`                                                      | `name`, `topic`                         | Generates a Dapr `Subscription` on a given Topic and `PubSub`.
| 10-env.provisioners.yaml                      | `environment`               | (any)   | (none)                                                                 | (none)                                  | Loads environment variables from a local `.env` file.
| 10-hpa.provisioners.yaml                      | `horizontal-pod-autoscaler` | (any)   | `maxReplicas`, `minReplicas`, `defaultTargetCPUUtilizationPercentage`  | (none)                                  | Generates an `HorizontalPodAutoscaler` manifest.
| 10-redis-helm-template.provisioners.yaml      | `redis`                     | (any)   | (none)                                                                 | `host`, `password`, `port`, `username`  | Generates the manifests of the `bitnami/redis` Helm chart.
| 10-redis-helm-upgrade.provisioners.yaml       | `redis`                     | (any)   | (none)                                                                 | `host`, `password`, `port`, `username`  | Deploys the `bitnami/redis` Helm chart in an existing cluster.
| 10-shared-gateway-httproute.provisioners.yaml | `route`                     | (any)   | `host`, `path`, `port`                                                 | (none)                                  | Generates an `HTTPRoute` attached to a shared `Gateway`.
| 10-service.provisioners.yaml                  | `service`                   | (any)   | (none)                                                                 | `name`                                  | Outputs the name of the Workload dependency if it exists in the list of Workloads.

## Examples

See all the examples about how to use them [here](./examples/).
