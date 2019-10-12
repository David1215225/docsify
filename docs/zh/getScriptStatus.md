# 脚本状态

> 根据脚本集合获取每个脚本的状态

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "script",
  "action": "script",
  "op": "Script.checkInfos",
  "data": {
    "scriptIds": [
      19468,
      19467,
      19452
    ]
  }
}
```

|字段|说明|必填|类型|
|---|---|---|---|
|`mkey`|` `|`Y`|`String`|
|`action`|` `|`Y`|`String`|
|`op`|`唯一标识`|`Y`|`String`|
|`data`|`参数对象`|`Y`|`String`|
|`scriptIds`|`脚本ID`|`Y`|`Array`|

* 返回参数

```json
{
  "data": {
    "list": [
      {
        "checkStatus": 0,
        "scriptNo": 543525
      }
    ]
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`String`|`返回的数据`|
|`list`|`数据`|`Array`|` `|
|`checkStatus`|`脚本状态`|`Number`|`0失效1有效2不存在`|
|`scriptNo`|`脚本ID`|`Number`|` `|


