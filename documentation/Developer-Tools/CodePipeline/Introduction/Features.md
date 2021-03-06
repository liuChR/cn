# 功能
## 实现发布过程自动化
### 端到端的流水线
从代码提交、构建、测试、部署，实现完整的端到端的流水线功能。通过Webhook触发或者事件监听的方式，自动执行流水线。同时，流水线也提供人工把控的能力，通过在执行过程中加入手工审批操作的方式，支持用户手工测试或者手工部署至不同环境。
### 自定义流水线
根据用户在产品不同阶段的不同侧重点，支持灵活配置流水线。同一阶段内的任务可以设置为串行执行或并行执行，满足多种使用场景。
## 对接用户常用工具
### 多种源代码供应方
支持多种代码管理平台的集成，可以与Git、GitHub、京东云代码托管等平台无缝集成获取源码。
### 持续集成
支持 Java、Golang、NodeJs、Python等多种编译语言的构建及单元测试。支持Docker镜像编译，通过容器级资源隔离方式提供编译构建和安全检查。
### 持续部署
与京东云Kubernetes集群服务进行了深度集成，支持容器化应用的生命周期管理，打通容器环境下应用发布全过程自动化。
## 查看执行记录
### 查看流程执行进度
支持查看流水线的执行状态，查看接入操作的详细信息，运行记录等。
### 查看管道详细历史信息
支持查看流水线执行详细信息，包括开始时间和结束时间、执行持续时间和执行ID。
