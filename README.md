# Qtalk(暂定名)——通信工具解决方案

Qtalk的目标是成为一款高性能的企业级im套件。在Qunar稳定运行3年多，同时为去哪儿网内部企业办公和商家tob业务，用户端提供的售前及售后咨询

Qtalk is a high performance full platform enterprise level instant message software. It had been support qunar.com over 3 years for different customers, both internal and external communication supported. 
Qtalk support plugin style module extension, like office automation, customer care, imbedded into the other Apps etc.

# 我们的使用场景
* 办公自动化OA
* 商业企业客服系统
* 各种im场景的SDK级嵌入

# Qtalk的自有特点
* 开放源代码

```comment
我们正在逐步把工作重心从公司转移到github上，希望可以为大家提供更稳定持久的服务。
```
* 我们推荐私有化部署

```comment
企业有私有化部署的理由和需求，我们也是希望帮助企业甚至团体在满足高效沟通和足够的扩展性上提供尽可能多的帮助。
```

## 部署环境要求
-   后端服务器centos 7(未来会支持ubuntu,以及各种私有云)
-   QIMSDK最低支持iOS9系统
-   最低Android SDK：QTalk SDK要求最低API级别为16
-   编译Android SDK：QTalk SDK要求您针对API 26或更高版本进行编译


### 看到这里，您现在可能已经希望测试一番了。。。

## 快速开始
* [ejabberd](https://github.com/qunarcorp/ejabberd-open)  后端源码及介绍

* [imsdk-android](https://github.com/qunarcorp/imsdk-android) 安卓源码及介绍

* [imsdk-iOS](https://github.com/qunarcorp/imsdk-ios) iOS 源码及介绍

如果您不想费事，或者希望可以快速开始，那么可以进入我们的[官方网站](https://im.qunar.com/new/)注册公共域账号进行测试。


### Qtalk客户端
> QTalk客户端SDK开源，目前仅开源移动端，PC端即将开源

## Qtalk官方网址
Qtalk支持多种部署方式，欢迎官网了解详情

### QTalk后端
QTalk是基于ejabberd，根据业务需要改造而来。修改和扩展了很多 ejaberd不支持的功能

Qtalk基本支持所有的消息类型，文本、表情、文件、音视频、图片、位置、红包、代码……；支持全平台接入；Qtalk采用端到端加密方式，TLS连接，纯二进制协议

Qtalk采用去中心化设计，支持私有云或公有云部署

Qtalk主要提供以下功能：
-   单聊及群聊
-   搜索
-   push
-   音视频
-   红包&AA收款
-   会话加密
-   组织架构
-   企业OA


## 去中心化设计及部署方式
![architecture](image/arch.png)

Qtalk采用去中心化设计，将非状态服务合并到了Public中，状态服务进入了Domain中。Domain横向扩展，相互之间隔离

![architecture](image/deploy.png)

去中心化部署，只要有服务器，自己家里都能部署一套im服务



Qtalk后端模块

![architecture](image/arch_ejab.png)

+ [ejabberd](https://github.com/qunarcorp/ejabberd-open)

IM核心组件，负责维持与客户端的长连接和消息路由

+ [or](https://github.com/qunarcorp/or_open)

IM负载均衡组件，负责验证客户端身份，以及转发http请求到对应的后台服务
+ [im_http_service](https://github.com/qunarcorp/im_http_service_open)

IM HTTP接口服务，负责IM相关数据的查询、设置以及历史消息同步

+ [qtalk_cowboy](https://github.com/qunarcorp/qtalk_cowboy_open)(后面所有的接口都会迁移到im_http_service，这个服务会废弃)

IM HTTP接口服务，负责IM相关数据的查询、设置以及历史消息同步，后面会全部迁移到im_http_service上

+ [qfproxy](https://github.com/qunarcorp/qfproxy_open)

IM文件服务，负责文件的上传和下载

+ [qtalk_search](https://github.com/qunarcorp/qtalk_search)

提供远程搜索人员和群的服务

+ redis

IM缓存服务

+ postgresql

IM数据库服务

### Qtalk客户端
> QTalk客户端SDK开源，目前仅开源移动端，PC端即将开源

#### android端
+ [imsdk-android](https://github.com/qunarcorp/imsdk-android)

QTalk安卓SDK

#### ios端
+ [imsdk-iOS](https://github.com/qunarcorp/imsdk-ios)

QTalk ios SDK

+ [libqimkit-ios-cook ](https://github.com/qunarcorp/libqimkit-ios-cook)

QTalk各个组件Pod库

+ [libqimcommoncategories](https://github.com/qunarcorp/libqimcommoncategories-ios)

QTalk中扩展工具组件库

+ [libqimdatabase](https://github.com/qunarcorp/libqimdatabase-ios)

QTalk中数据库组件库

+ [libqimopenssl](https://github.com/qunarcorp/libqimopenssl-ios)

适用于iOS/Mac的OpenSSL库


>Qtalk PC及MAC端即将开源，如有需要，可先行下载客户端自主部署,下载地址:[https://im.qunar.com/new/#/download](https://im.qunar.com/new/#/download)



## 用户（已在生产环境使用）

Qtalk已广泛应用在各行各业的im在线沟通中，如去哪儿、北工大、便利蜂、新辰航空、爱运动

![architecture](image/qunar.png)![architecture](image/blf.png)![architecture](image/sports.png)![architecture](image/bjgydx.png)![architecture](image/xchk.png)
