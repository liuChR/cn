# 触发器的增删改查

触发器（triger）定义了事件源触发函数的规则。通过操作控制台、API/SDK可实现触发器的增删改查。本章节介绍通过控制台对触发器进行增、删、改、查。

准备工作:

1. 创建API网关触发器之前，需要开通API网关服务，并在API网关服务中创建分组及API。创建过程请参考[创建API分组](../../../../../../documentation/Internet-Middleware/API-Gateway/Operation-Guide/Create-APIGroup/Create-APIGroup.md)及[创建API](../../../../../../documentation/Internet-Middleware/API-Gateway/Operation-Guide/Create-API/Create-API.md)。

2. 创建OSS触发器之前，需要开通对象存储服务，并且在对象存储服务中创建存储桶。创建过程请参考[创建存储空间](../../../../../../documentation/Storage-and-CDN/Object-Storage-Service/Operation-Guide/Manage-Bucket/Create-Bucket.md)。

 

## 创建触发器：

创建触发器规定了事件源事件触发函数的方式，事件根据事件源类型同步或异步触发函数运行，并在函数触发执行时，将event事件作为入参传递给入口函数。

1. 用户登陆函数服务，进入“函数列表“页面。

2. 在函数列表中选择要配置的函数，单击函数名称进入该函数详情页。

3. 在函数详情页中，选择要配置触发的函数的版本或别名后，单击“触发器“tab页。

4. 在“触发器“tab页中，单击”创建触发器“，弹出”创建触发器“弹窗。

5. 填写触发器信息，开始创建一个新的触发器，不同触发方式，对应的触发器配置信息不同，详情参见[事件源服务](../triggermanagement/eventsourceservice/eventsource-service.md)。

6. 单击“保存“，创建触发器。

 

## 删除触发器：

通过删除触发器可解绑事件源事件与函数的调用关系，删除触发器后，该触发器定义的事件源触发方式将不再触发函数运行。

1. 在“触发器”页，选择待删除触发器，单击“删除”，弹出“删除触发器”界面。

2. 根据提示完成确认，单击“确定”，完成触发器删除操作。

 

## 查询及更新触发器：

查询触发器：已创建的触发器，可在触发器页面的触发器列表中查询配置。

更新触发器：在触发器页面的触发器列表中选择需要更新的触发器，单击“编辑“，进行触发器配置更新。其中：API网关触发器创建后不可编辑，只能删除。为保证您的业务运行，请先下线已发布的API，再删除触发器，详情请参见API网关。