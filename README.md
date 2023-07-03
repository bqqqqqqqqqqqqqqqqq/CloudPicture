# CloudPicture

**应用网关**

 **cloud-photo-gateway**：基于springCloudgateway的API网关项目，框架Netty，异步阻塞模型，主要统一入口，负责路由转发，统一签名认证

**上层接口**

**cloud-photo-api**:提供API给相册前端项目，如，用户登录，相册列表，相册上传，下载，预览

**cloud-photo-audit**:提供管理员登陆，审核列表，审核图片，黑名单管理

**底层能力**

cloud-photo-trans：提供底层图片上传，下载能力，对接华为OBS存储；

cloud-photo-user：提供底层用户管理能力，如用户信息查询，登录等。

cloud-photo-image:提供底层图片缩略图生成，图片格式分析等能力

**其他**

**注册中心**：基于nacos/eureka提供服务的注册与发现功能；

消息kafka：对业务逻辑进行解耦异步处理，如上传后异步处理图片，审核

mysql/redis:数据持久化/数据缓存。