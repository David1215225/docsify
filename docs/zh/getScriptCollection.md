# 脚本集合

> 获取每个步骤中脚本的集合

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "apikey": "xxxxxxxxxxxxxx",
  "timestamp": 1570691370136,
  "sid": "xxxxxxxxxxxxxx",
  "mkey": "script",
  "action": "script",
  "op": "Collections.scriptList",
  "data": {
    "deep": "1",
    "projectid": 6,
    "scriptDirId": "29"
  },
  "sig": "xxxxxxxxxxxxxx"
}
```

|字段|说明|必填|类型|
|---|---|---|---|
|`apikey`|`密钥`|`Y`|`String`|
|`timestamp`|`请求时间`|`Y`|`Date`|
|`sid`|`项目组`|`Y`|`String`|
|`mkey`|` `|`Y`|`String`|
|`action`|` `|`Y`|`String`|
|`op`|`唯一标识`|`Y`|`String`|
|`data`|`参数对象`|`Y`|`String`|
|`deep`|` `|`Y`|`String`|
|`projectid`|`项目ID`|`Y`|`Number`|
|`scriptDirId`|`脚本ID`|`Y`|`String`|
|`sig`|`用户信息`|`Y`|`String`|

* 返回参数

```json
{
  "msg": "成功",
  "op": "Collections.scriptList",
  "mkey": "script",
  "code": 0,
  "data": {
    "list": [
      542858,
      543308,
      549708
    ]
  },
  "apikey": "xxxxxxxxxxxxxx",
  "action": "script"
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`msg`|`状态码对应信息`|`String`|`成功或失败信息`|
|`op`|`唯一标识`|`String`|` `|
|`mkey`|` `|`String`|` `|
|`code`|`状态码`|`Number`|`0表示成功`|
|`data`|`参数对象`|`String`|`返回的数据`|
|`apikey`|`密钥`|`String`|` `|
|`action`|` `|`String`|` `|

