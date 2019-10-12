# 用户数据

## 快速导航

- [```[用户信息]``` 用户信息](#用户信息)

## 用户信息

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "usermanager",
  "action": "user",
  "op": "User.getUser",
  "data": {
    "sid": "te2c883bbc0368962946a16db470d19f"
  }
}
```

|字段|说明|必填|类型|
|---|---|---|---|
|`mkey`|` `|`Y`|`String`|
|`action`|` `|`Y`|`String`|
|`op`|`唯一标识`|`Y`|`String`|
|`data`|`参数对象`|`Y`|`String`|
|`sid`|`项目组`|`Y`|`String`|

* 返回参数

```json
{
  "data": {
    "objInfo": {
      "createTime": 1502260814117,
      "name": "甘海",
      "job": "后台管理员",
      "userid": 2198,
      "email": "ganhai@testin.cn",
      "status": 1
    }
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`String`|`返回的数据`|
|`objInfo`|`基本信息`|`Object`|` `|
|`name`|`用户名称`|`String`|` `|
|`email`|`用户邮箱`|`String`|` `|
