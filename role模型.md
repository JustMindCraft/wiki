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

## setSettingValue(name, value)
设置系统的属性值
## getSettingValue(name)
获取系统的属性


# 关联的其他模型
