<!-- TITLE: App模型 -->
<!-- SUBTITLE: App模型 -->

# 字段
| 字段名           | 类型   | 解释                                               | 默认             | 验证       |
|------------------|--------|----------------------------------------------------|------------------|------------|
| name             | String | 应用名称，一般为英文                               | uuid+noname_app  | 必要, 唯一 |
| name_zh          | String | 应用中文名称                                       | 未命名应用       | 必要       |
| secrect          | String | 应用密钥，用于和api验证                            | 自动生成         | 必要       |
| masterSecrect    | String | 应用主密钥，用于应用管理                           | 自动生成         | 必要       |
| type             | String | 应用类型                                           | "shop"           | 必要       |
| host             | String | 应用认证的主机名，默认为开发环境主机名             | "localhost:3000" | 必要       |
| adminHost        | String | 应用后台管理程序认证的主机名，默认为开发环境主机名 | 'localhost:3002' | 必要       |
| smsServiceSecret | String | 短信验证平台密钥                                   | ""               | 必要       |
| smsServiceUrl    | String | 短信验证平台发送地址                               | ""               | 必要       |