# 脚本集合

> 获取每个步骤中脚本的集合

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "script",
  "action": "script",
  "op": "Collections.scriptList",
  "data": {
    "deep": "1",
    "projectid": 6,
    "scriptDirId": "29"
  }
}
```

|字段|说明|必填|类型|
|---|---|---|---|
|`mkey`|` `|`Y`|`String`|
|`action`|` `|`Y`|`String`|
|`op`|`唯一标识`|`Y`|`String`|
|`data`|`参数对象`|`Y`|`String`|
|`deep`|` `|`Y`|`String`|
|`projectid`|`项目ID`|`Y`|`Number`|
|`scriptDirId`|`脚本ID`|`Y`|`String`|
* 返回参数

```json
{
  "data": {
    "list": [
      542858,
      543308,
      549708
    ]
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`op`|`唯一标识`|`String`|` `|
|`data`|`参数对象`|`Object`|`返回的数据`|
|`list`|`数据`|`Array`|` `|
