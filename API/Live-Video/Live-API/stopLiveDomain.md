# stopLiveDomain


## 描述
停用域名

## 请求方式
PUT

## 请求地址
https://live.jdcloud-api.com/v1/domains:stop


## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**publishDomain**|String|True| |要停用的域名|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String|ruquestId|


## 返回码
|返回码|描述|
|---|---|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**503**|Service unavailable|
|**200**|OK|
|**500**|Internal server error|
