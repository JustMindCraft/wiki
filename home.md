<!-- TITLE: 正觉云 -->
<!-- SUBTITLE: 概述 -->



# 正觉工场知识库
## 主要功能
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

## 本周任务列表2018/12/25~2018/12/31
- [x]  服务器启动流程图
- [x]  服务器启动流程图涉及的模型和方法的文档编写
- [ ]  代码重构服务器启动流程
- [ ]  手机号登录注册的流程图
- [ ]  手机号登录注册的流程图涉及的模型和方法的文档编写
- [ ]  编写手机登录注册方法和http API
- [ ]  重构手机登录注册界面
- [ ]  测试交付手机登录注册功能


## 里程碑
- [ ] 基础模型设计和API设计
- [ ] 官网注册登录以及快速购买应用
- [ ] 私有云服务，支持mp4播放和pdf播放
- [ ] 制作正觉APP1.0上线，支持Android和IOS
- [ ] 支持点对点社交和视频聊天
- [ ] 2.0正式上线

## 开发环境
###   系统要求

本系统基于nodejs语言和mongodb数据进行开发，使用nodejs的hapiJS框架，已经nodejs的mongodb的ORM作为数据驱动。

不建议使用windows环境进行开发，若是预装windows的PC，建议装vagrant开发环境，本文档所有的内容也会基于Linux/Unix 内核的操作系统进行介绍。

推荐的操作系统有MacOS， 以及linux 发型版： linux mint, ubuntu18.04， 以及基于ubuntu18.04的各类发型版， vagrant 环境推荐的box, 点击此处

若是您的PC的CPU不支持虚拟化，可以安装双系统。

本系统大部分技术资料在海外，请学会用[梯子科学上网](https://github.com/getlantern/download)

###  搭建教程
1. [Mac 下， nvm 安装 Node 及配置](https://www.jianshu.com/p/a3f8778bc0a1)
2. [ubuntu 下搭建 nodejs 环境](https://www.jianshu.com/p/e1c79e156e8f)
3. [Mac 下 安装 brew]([https://www.jianshu.com/p/ab50ea8b13d6)
4. [安装 vscode](https://jeasonstudio.gitbooks.io/vscode-cn-doc/content/md/%E7%BC%96%E8%BE%91%E5%99%A8/%E5%AE%89%E8%A3%85.html)
## 软件依赖及文档
1. [hapijs](https://hapijs.com/)
2. [mongoose](https://mongoosejs.com/])
3. [ipfs](https://ipfs.io/)

## 软件目录结构以及介绍

├── api  // api 路由文件
├── bin // 工具脚本
├── bootstrap // 启动脚本
├── config //设置
├── core // 核心
├── index.js //入口文件
├── models //模型类
├── node_modules //npm 模块
├── package.json
├── public //静态文件


## 开发规范

### 命名
### 封装
### 返回值
### 判断
### 循环


## 技术知识教程

* javascript 语言基础
* nodejs 环境搭建
* babel 基础
* ES5, ES6 语言基础
* 函数式编程入门
* typescript 基础

## 模型设计原则
a. 数据内容和模型关系完全分开
b. 总是有条件的查询
c. 除非验证为必要，不然总是有默认数据
d. 必须有验证
e. 所有模型必须包括以下字段，其后不再累述：

| 字段名    | 类型    | 解释     | 默认     | 验证 |
|-----------|---------|----------|----------|------|
| _id       | Object  | id       | 自动生成 | 必要 |
| createdAt | Date    | 创建时间 | 自动生成 | 必要 |
| updatedAt | Date    | 更新时间 | 自动生成 | 必要 |
| isDeleted | Boolean | 是否删除 | false    | 必要 |

## 基础模型
基础模型是指的是没有任何关联性关系的模型
###  应用模型——App
表示系统内所有的应用
* [文件位置](/app#文件位置)
* [字段表](/app#字段表)
* [方法](/app#方法)
* [关联的其他模型](/app#关联的其他模型)

### 系统设置模型——Setting
表示系统内所有的用户角色
* [文件位置](/setting#文件位置)
* [字段表](/setting#字段表)
* [方法](/setting#方法)
* [关联的其他模型](/setting#关联的其他模型)

### 角色模型——Role
表示系统内所有的用户角色
* [文件位置](/role#文件位置)
* [字段表](/role#字段表)
* [方法](/role#方法)
* [关联的其他模型](/role#关联的其他模型)


### 用户模型——User
表示系统内所有的用户
* [文件位置](/user#文件位置)
* [字段表](/user#字段表)
* [方法](/user#方法)
* [关联的其他模型](/user#关联的其他模型)
### 店铺模型——Shop
表示系统内所有的店铺
* [文件位置](/Shop#文件位置)
* [字段表](/Shop#字段表)
* [方法](/Shop#方法)
* [关联的其他模型](/Shop#关联的其他模型)
### 商店模型模型——Good
表示系统内所有的商品，以及所有用户能够购买，赠予，预定，领取的虚拟或者实体的所有指代
* [文件位置](/good#文件位置)
* [字段表](/app模型#字段表)
* [方法](/app模型#方法)
* [关联的其他模型](/app模型#关联的其他模型)

### 存储空间模型——Storage
表示系统内所有用户创建的文件存储空间
字段表
方法
### 文件模型模型——Document
字段表
方法
### 订单模型——Order
字段表
方法
### 货架模型——Shelf
字段表
方法
### 系统设置模型——Setting
字段表
方法
## 关系模型
### 应用拥有者模型——AppOwner
表示应用拥有者的关系模型
* [文件位置](/AppOwner%E6%A8%A1%E5%9E%8B#%E6%A8%A1%E5%9E%8B%E5%AE%9A%E4%B9%89%E7%9A%84%E6%96%87%E4%BB%B6%E4%BD%8D%E7%BD%AE)
* [字段表](/AppOwner模型#字段表)
* [方法](/AppOnwer模型#方法)
* [关联的其他模型](/AppOwner模型#关联的其他模型)
##  业务流程
###  服务器启动流程
*  [文件位置](/flow/serverStartup#文件位置)
*  [流程图](/flow/serverStartup#流程图)
*  [涉及的对象方法](/flow/serverStartup#涉及到的对象方法)


### 软件购买流程
*  [文件位置](/flow/buySoftWare#文件位置)
*  [流程图](/flow/buySoftWare#流程图)
*  [涉及的对象方法](/flow/buySoftWare#涉及到的对象方法)

### 新建应用流程
*  [文件位置](/flow/createApp#文件位置)
*  [流程图](/flow/createApp#流程图)
*  [涉及的对象方法](/flow/createApp涉及到的对象方法)


##  单元测试设计
##  场景业务设计
##  私有云存储设计
ipfs 节点
ipfs 开发要点
HLS 节点管理
webTorrent Tracker 管理
webTorrent HLS 管理
前端文件播放器
部署
##  前端开发环境搭建
typescript
react 以及 react native
material UI
ipfsAPI
前端原型线框页面截图
http(s) API 手册
##  生产环境部署
a. 描述
b. 搭建
c. 优化
## 迭代展望
d. 进一步的分布式
e. gunjs
f. webtorrent
g. nodejs on react native
h. rust on nodejs


