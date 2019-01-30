```comment
Startalk下一阶段开源预告：
各位星粉~~ Startalk自开源以来，受到大家的热情欢迎，为了回馈大家的信任，2019年春节后，我们将加大开源力度，开源功能包含：
* 红包
* AA付款(主要是界面部分)
* PC客户端
* 音视频
* 音视频会议和直播
* startalk全球网络加速服务（需单独订购）
```

Startalk是世界上最好的开源im系统级解决方案!

* [English Version](https://github.com/qunarcorp/qtalk/blob/master/README.en.md)
* [Startalk是啥](#Startalk(星语)——通用通信解决方案)
* [我们的使用场景](#我们的使用场景)
* [系统特性](#系统特性)
* [系统独有特性](#系统自有特点)
* [如何使用？](#如何使用？)
  * [部署环境要求](#部署环境要求)
  * [快速开始](#快速开始)
  * [官方网站](https://im.qunar.com/new/)
* [已有用户](#已有用户)


# Startalk(星语)——通用通信解决方案

沟通是人类最基础的需求——《人类简史》

Startalk 的目标是成为一款通用的，高性能的企业级im套件。也在努力改变当前大型im系统无完整开源解决方案的现状。

Startalk 前身是去哪儿的Qtalk，已在Qunar稳定运行3年多。

其内核也在去哪儿旅行和去哪儿网站上扮演着着客服服务工具的角色。

也就是说，一套内核同时为去哪儿网提供了内部企业办公和商家tob业务的支撑。


# 我们的使用场景
* 办公自动化OA
* 商业企业客服系统
* 各种im场景的SDK级嵌入

# 系统自有特点
* 开放源代码

```comment
我们正在逐步把工作重心从公司git转移到github上，希望可以为大家提供更稳定持久的服务。
```
* 只推荐私有化部署

```comment
企业有私有化部署的理由和需求，我们是希望帮助企业甚至团体在满足高效沟通和足够的扩展性上提供尽可能多的帮助。
```

# 如何使用？

Startalk专注于基于私有化部署。
这导致了startalk的登录过程略显复杂。
但是没关系，Startalk团队致力于把im系统设计门槛降低到很低的同时，也致力于降低首次接入时的成本。

通常，我们使用一款自有软件时，常见的接入方式分三步：
* 下载app
* 根据官方要求做一些设定
* 注册账号&登录

Startalk因为是私有化部署，服务器也需要部署在自己公司，这使得接入步骤变成了四步：
* 下载app
* 部署后台系统(新增)
* 通过后台配置，给客户端做一些设定
* 倒入账号&登录

如果您真的很希望做私有化接入，但是又不想在前期有一些投入和成本，可以考虑在公共环境中做试用或暂住：

* 加入[公共域](https://im.qunar.com/new/#/regist).

当您已经决定加入私有化部署，或者决定从公共环境中将数据迁移到私有环境：

* 开始[私有化部署!](https://github.com/qunarcorp/ejabberd-open#startalk-ejabberd).


## 部署环境要求
-   [后端](https://github.com/qunarcorp/ejabberd-open)服务器centos 7(未来会支持ubuntu,以及各种私有云)
-   [ios SDK](https://github.com/qunarcorp/imsdk-ios)  最低支持iOS9系统
-   最低[Android SDK](https://github.com/qunarcorp/imsdk-android)：
SDK要求最低API级别为16
-   编译[Android SDK](https://github.com/qunarcorp/imsdk-android)： SDK要求您针对API 26或更高版本进行编译
-   其他平台均可使用C++14进行编译。界面是[qt](https://qt.io/)

### 看到这里，您现在可能已经希望测试一番了。。。

## 快速开始
* [ejabberd](https://github.com/qunarcorp/ejabberd-open)  后端源码及介绍

* [imsdk-android](https://github.com/qunarcorp/imsdk-android) 安卓源码及介绍

* [imsdk-iOS](https://github.com/qunarcorp/imsdk-ios) iOS 源码及介绍

如果您不想费事，或者希望可以快速开始，那么可以进入我们的[官方网站](https://im.qunar.com/new/)注册公共域账号进行测试。

## [官方网站](https://im.qunar.com/new/)
我们针对不同层次的客户提供了不同层次的支持方式。
如果您感兴趣但是担心各种使用上的问题，可以移步[官网](https://im.qunar.com/new/)了解详情

## 系统特性

* 注重您的使用体验和信息安全
* 支持端到端加密方式。默认使用TLS连接，纯二进制协议
* 支持所有的消息类型，文本、表情、文件、音视频、图片、位置、红包、代码……；
* 支持全平台接入；
* 采用去中心化设计。支持私有云或公有云部署

# 已有用户

目前已广泛使用的主要厂商，如去哪儿、北工大、便利蜂、新晨航空、爱云动

![architecture](image/qunar.png)![architecture](image/blf.png)![architecture](image/sports.png)![architecture](image/bjgydx.png)![architecture](image/xchk.png)


### 包括以下扩展功能
-   企业OA
-   单聊及群聊
-   搜索
-   push
-   音视频
-   红包&AA收款
-   会话加密
-   组织架构



## 去中心化设计及部署方式
![architecture](image/arch.png)

Startalk 采用去中心化设计，将非状态服务合并到了Public中，状态服务进入了Domain中。Domain横向扩展，相互之间隔离

![architecture](image/deploy.png)

去中心化部署，只要有服务器，自己家里都能部署一套im服务



Startalk 后端模块

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

### 客户端简介
[客户端私有化配置](https://im.qunar.com/new/#/platform/access_guide/manage_nav?id=manage_nav_pc)
> 客户端SDK开源，目前仅开源移动端，PC端即将开源

#### android端
+ [imsdk-android](https://github.com/qunarcorp/imsdk-android)

安卓SDK

#### ios端
+ [imsdk-iOS](https://github.com/qunarcorp/imsdk-ios)

ios SDK

+ [libqimkit-ios-cook ](https://github.com/qunarcorp/libqimkit-ios-cook)

各个组件Pod库

+ [libqimcommoncategories](https://github.com/qunarcorp/libqimcommoncategories-ios)

扩展工具组件库

+ [libqimdatabase](https://github.com/qunarcorp/libqimdatabase-ios)

数据库组件库

+ [libqimopenssl](https://github.com/qunarcorp/libqimopenssl-ios)

适用于iOS/Mac的OpenSSL库


>PC及MAC端即将开源，如有需要，可先行下载客户端自主部署,下载地址:[https://im.qunar.com/new/#/download](https://im.qunar.com/new/#/download)
