# startVmInstanceById


## 描述
启动一台实例。实例状态必须为 已停止（Stopped），才可以调用该接口。

## 请求方式
PUT

## 请求地址
https://jdfusion.jdcloud-api.com/v1/regions/{regionId}/vm_instances/{id}:start

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**id**|String|True| |资源实例ID|
|**regionId**|String|True| |地域ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**authorization**|String|True| |获取方式请参考签名算法指导文档|
|**x-jdcloud-date**|String|True| |获取方式请参考签名算法指导文档|
|**x-jdcloud-fusion-cloudid**|String|True| |云注册信息ID|
|**x-jdcloud-nonce**|String|True| |获取方式请参考签名算法指导文档|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String|请求ID|


## 返回码
|返回码|描述|
|---|---|
|**204**|OK|
|**404**|instance not found|
