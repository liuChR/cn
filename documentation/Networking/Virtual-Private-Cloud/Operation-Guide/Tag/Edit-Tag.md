# 编辑标签
当新申请的公网IP需要绑定标签，或者需要对已绑定的标签进行编辑，可通过编辑标签实现。

## 操作步骤

1. 访问[公网IP控制台](https://cns-console.jdcloud.com/host/pip/list)，即进入公网IP列表页面。或访问[京东云控制台](https://console.jdcloud.com)点击左侧导航栏【私有网络】-【弹性公网IP】进入公网IP列表页。
2. 选择地域。
3. 在公网IP列表中选择编辑标签的公网IP。
4. 单台操作：点击【操作】-【更多】-【编辑标签】按钮，或点击公网IP名称进入详情页后点击【操作】-【编辑标签】按钮。
5. 在弹出的“编辑标签”弹窗里，当前标签默认显示公网IP当前已绑定的标签，若当前公网IP当前标签内已有10个标签则【添加】按钮置灰。
6. 可根据已有标签直接下拉选择或者根据输入进行模糊匹配后选择对应标签键/值（Key-Value）进行添加标签，点击【添加】则将显示在当前标签内
7. 单击【确定】，将按照当前标签内显示情况完成编辑标签。

		请注意：
		* 同一个资源，标签键不能重复，编辑前后标签键（Key）相同而值不同则将以新的值覆盖旧的值。
		* 点击【添加】按钮不触发编辑标签，只有点击【确定】按钮会触发编辑标签，会根据编辑后的标签对当前公网IP先解绑不再需要的标签，后绑定新标签/覆盖原有标签。例：公网IP当前绑定了以下标签：“所有者：产品研发，用途：测试，操作人：管理员，环境：预发”，需要编辑成：“所有人：产品研发，用途：开发，操作人：管理员”，则将先操作解绑标签“环境：预发”，再操作绑定新标签/覆盖原有标签：“用途：开发”。若遇到网络抖动可能会遇到解绑成功而绑定/覆盖不成功的情况，此时还请再次操作编辑标签。

完成编辑标签后，您可以通过公网IP列表页/详情页查看标签是否编辑成功，也可以单击公网IP列表上方的【标签筛选】按钮[筛选资源](Filter-by-Tag.md)。请注意列表页若未显示标签信息项，可通过自定义列表选择显示标签，详细操作步骤请参见[查看资源](../Instance/Query-Instance-Info.md)。

## 相关参考
[根据标签筛选资源](Filter-by-Tag.md)

[查看资源](../Instance/Query-Instance-Info.md)


