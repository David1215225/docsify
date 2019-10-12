# 脚本树结构

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "script",
  "action": "script",
  "op": "Collections.list",
  "data": {
    "lazyTree": 0,
    "projectid": 6
  }
}
```

|字段|说明|必填|类型|
|---|---|---|---|
|`mkey`|` `|`Y`|`String`|
|`action`|` `|`Y`|`String`|
|`op`|`唯一标识`|`Y`|`String`|
|`data`|`参数对象`|`Y`|`String`|
|`lazyTree`|` `|`Y`|`Number`|
|`projectid`|`项目ID`|`Y`|`Number`|

* 返回参数

```json
{
  "data": {
    "list": [
      {
        "children": [
          {
            "children": [
              {
                "name": "afa",
                "scriptDirId": 35,
                "parentDirId": 34
              }
            ],
            "name": "ss",
            "scriptDirId": 34,
            "parentDirId": 29
          }
        ],
        "name": "质保团队APP组",
        "scriptDirId": 29
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
|`name`|`脚本名称`|`String`|` `|
|`scriptDirId`|`脚本ID`|`Number`|` `|
|`children`|`脚本子元素`|`Array`|` `|
|`parentDirId`|`脚本父级ID`|`Number`|` `|

