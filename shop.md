<!-- TITLE: Shop模型 -->
<!-- SUBTITLE: 表示系统的店铺实体 -->

# 文件位置
[项目目录]/models/Shop.js

# 字段表
| 字段名           | 类型   | 解释                                               | 默认             | 验证       |
|------------------|--------|----------------------------------------------------|------------------|------------|
| name    | String | 店铺名称                               | uuid+_nonameshop               | 必要且唯一       |
| name_zh    | String | 店铺中文名称                | ”未命名店铺“               | 必要     |
| description    | String | 店铺描述                | ”店铺尚未简介“               | 类型验证    |
| isDefault    | Boolean | 是否是系统默认                | false               | 类型验证     |
| cardLevelCurrent    | Number | 店铺目前发的卡的最高等级                | 0               | 类型验证，不能为负数     |
