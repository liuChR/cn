# 使用s3browser管理OSS

## 简介

s3browsers是一种易于使用的Amazon S3免费客户端。它提供了一个简单的服务Web服务接口，可以使用绝大部分的对存储空间（bucket）、对象(object)进行操作管理的功能。

## 安装

1.下载安装包

下载地址：https://s3browser.com/download.aspx

2.安装

点开安装即可

## 使用s3browser接入OSS
###  增加用户

#### 步骤 1 在左侧的 account 下拉菜单中点击“add new account”
![](../../../../image/Object-Storage-Service/OSS-124.png)

#### 步骤 2 在弹出的对话框中，填写相应参数：

![](../../../../image/Object-Storage-Service/OSS-125.png)
*  Account Name：显示名称，一般填自己的用户名即可。
*  Account Type: S3 Compatible Storage
* REST Endpoint ,填写京东云[兼容S3的服务域名](https://docs.jdcloud.com/cn/object-storage-service/regions-and-endpoints)。
* Signature Version: 选择Version 4
* Access Key ID: (京东云的AK)
* Secret Access Key: (京东云的SK)
* 是否使用HTTPS: OSS支持http和https,为了您的数据更加安全建议默认勾选，使用https

## 使用s3browsers管理OSS
### 存储空间操作
#### 创建存储空间（bucket）

![](../../../../image/Object-Storage-Service/OSS-126.jpg)

1.点击【New bucket】创建存储空间

![](../../../../image/Object-Storage-Service/OSS-126.jpg)

2.创建弹框中输入bucket name

**说明**
* 存储空间名称全局唯一，如果该名称已经被其他用户占用，将不能创建成功，请您根据[OSS命名规范](https://docs.jdcloud.com/cn/object-storage-service/put-bucket-2)，输入恰当的能够标识自身业务的名称。
* 存储空间创建时默认ACL 为私有读写，您可以根据自己的需求，在创建后更改空间访问权限。参见【设置存储空间的Acl】与【设置Bucket policy】

#### 设置存储空间的Acl
##### 操作步骤
1.在存储空间列表中，选中需要设置的bucket名称，单击右键，选择【edit Permissions(ACL)】。如图：

![](../../../../image/Object-Storage-Service/OSS-131.png)

2.按照OSS支持的规则设置，完成设置。

##### 仅支持设置规则：

* 私有读写，对应设置如图：

![](../../../../image/Object-Storage-Service/OSS-128.png)

* 公有读私有写，对应设置如图：

![](../../../../image/Object-Storage-Service/OSS-130.png)

* 公共读写，对应设置如图：

![](../../../../image/Object-Storage-Service/OSS-129.png)

* 如果您想实现精细化授权给其他用户，可利京东云IAM ，通过京东云控制台可完成设置，如果想仅需为其他京东云账号(包括主账号与子账号)授权OSS 资源的权限，并实现细粒度的灵活授权请参考【设置Bucket policy】


**说明**
设置Bucket ACL时，建议您通过OSS控制台或者SDK设置，相比使用s3browsers更加便捷高效。
同时您需要注意，目前对于OSS而言Bucket ACL 与Bucket policy 仅可通过其一管理存储空间权限，二者不可共存。如同时设置，s3browsers将出现报错并显示异常。

#### 设置Bucket policy

1.在存储空间列表中，选中需要设置的bucket名称，单击右键，选择【edit Bucket policy】。如图：

![](../../../../image/Object-Storage-Service/OSS-132.png)


2.参考[Bucket policy 规范](https://docs.jdcloud.com/cn/object-storage-service/access-control-base-on-bucket-policy),在如下表格中完成设置。

![](../../../../image/Object-Storage-Service/OSS-133.png)

#### 删除存储空间

**说明：**
OSS 存储空间的删除目前必须满足以下条件：

* 存储空间内为空，即无任何文件，包括没有未完成的complete 的分片。
* 存储空间未开启跨区域复制，即不是跨区域复制中的目标存储空间或源存储空间
* 存储空间内没有图片样式。

满足以上条件您可以执行删除存储空间，否则将失败。

##### 操作步骤

1.在存储空间列表中，选中需要设置的bucket名称，单击右键，选择【delete policy】。

1.点击下图中确定删除复选框，即可完成删除，如图：

![](../../../../image/Object-Storage-Service/OSS-134.png)









