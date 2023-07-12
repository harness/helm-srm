# et-receiver

![Version: 0.5.0](https://img.shields.io/badge/Version-0.5.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 5.23.1](https://img.shields.io/badge/AppVersion-5.23.1-informational?style=flat-square)

A Helm chart for Kubernetes

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://harness.github.io/helm-common | harness-common | 1.x.x |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `true` |  |
| autoscaling.maxReplicas | int | `5` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| et.grpc.gitsyncAuthority | string | `"ng-manager:13002"` |  |
| et.grpc.gitsyncSSL | bool | `false` |  |
| et.grpc.gitsyncTarget | string | `"ng-manager:13002"` |  |
| et.hikari.connectionTimeout | int | `60000` |  |
| et.hikari.maximumPoolSize | int | `10` |  |
| et.java.heapSize | string | `"1600m"` |  |
| et.logLevel | string | `"INFO"` |  |
| et.redis.enabled | bool | `true` |  |
| et.redis.host | string | `nil` |  |
| et.redis.port | int | `6379` |  |
| et.redis.streamLength | int | `500` |  |
| et.redis.streamLengths.AddHit | int | `2500` |  |
| et.redis.streamLengths.AgentStats | int | `2500` |  |
| et.redis.streamLengths.Decompile | int | `1000` |  |
| et.redis.streamLengths.DeferredAgentStats | int | `1000` |  |
| et.redis.streamLengths.SQL_Insertion | int | `2500` |  |
| et.redis.streamLengths.SQL_LocInvInsertion | int | `2500` |  |
| et.redis.streamLengths.SQL_MetricInsertion | int | `2500` |  |
| et.redis.streamLengths.ServiceStats | int | `1000` |  |
| et.redis.trimCronExpression | string | `"@hourly"` |  |
| et.redis.useSentinel | bool | `true` |  |
| et.redisQueue.type | string | `"hit"` |  |
| extraVolumeMounts | list | `[]` |  |
| extraVolumes | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| global.database.postgres.extraArgs | string | `""` |  |
| global.database.postgres.hosts[0] | string | `"postgres:5432"` |  |
| global.database.postgres.installed | bool | `true` |  |
| global.database.postgres.passwordKey | string | `""` |  |
| global.database.postgres.protocol | string | `"postgres"` |  |
| global.database.postgres.secretName | string | `""` |  |
| global.database.postgres.userKey | string | `""` |  |
| global.imagePullSecrets | list | `[]` |  |
| global.kubeVersion | string | `""` |  |
| image.digest | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.registry | string | `"docker.io"` |  |
| image.repository | string | `"harness/et-receiver-signed"` |  |
| image.tag | string | `"5.3.0"` |  |
| imagePullSecrets | list | `[]` |  |
| lifecycleHooks | object | `{}` |  |
| livenessProbe.enabled | bool | `true` |  |
| livenessProbe.failureThreshold | int | `3` |  |
| livenessProbe.initialDelaySeconds | int | `40` |  |
| livenessProbe.periodSeconds | int | `10` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `1` |  |
| maxSurge | string | `"100%"` |  |
| maxUnavailable | int | `0` |  |
| name | string | `"et-receiver"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| postgresPassword.key | string | `"postgres-password"` |  |
| postgresPassword.name | string | `"postgres"` |  |
| readinessProbe.enabled | bool | `true` |  |
| readinessProbe.failureThreshold | int | `3` |  |
| readinessProbe.initialDelaySeconds | int | `35` |  |
| readinessProbe.periodSeconds | int | `5` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `1` |  |
| replicaCount | int | `1` |  |
| resources.limits.memory | string | `"2Gi"` |  |
| resources.requests.cpu | string | `"250m"` |  |
| resources.requests.memory | string | `"2Gi"` |  |
| securityContext.runAsNonRoot | bool | `true` |  |
| securityContext.runAsUser | int | `65534` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `false` |  |
| serviceAccount.name | string | `"harness-default"` |  |
| startupProbe.enabled | bool | `true` |  |
| startupProbe.failureThreshold | int | `10` |  |
| startupProbe.initialDelaySeconds | int | `40` |  |
| startupProbe.periodSeconds | int | `10` |  |
| startupProbe.successThreshold | int | `1` |  |
| startupProbe.timeoutSeconds | int | `1` |  |
| tolerations | list | `[]` |  |
| waitForInitContainer.image.digest | string | `""` |  |
| waitForInitContainer.image.pullPolicy | string | `"IfNotPresent"` |  |
| waitForInitContainer.image.registry | string | `"docker.io"` |  |
| waitForInitContainer.image.repository | string | `"harness/helm-init-container"` |  |
| waitForInitContainer.image.tag | string | `"latest"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)
