<!-- TITLE: Role模型 -->
<!-- SUBTITLE: 用户角色模型 -->

# 文件位置
[项目目录]/models/Role.js

# 字段表

| 字段名           | 类型   | 解释                                               | 默认             | 验证       |
|------------------|--------|----------------------------------------------------|------------------|------------|
| name    | String | 角色名，一般是英文                               | uuid+"_nonamerole"               | 必要且在同一个app内唯一       |
| name_zh    | String | 角色中文名               | "未命名角色“               |  不必要       |
| isSuper    | Boolean | 是否是超级管理员                    | false             | 必要       |
| isDefault   | Boolean | 是否是系统默认的角色                    | false             | 必要       |
| isSystemAdmin   | Boolean | 是否是系统后台管理员的角色。由于系统的在用户交互的过程中会产生大量的角色，我们可以这个字段来区分管理                    | false             | 必要       |


# 方法

## createRole(params, appId)
设置系统的属性值
## 参数表
| 参数名 | 类型     | 解释                                         | 默认   | 验证                                        |
|--------|----------|----------------------------------------------|--------|---------------------------------------------|
| params | Object   | 包含Role字段内容的对象                        | {}     | 不得等价为false, 并且params.name在同一个app唯一            |
| appId  | ObjectId | 说明这个role属于那个app               | null   | 不得等价为false                                 |


## 返回值
|返回值|类型|解释|
|---------|------|------|
|'name required'|String|参数params的name等价为false|
|'appId required'|String|参数appId等价为false|
|'role name or name_zh exists'|String|字段name或者name_zh在同一个App内已经存在|
|object|Object|创建成功，返回一个类型为Role的对象|


# 关联的其他模型

* [/approle类型](AppRole)
* [/roleuser类型](RoleUser)
