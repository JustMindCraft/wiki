<!-- TITLE: 服务器启动流程 -->
<!-- SUBTITLE: 描述服务器启动涉及到的默认数据插入和判断 -->

# 文件位置
[项目目录]/bootstrap/fixture.js
# 流程图
![Serverstartupflow](/uploads/flows/serverstartupflow.png "Serverstartupflow")

# 涉及到的对象方法
* User#isSuperUserExists()
* User#setSuperAdmin()
* App#isDefaultAppExists()
* App#createApp(params, ownerId, type)
* App#getOwner(appId)
* AppOwner#bindAppForUser(appId, ownerId)
* AppShop#getShopFromApp(appId, fields, match)
* Shop#createShop(params, appId)
* ShopGoodClass#getOneGoodClassFromShopId(shopId, fields, match)
* GoodClass#createGoodClass(params, shopId)
* GoodClassGood#getOneGoodFromGoodClassId(goodClassId, Fields, match)
* Good#createGood(params, goodClassId)