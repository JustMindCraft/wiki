<!-- TITLE: 服务器启动流程 -->
<!-- SUBTITLE: 描述服务器启动涉及到的默认数据插入和判断 -->

# 文件位置
[项目目录]/bootstrap/fixture.js
# 流程图
![Serverstartupflow](https://www.plantuml.com/plantuml/png/hPVRJzDG7CUVsxzY2I_ZNy0N4CNue3uGt_RIR6UiORHBsmKIOp9KS8IBABWjWXSYDnCPOWnA5-IVsMct_y9pQyzfUtOH20yxf-lv_cwVxmaRjntDSifpHLKbArNLysdlQyNxVD1TMlSlcrxjTRjrRWEGyngdSFEm-_BI_tu8DwkTmqNlx4N6oEiBJja28za2oCvEe_T6Kqu166dwrgWAYZP8j_-i1tlRCKigC79wNbLBAABkwAQHWjMFy6WLhjKwvqk-U-Gtz_pDPVYseHkwCrqk0MiYDwSRgMUgWl9xQWDhHBVvy_iBkktO6KDLO7NVgvs88ZHjUDA0kySqjLIQxLH5gZQbEvCcgci62_PKfFM8JGhKWqeL9LwxeYXZ95ovbDCSm4DcZEvk1NVqouMttXH5lPrVNkr7s8_srPwtU7e7QvCMXY5uIIn4rWAn4B2w0rikLllmAXH4KcmOwdFfGBgjHgUv3zrjV_kOzN-YL48Dou6yLYuwQ1DlltXaOFlZOhBk9mMlstqSZJOVhGPrNGoBUZPKxt40slh7O9x44DikAeQTPrruCc-WiSq0XomoHcVZDtnJY-NWhHvukokToX9pcVTp3-tvKvMcGBNcj5c0MK0xaacd-IrcBtemdXKkAwugvgYnnKFxaUPa2wYDqIIvF1t-sWNgBKkOROJny2T2wdH6P3rbMYHxwKn4ZiEnq0_qrvVezylGhJEYfmicfl0UfH3l0gR5bvCiHr5EgWWm9uLwCTmNuJ4IXDqVQ8dwCe3UUdVB7G9TAink3I8i0nUBnS4b1n6tb352BIjpfGBFFg7JT5nHPCbtx0j6BH72qEB5NL0qZHcYsRwyWd_hOWFHqRQx8UEM5XHN5nBLw6U2NLmPVBSckRla-ChuJG2CxpFJOdDAJ8LMaRmMOYGFk9Z9VDqZkBK8gyl-MOiX_S0qSvD5pROvaU6ZADpYuK68zrDDm2uAe_yRRa8zZqiR6-u7yI_cq9z_7eAQG0YHT49Cbli1pveh8LVGuOkNUQJVt29uZbABa2y2Xt9jR9HmHzr2Oubs4MD5JHCuEMcQ85wYce9cXnjWzx2EXAR_CL0q8h_da8t4cVUOSC9HhCgOe-I6ec-BeeALehpB33ICTRXA3xFSWaq4XzokEGHVzBQ4r0pzV70j1uJm3-3--iG7iFUb_0Py9z6MKZqqp-HdbJgEzkZ7t3y0 "Serverstartupflow")

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