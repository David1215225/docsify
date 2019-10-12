# 接口必须参数

> 接口协议中必填参数

* 请求参数

```json
{
  "apikey": "xxxxxxxxxxxxxx",
  "timestamp": 1570691370136,
  "sid": "xxxxxxxxxxxxxx",
  "mkey": "见单独每个接口",
  "action": "见单独每个接口",
  "op": "见单独每个接口",
  "data": "Object 见每个单独接口",
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
|`data`|`参数对象`|`Y`|`Object`|
|`sig`|`用户信息`|`Y`|`String`|

* 返回参数

```json
{
  "msg": "成功",
  "op": "见单独每个接口",
  "mkey": "见单独每个接口",
  "code": 0,
  "data": {
    "list": "返回的所需数据"
  },
  "apikey": "xxxxxxxxxxxxxx",
  "action": "见单独每个接口"
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`msg`|`状态码对应信息`|`String`|`成功或失败信息`|
|`op`|`唯一标识`|`String`|` `|
|`mkey`|` `|`String`|` `|
|`code`|`状态码`|`Number`|`0表示成功`|
|`data`|`参数对象`|`String`|`Object`|
|`apikey`|`密钥`|`String`|` `|
|`action`|` `|`String`|` `|

