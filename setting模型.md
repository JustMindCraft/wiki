<!-- TITLE: Setting模型 -->
<!-- SUBTITLE: 系统设置模型 -->

# 文件位置
[项目目录]/models/Settting.js

# 字段表

| 字段名           | 类型   | 解释                                               | 默认             | 验证       |
|------------------|--------|----------------------------------------------------|------------------|------------|
| name    | String | 系统设置的属性名                               | 自动生成               | 必要且唯一       |
| valText    | String | 系统设置的字符类型属性值               | "unset“               |  不必要       |
| valJudge    | Boolean | 系统设置布尔类型属性值                    | false             | 不必要       |


# 方法

## setSettingValue(name, value)
设置系统的属性值
## getSettingValue(name)
获取系统的属性


# 关联的其他模型
