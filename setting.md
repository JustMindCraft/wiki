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
### 参数表
| 参数           | 类型   | 解释                                               | 默认             | 验证       |
|------------------|--------|----------------------------------------------------|------------------|------------|
| name    | String | 系统设置的属性名                               | "unknown"               | 不能等值为false     |
| value    | String|Boolean | 系统设置的字符类型属性值               | "unset“               |  不能等值为false       |

### 返回值

| 返回值           | 类型   | 解释                                               | 
|------------------|--------|----------------------------------------------------|
|       object    | Object   | Setting类型的对象                                               | 
|       "Already Exist"     | String   | 系统设置名已经存在                                               | 
|      "UNSUPPORT TYPE "   | String   | 不支持的系统设置类型           | 
## getSettingValue(name)
获取系统的属性

### 参数表
无。
### 返回值

| 返回值           | 类型   | 解释                                               | 
|------------------|--------|----------------------------------------------------|
|       null    | Null   | 若是没有找到这个系统设置属性，那么返回null                                               | 
|       boolean     | Boolean   | 返回一个布尔类型的系统设置                                               | 
|      string   | String   | 返回一个字符串类型的系统设置           |


# 关联的其他模型

无。
