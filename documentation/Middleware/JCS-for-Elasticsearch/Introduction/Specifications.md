## 产品规格
京东云搜索Elasticsearch提供了多种节点实例规格，用户可以按需配置自定义节点的存储空间，满足不同业务场景需求。

* ES节点支持6种通用计算规格 ：1核2G、2核4G、2核8G、4核16G、8核32G、16核64G。其中，1核2G仅用于测试，不适用于生产环境。

* 节点数量限制为1-15，由于ES集群通常是分布式多节点构成的，因此需要有主节点对集群进行统一管理，为了保障集群的稳定性，建议您至少选择3个节点。

* 单点存储，采用ZBS服务(20-1000G SSD)(步长为10GB)。
