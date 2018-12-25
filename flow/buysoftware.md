<!-- TITLE: 服务器启动流程 -->
<!-- SUBTITLE: 描述服务器启动涉及到的默认数据插入和判断 -->

# 文件位置
[项目目录]/flows/softwareBuy.js
# 流程图
![Softwarebuy](/uploads/flows/softwarebuy.png "Softwarebuy")

# 涉及到的对象方法
* [User#isSuperAdminExists()](/User#is-super-admin-exists)
* [User#setSuperAdmin()](/User#set-super-admin)
* [App#isDefaultAppExists()](/app模型#is-default-app-exists)
* [App#createApp(params, ownerId, type)](/app模型#create-app-params-owner-id-type)
* [App#getOwner(appId)](/App#getOwner(appId))
* [AppOwner#bindAppForUser(appId, ownerId)](/AppOwner#bind-app-for-user-app-id-owner-id)
* [AppShop#getShopFromApp(appId, fields, match)](/AppShop#get-shop-from-app-app-id-fields-match)
* [Shop#createShop(params, appId)](/Shop#create-shop-params-app-id)
* [ShopGoodClass#getOneGoodClassFromShopId(shopId, fields, match)](/ShopGoodClass#get-one-good-class-from-shop-id-shop-id-fields-match)
* [GoodClass#createGoodClass(params, shopId)](/GoodClass#create-good-class-params-shop-id)
* [GoodClassGood#getOneGoodFromGoodClassId(goodClassId, fields, match)](/GoodClassGood#get-one-good-from-good-class-id-good-class-id-fields-match)
* [Good#createGood(params, goodClassId)](/Good#create-good-params-good-class-id)