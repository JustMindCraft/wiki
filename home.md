<!-- TITLE: 正觉云 -->
<!-- SUBTITLE: 概述 -->

# 正觉工场知识库

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
###   系统要求

本系统基于nodejs语言和mongodb数据进行开发，使用nodejs的hapiJS框架，已经nodejs的mongodb的ORM作为数据驱动。

不建议使用windows环境进行开发，若是预装windows的PC，建议装vagrant开发环境，本文档所有的内容也会基于Linux/Unix 内核的操作系统进行介绍。

推荐的操作系统有MacOS， 以及linux 发型版： linux mint, ubuntu18.04， 以及基于ubuntu18.04的各类发型版， vagrant 环境推荐的box, 点击此处

若是您的PC的CPU不支持虚拟化，可以安装双系统。

本系统大部分技术资料在海外，请学会用[https://github.com/getlantern/download] (梯子科学上网)

###  搭建教程
1. [https://www.jianshu.com/p/a3f8778bc0a1] (Mac 下， nvm 安装 Node 及配置)
2. [https://www.jianshu.com/p/e1c79e156e8f] (ubuntu 下搭建 nodejs 环境)
3. [https://www.jianshu.com/p/ab50ea8b13d6] (Mac 下 安装 brew)
4. [https://jeasonstudio.gitbooks.io/vscode-cn-doc/content/md/%E7%BC%96%E8%BE%91%E5%99%A8/%E5%AE%89%E8%A3%85.html] (安装 vscode)
## 3. 软件依赖及文档
1. [https://hapijs.com/] (hapijs)
2. [https://mongoosejs.com/] (mongoose)
3. [https://ipfs.io/] (ipfs)

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
├── public //静态文件

## 5. 模型设计原则
a. 数据内容和模型关系完全分开
b. 总是有条件的查询
c. 总是有默认数据
d. 必须有验证
e. 所有模型必须包括以下字段，其后不再累述：

| 字段名    | 类型    | 解释     | 默认     | 验证 |
|-----------|---------|----------|----------|------|
| _id       | Object  | id       | 自动生成 | 必要 |
| createdAt | Date    | 创建时间 | 自动生成 | 必要 |
| updatedAt | Date    | 更新时间 | 自动生成 | 必要 |
| isDeleted | Boolean | 是否删除 | false    | 必要 |

## 6. 基础模型
基础模型是指的是没有任何关联性关系的模型
###  应用模型——App
表示系统内所有的应用
* [文件位置](/app%E6%A8%A1%E5%9E%8B#%E6%A8%A1%E5%9E%8B%E5%AE%9A%E4%B9%89%E7%9A%84%E6%96%87%E4%BB%B6%E4%BD%8D%E7%BD%AE)
* [字段表](/app模型#字段表)
* [方法](/app模型#方法)
* [关联的其他模型](/app模型#关联的其他模型)

### 系统设置模型——Setting
表示系统内所有的用户角色
* [文件位置](/Setting%E6%A8%A1%E5%9E%8B#%E6%A8%A1%E5%9E%8B%E5%AE%9A%E4%B9%89%E7%9A%84%E6%96%87%E4%BB%B6%E4%BD%8D%E7%BD%AE)
* [字段表](/Setting模型#字段表)
* [方法](/Setting模型#方法)
* [关联的其他模型](/Setting模型#关联的其他模型)

### 角色模型——Role
表示系统内所有的用户角色
* [文件位置](/Role%E6%A8%A1%E5%9E%8B#%E6%A8%A1%E5%9E%8B%E5%AE%9A%E4%B9%89%E7%9A%84%E6%96%87%E4%BB%B6%E4%BD%8D%E7%BD%AE)
* [字段表](/Role模型#字段表)
* [方法](/Role模型#方法)
* [关联的其他模型](/Role模型#关联的其他模型)


### 用户模型——User
表示系统内所有的用户
* [文件位置](/app%E6%A8%A1%E5%9E%8B#%E6%A8%A1%E5%9E%8B%E5%AE%9A%E4%B9%89%E7%9A%84%E6%96%87%E4%BB%B6%E4%BD%8D%E7%BD%AE)
* [字段表](/app模型#字段表)
* [方法](/app模型#方法)
* [关联的其他模型](/app模型#关联的其他模型)
### 店铺模型——Shop
表示系统内所有的店铺
* [文件位置](/app%E6%A8%A1%E5%9E%8B#%E6%A8%A1%E5%9E%8B%E5%AE%9A%E4%B9%89%E7%9A%84%E6%96%87%E4%BB%B6%E4%BD%8D%E7%BD%AE)
* [字段表](/app模型#字段表)
* [方法](/app模型#方法)
* [关联的其他模型](/app模型#关联的其他模型)
### 商店模型模型——Good
表示系统内所有的商品，以及所有用户能够购买，赠予，预定，领取的虚拟或者实体的所有指代
* [文件位置](/app%E6%A8%A1%E5%9E%8B#%E6%A8%A1%E5%9E%8B%E5%AE%9A%E4%B9%89%E7%9A%84%E6%96%87%E4%BB%B6%E4%BD%8D%E7%BD%AE)
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
## 7. 关系模型
### 应用拥有者模型——AppOwner
表示系统内所有的用户角色
* [文件位置](/AppOwner%E6%A8%A1%E5%9E%8B#%E6%A8%A1%E5%9E%8B%E5%AE%9A%E4%B9%89%E7%9A%84%E6%96%87%E4%BB%B6%E4%BD%8D%E7%BD%AE)
* [字段表](/AppOwner模型#字段表)
* [方法](/AppOnwer模型#方法)
* [关联的其他模型](/AppOwner模型#关联的其他模型)
## 8. 默认数据
## 9. 业务场景描述
## 10. 单元测试设计
## 11. 场景业务设计
## 12. 私有云存储设计
ipfs 节点
ipfs 开发要点
HLS 节点管理
webTorrent Tracker 管理
webTorrent HLS 管理
前端文件播放器
部署
## 13. 前端开发环境搭建
typescript
react 以及 react native
material UI
ipfsAPI
前端原型线框页面截图
http(s) API 手册
## 14. 生产环境部署
a. 描述
b. 搭建
c. 优化
## 15. 迭代展望
d. 进一步的分布式
e. gunjs
f. webtorrent
g. nodejs on react native
h. rust on nodejs


