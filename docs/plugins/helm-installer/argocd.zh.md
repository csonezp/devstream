# 使用 DevStream 部署 Argo CD

## 前缀匹配

`instanceID` 的前缀需要是 `argocd`，最小化 tools 配置示例：

```yaml
tools:
- name: helm-installer
  instanceID: argocd
```

## 默认配置

| 配置项              | 默认值                    | 描述                                 |
| ----               | ----                     | ----                                |
| chart.chartPath    | ""                       | 本地 chart 包路径                     |
| chart.chartName    | argo/argo-cd             | chart 包名称                         |
| chart.version      | ""                       | chart 包版本                         |
| chart.timeout      | 10m                      | helm install 的超时时间               |
| chart.upgradeCRDs  | true                     | 是否更新 CRDs（如果有）                |
| chart.releaseName  | argocd                   | helm 发布名称                         |
| chart.namespace    | argocd                   | 部署的命名空间                         |
| chart.wait         | true                     | 是否等待部署完成                       |
| repo.url           | https://argoproj.github.io/argo-helm | helm 仓库地址             |
| repo.name          | argo                     | helm 仓库名                           |
