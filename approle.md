<!-- TITLE: AppRole模型 -->
<!-- SUBTITLE: 用以表示应用内角色的关系 -->
# 模型定义的文件位置
[项目目录]/models/App.js

# 字段表
| 字段名           | 类型   | 解释                                               | 默认             | 验证       |
|------------------|--------|----------------------------------------------------|------------------|------------|
| app    | ObjectId | App类型objectId                               | null               | 必要,不可等价为false       |
| role    | ObjectId | Role类型objectId                               | null               | 必要,不可等价为false       |
| isDefault    | Boolean | 是否为系统默认                               | false               | 必要       |


# 方法

## assginRoleToApp(roleId, appId, optional)
将一个角色绑定给一个App所有
### 参数表
| 参数名 | 类型     | 解释                                         | 默认   | 验证                                        |
|--------|----------|----------------------------------------------|--------|---------------------------------------------|
| roleId | ObjectId   | Role模型的ObjectId                        | null    | 不得等价为false          |
| appId  | ObjectId | App模型的Id， 说明Role的归属的App               | null   | 不得等价为false                                 |
| optional   | Object   | 可选的其他参数| {} | 类型检查 |
| optional.isDefault   | Boolean   | 是否为系统默认关系| false | 类型检查 |


### 返回值
| 返回值             | 类型   | 解释                               |
|--------------------|--------|------------------------------------|
| object       | Object | 若是绑定成功，则返回一个AppRole对象 |
| "ALREADY EXISTS"    | String | 这个应用的role已经存在重名           |


## getOneRoleForApp(appId, match)
获取系统默认应用
### 参数表
| 参数名 | 类型     | 解释                                         | 默认   | 验证                                        |
| roleId | ObjectId   | Role模型的ObjectId                        | null    | 不得等价为false          |
| match   | Object   | mongo风格查询对象， 用以查找roles表 | {} | 类型检查
### 返回值
| 返回值             | 类型   | 解释                               |
|--------------------|--------|------------------------------------|
| object        | Object | 若是存在默认应用，则返回一个Role对象 |
| null | Null | 没有找到符合要求的Role对象 |           |


# 关联的其他模型

* [App](/app模型)
* [Role](/role模型)


