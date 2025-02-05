# seldon-mab

![Version: 0.2.0](https://img.shields.io/badge/Version-0.2.0-informational?style=flat-square)

Chart to deploy a multi-armed bandits router over two Seldon Core v1 deployments,
so that traffic is sent to the best performing model.
You will need to utilize both the `predict` and `send_feedback` API methods.

**Homepage:** <https://github.com/SeldonIO/seldon-core>

## Source Code

* <https://github.com/SeldonIO/seldon-core>
* <https://github.com/SeldonIO/seldon-core/tree/master/helm-charts/seldon-mab>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| engine.env.SELDON_LOG_MESSAGES_EXTERNALLY | bool | `false` |  |
| engine.env.SELDON_LOG_MESSAGE_TYPE | string | `"seldon.message.pair"` |  |
| engine.env.SELDON_LOG_REQUESTS | bool | `false` |  |
| engine.env.SELDON_LOG_RESPONSES | bool | `false` |  |
| engine.resources.requests.cpu | string | `"0.1"` |  |
| mab.branches | int | `2` |  |
| mab.epsilon | float | `0.2` |  |
| mab.image.name | string | `"seldonio/mab_epsilon_greedy"` |  |
| mab.image.version | string | `"1.18.0"` |  |
| mab.name | string | `"eg-router"` |  |
| mab.verbose | int | `1` |  |
| modela.image.name | string | `"seldonio/mock_classifier"` |  |
| modela.image.version | string | `"1.18.0"` |  |
| modela.name | string | `"classifier-1"` |  |
| modelb.image.name | string | `"seldonio/mock_classifier"` |  |
| modelb.image.version | string | `"1.18.0"` |  |
| modelb.name | string | `"classifier-2"` |  |
| predictor.name | string | `"default"` |  |
| predictorLabels.fluentd | string | `"true"` |  |
| predictorLabels.version | string | `"1.18.0"` |  |
| replicas | int | `1` |  |
| sdepLabels.app | string | `"seldon"` |  |
