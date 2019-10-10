# 脚本状态

> 根据脚本集合获取每个脚本的状态

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "apikey": "xxxxxxxxxxxxxx",
  "timestamp": 1570691370240,
  "sid": "xxxxxxxxxxxxxx",
  "mkey": "script",
  "action": "script",
  "op": "Script.checkInfos",
  "data": {
    "scriptIds": [
      19468,
      19467,
      19452
    ]
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
|`scriptIds`|`脚本ID`|`Y`|`Array`|
|`sig`|`用户信息`|`Y`|`String`|

* 返回参数

```json
{
  "msg": "成功",
  "op": "Script.checkInfos",
  "mkey": "script",
  "code": 0,
  "data": {
    "list": [
      {
        "scriptId": 13061,
        "checkStatus": 0,
        "checkTime": 1512705015939,
        "checkContent": "{depends:[],self:[{scriptUrl:{result:scriptNotVisit,code:0}},{scriptStepUrl:{result:OK,code:1}}]}",
        "scriptNo": 543525,
        "scriptCreateDesc": "SharedMethods_CloseHomePagePopupDialog",
        "id": 692427
      }
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

