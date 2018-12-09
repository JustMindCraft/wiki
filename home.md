<!-- TITLE: 正觉云 -->
<!-- SUBTITLE: 概述 -->

# 正觉云知识库

## 1.  主要功能
### 系统设计目的所有面对的主要包括以下客户主体：

* 需要快速启动电商业务的企业主（50%）
* 需要快速获取电商销售团队的企业主（60%）
* 需要解决企业内部文件存储的企业主（20%）
* 需要获得企业内部管理效率的企业主（10%）
* 需要获得极其便宜而又高性能的软件服务的企业主（100%）
* 需要大量存储文件的个人或者企业（10%）
* 需要保证隐私安全的软件服务（5%）

### 为了服务这些对象，我们的技术被要求实现以下特点的大数据和区块链服务：

* 提供一整套数据服务API，使得用户可以创建，管理，甚至开发属于自己的应用。
* 提供一套简单的电商分销软件，使得用户可以一键创建属于自己的微商城。
* 提供企业云和个人云存储服务，使得用户可以上传下载自己的文件，并且分享给其他用户
* 提供简单的即时聊天功能和项目任务管理功能，使得小企业能够办公协同
* 使用分布式存储和胖客户端的计算能力大大降低软件的成本
* 使用区块链加密技术保障用户数据安全
* 逐步把数据去中心化，使得数据分布式在各个客户间，以保证平台责任中立



-----



## 2.  开发环境
### *  系统要求

本系统基于nodejs语言和mongodb数据进行开发，使用nodejs的hapiJS框架，已经nodejs的mongodb的ORM作为数据驱动。

不建议使用windows环境进行开发，若是预装windows的PC，建议装vagrant开发环境，本文档所有的内容也会基于Linux/Unix 内核的操作系统进行介绍。

推荐的操作系统有MacOS， 以及linux 发型版： linux mint, ubuntu18.04， 以及基于ubuntu18.04的各类发型版， vagrant 环境推荐的box, 点击此处

若是您的PC的CPU不支持虚拟化，可以安装双系统。

本系统大部分技术资料在海外，请学会用梯子科学上网

### * 搭建教程
1. Mac 下， nvm 安装 Node 及配置
2. ubuntu 下搭建 nodejs 环境
3. Mac 下 安装 brew
4. 安装 vscode
## 3. 软件依赖及文档
1. hapijs
2. mongoose
3. ipfs

## 4. 软件目录结构以及介绍

├── api  // api 路由文件
├── bin // 工具脚本
├── bootstrap // 启动脚本
├── config //设置
├── core // 核心
├── index.js //入口文件
├── models //模型类
├── node_modules //npm 模块
├── package.json
├── public

## 4. 模型设计原则
a. 数据内容和模型关系完全分开
b. 总是有条件的查询
c. 总是有默认数据
d. 必须有验证
e. 所有模型必须包括以下字段，其后不再累述：

## 5. 基础模型
基础模型是指的是没有任何关联性关系的模型
### 应用模型——App
方法
1. createApp(params, ownerId, type)——创建一个新的应用
2. 商店模型——Shop
字段表
方法
商品模型——Good
字段表
商品类别模型——GoodClass
字段表
方法
存储空间模型——Storage
字段表
方法
文件模型模型——Document
字段表
方法
订单模型——Order
字段表
方法
货架模型——Shelf
字段表
方法
系统设置模型——Setting
字段表
方法
关系模型
应用拥有者模型——AppOwner
默认数据
业务场景描述
单元测试设计
场景业务设计
私有云存储设计
ipfs 节点
ipfs 开发要点
HLS 节点管理
webTorrent Tracker 管理
webTorrent HLS 管理
前端文件播放器
部署
前端开发环境搭建
typescript
react 以及 react native
material UI
ipfsAPI
前端原型线框页面截图
http(s) API 手册
生产环境部署
a. 描述
b. 搭建
c. 优化
迭代展望
d. 进一步的分布式
e. gunjs
f. webtorrent
g. nodejs on react native
h. rust on nodejs


