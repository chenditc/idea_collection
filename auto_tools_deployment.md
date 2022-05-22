## 痛点

基于过去的项目经验：[http://chendi.me/2020/05/23/on-premise-deployment-solution-change-v3/)(http://chendi.me/2020/05/23/on-premise-deployment-solution-change-v3/)
希望可以利用 kubernetes 的原生能力解决同样的问题：

1. 安装软件时需要用的脚本往往是一次性的，但是不容易进行版本管理，流程文档容易过时。例如下载依赖包，配置本地用户权限等。希望不需要文档也可以完成整个部署流程。
2. 在单机上的部署方式和在集群上基本相同。
3. 配置文件可以在线修改，同时进行版本控制，实现 Infrastructure as Code
4. 配置文件更新时，可以和以前的版本进行合并迁移，类似于 SQL migration


## 方案

老的解决方案往新方案迁移：

- 基于 Jenkins 的部署流程工具 -> 基于 k8s 的 helm 包，一个产品即一个 helm 包。
- 配置文件服务 -> 在 k8s 上部署一个 GitLab

## 应用场景

快速部署、配置、升级开源项目，例如带前端、后段、数据库的三层结构项目。
