<!-- TITLE: 服务器启动流程 -->
<!-- SUBTITLE: 描述服务器启动涉及到的默认数据插入和判断 -->

# 文件位置
[项目目录]/bootstrap/fixture.js
# 流程图
![Serverstartupflow](/uploads/flows/serverstartupflow.png "Serverstartupflow")

# 涉及到的对象方法
* [User#setSuperAdmin()](/User#setSuperAdmin())
* [App#isDefaultAppExists()](/App#isDefaultAppExists())
* [App#createApp(params, ownerId, type)](/App#create-app-params-ownerid-type)
* [App#getOwner(appId)](/App#getOwner(appId))
* [AppOwner#bindAppForUser(appId, ownerId)](/AppOwner#bindAppForUser(appId, ownerId))
* [AppShop#getShopFromApp(appId, fields, match)](/AppShop#getShopFromApp(appId, fields, match))
* [Shop#createShop(params, appId)](/Shop#createShop(params, appId))
* [ShopGoodClass#getOneGoodClassFromShopId(shopId, fields, match)](/ShopGoodClass#getOneGoodClassFromShopId(shopId, fields, match))
* [GoodClass#createGoodClass(params, shopId)](/GoodClass#createGoodClass(params, shopId))
* [GoodClassGood#getOneGoodFromGoodClassId(goodClassId, Fields, match)](/GoodClassGood#getOneGoodFromGoodClassId(goodClassId, Fields, match))
* [Good#createGood(params, goodClassId)](/Good#createGood(params, goodClassId))