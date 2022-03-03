# kf-pipelines-standalone

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

A Helm chart for deploying kubeflow pipelines standalone service.

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | minio | 10.1.9 |
| https://charts.bitnami.com/bitnami | mysql | 8.8.23 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| argo.affinity | object | `{}` |  |
| argo.argoworkflowcontroller.image | string | `"gcr.io/ml-pipeline/google/pipelines/argoworkflowcontroller:1.8.0"` |  |
| argo.executor.image | string | `"gcr.io/ml-pipeline/google/pipelines/argoexecutor:1.8.0"` |  |
| argo.nodeSelector | object | `{}` |  |
| argo.priorityClassName | object | `{}` |  |
| argo.resources | object | `{}` |  |
| argo.securityContext | object | `{}` |  |
| argo.tolerations | object | `{}` |  |
| executor.emissary | bool | `false` |  |
| managedstorage.enabled | bool | `false` |  |
| metadata.envoy.affinity | object | `{}` |  |
| metadata.envoy.image | string | `"gcr.io/ml-pipeline/google/pipelines/metadataenvoy:1.8.0"` |  |
| metadata.envoy.nodeSelector | object | `{}` |  |
| metadata.envoy.priorityClassName | object | `{}` |  |
| metadata.envoy.resources | object | `{}` |  |
| metadata.envoy.securityContext | object | `{}` |  |
| metadata.envoy.tolerations | object | `{}` |  |
| metadata.grpc.affinity | object | `{}` |  |
| metadata.grpc.image | string | `"gcr.io/ml-pipeline/google/pipelines/metadataserver:1.8.0"` |  |
| metadata.grpc.nodeSelector | object | `{}` |  |
| metadata.grpc.priorityClassName | object | `{}` |  |
| metadata.grpc.resources | object | `{}` |  |
| metadata.grpc.securityContext | object | `{}` |  |
| metadata.grpc.tolerations | object | `{}` |  |
| metadata.writer.affinity | object | `{}` |  |
| metadata.writer.image | string | `"gcr.io/ml-pipeline/google/pipelines/metadatawriter:1.8.0"` |  |
| metadata.writer.nodeSelector | object | `{}` |  |
| metadata.writer.priorityClassName | object | `{}` |  |
| metadata.writer.resources | object | `{}` |  |
| metadata.writer.securityContext | object | `{}` |  |
| metadata.writer.tolerations | object | `{}` |  |
| minio.disableWebUI | bool | `false` |  |
| minio.fullnameOverride | string | `"minio"` |  |
| minio.mode | string | `"standalone"` |  |
| minio.persistence.enabled | bool | `true` |  |
| minio.persistence.size | string | `"1Gi"` |  |
| minio.replicas | int | `4` |  |
| mysql.auth.database | string | `"kubeflow"` |  |
| mysql.auth.existingSecret | string | `"mysql-secret"` |  |
| mysql.auth.username | string | `"kubeflow"` |  |
| mysql.fullnameOverride | string | `"mysql"` |  |
| mysql.image.tag | float | `5.7` |  |
| pipeline.api.affinity | object | `{}` |  |
| pipeline.api.image | string | `"gcr.io/ml-pipeline/google/pipelines/apiserver:1.8.0"` |  |
| pipeline.api.nodeSelector | object | `{}` |  |
| pipeline.api.priorityClassName | object | `{}` |  |
| pipeline.api.resources | object | `{}` |  |
| pipeline.api.securityContext | object | `{}` |  |
| pipeline.api.tolerations | object | `{}` |  |
| pipeline.persistenceagent.affinity | object | `{}` |  |
| pipeline.persistenceagent.image | string | `"gcr.io/ml-pipeline/google/pipelines/persistenceagent:1.8.0"` |  |
| pipeline.persistenceagent.nodeSelector | object | `{}` |  |
| pipeline.persistenceagent.priorityClassName | object | `{}` |  |
| pipeline.persistenceagent.resources | object | `{}` |  |
| pipeline.persistenceagent.securityContext | object | `{}` |  |
| pipeline.persistenceagent.tolerations | object | `{}` |  |
| pipeline.scheduledworkflow.affinity | object | `{}` |  |
| pipeline.scheduledworkflow.image | string | `"gcr.io/ml-pipeline/google/pipelines/scheduledworkflow:1.8.0"` |  |
| pipeline.scheduledworkflow.nodeSelector | object | `{}` |  |
| pipeline.scheduledworkflow.priorityClassName | object | `{}` |  |
| pipeline.scheduledworkflow.resources | object | `{}` |  |
| pipeline.scheduledworkflow.securityContext | object | `{}` |  |
| pipeline.scheduledworkflow.tolerations | object | `{}` |  |
| pipeline.ui.affinity | object | `{}` |  |
| pipeline.ui.image | string | `"gcr.io/ml-pipeline/google/pipelines/frontend:1.8.0"` |  |
| pipeline.ui.ingress.tls.certsSecret | string | `nil` |  |
| pipeline.ui.nodeSelector | object | `{}` |  |
| pipeline.ui.priorityClassName | object | `{}` |  |
| pipeline.ui.resources | object | `{}` |  |
| pipeline.ui.securityContext | object | `{}` |  |
| pipeline.ui.tolerations | object | `{}` |  |
| pipeline.viewer.affinity | object | `{}` |  |
| pipeline.viewer.image | string | `"gcr.io/ml-pipeline/google/pipelines/viewercrd:1.8.0"` |  |
| pipeline.viewer.nodeSelector | object | `{}` |  |
| pipeline.viewer.priorityClassName | object | `{}` |  |
| pipeline.viewer.resources | object | `{}` |  |
| pipeline.viewer.securityContext | object | `{}` |  |
| pipeline.viewer.tolerations | object | `{}` |  |
| pipeline.visualisationserver.affinity | object | `{}` |  |
| pipeline.visualisationserver.image | string | `"gcr.io/ml-pipeline/google/pipelines/visualizationserver:1.8.0"` |  |
| pipeline.visualisationserver.nodeSelector | object | `{}` |  |
| pipeline.visualisationserver.priorityClassName | object | `{}` |  |
| pipeline.visualisationserver.resources | object | `{}` |  |
| pipeline.visualisationserver.securityContext | object | `{}` |  |
| pipeline.visualisationserver.tolerations | object | `{}` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.6.0](https://github.com/norwoodj/helm-docs/releases/v1.6.0)
