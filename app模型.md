<!-- TITLE: App模型 -->
<!-- SUBTITLE: 用于处理系统的应用管理 -->
# 模型定义的文件位置
[项目目录]/models/App.js

# 字段表
| 字段名           | 类型   | 解释                                               | 默认             | 验证       |
|------------------|--------|----------------------------------------------------|------------------|------------|
| name             | String | 应用名称，一般为英文                               | uuid+noname_app  | 必要, 唯一 |
| name_zh          | String | 应用中文名称                                       | 未命名应用       | 必要       |
| secrect          | String | 应用密钥，用于和api验证                            | 自动生成         | 必要       |
| masterSecrect    | String | 应用主密钥，用于应用管理                           | 自动生成         | 必要       |
| type             | String | 应用类型                                           | "shop"           | 必要       |
| host             | String | 应用认证的主机名，默认为开发环境主机名             | "localhost:3000" | 必要       |
| adminHost        | String | 应用后台管理程序认证的主机名，默认为开发环境主机名 | 'localhost:3002' | 必要       |
| smsServiceSecret | String | 短信验证平台密钥                                   | "unset"               | 必要       |
| smsServiceUrl    | String | 短信验证平台发送地址                               | "unset"               | 必要       |


# 方法

## create(params,  owner, type)
创建一个新的APP
### 参数表
| 参数名 | 类型     | 解释                                         | 默认   | 验证                                        |
|--------|----------|----------------------------------------------|--------|---------------------------------------------|
| params | Object   | 包含App字段内容的对象                        | {}     | 不得为false, 并且params.name唯一            |
| onwer  | ObjectId | User模型的Id， 说明App的拥有者               | null   | 不得为false                                 |
| type   | String   | 说明App类型，目前可选的有："shop", 'storage' | 'shop' | 不得为false,或者空字符串,或者不在可选范围内 |