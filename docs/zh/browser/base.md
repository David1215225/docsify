# 浏览器相关

## 快速导航

- [```[浏览器部分]``` 浏览器列表](#浏览器列表)
- [```[浏览器部分]``` 浏览器筛选条件](#浏览器筛选条件)


## 浏览器列表

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "controlcenter",
  "action": "pc",
  "op": "Pc.disList",
  "data": {
    "bizCode": 4100,
    "eid": "1",
    "page": 1,
    "pageSize": 20,
    "privateSource": 1,
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
|`bizCode`|` `|`Y`|`Number`|
|`page`|`当前页码`|`Y`|`Number`|
|`pageSize`|`每页条数`|`Y`|`Number`|
|`projectid`|`项目ID`|`Y`|`Number`|

* 返回参数

```json
{
  "data": {
    "totalRow": 6,
    "totalPage": 1,
    "pageSize": 20,
    "page": 1,
    "list": [
      {
        "source": "c9ea7bae671d4e99a01455654ac6eb08",
        "type": "Chrome",
        "osName": "Windows",
        "version": "76.0.3809.132"
      }
    ]
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`String`|`返回的数据`|
|`totalRow`|`总条数`|`Number`|` `|
|`totalPage`|`总页数`|`Number`|` `|
|`pageSize`|`每页条数`|`Number`|` `|
|`page`|`当前页码`|`Number`|` `|
|`type`|`浏览器名称`|`String`|`目前分五大浏览器`|
|`osName`|`系统`|`String`|`mac和window`|
|`version`|`浏览器版本`|`String`|` `|

## 浏览器筛选条件

> 该接口获取当前浏览器筛选所需条件（浏览器名称和系统）

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "controlcenter",
  "action": "pc",
  "op": "Pc.types",
  "data": {
    "bizCode": 4100,
    "eid": "1",
    "privateSource": 1,
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
|`bizCode`|` `|`Y`|`Number`|
|`eid`|` `|`Y`|`String`|
|`projectid`|`项目ID`|`Y`|`Number`|

* 返回参数

```json
{
  "data": {
    "result": {
      "types": [
        "Chrome",
        "Edge",
        "Firefox",
        "IE",
        "Safari"
      ],
      "osTypes": [
        "Windows",
        "MacOS"
      ]
    }
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`Object`|`返回的数据`|
|`result`|`数据`|`Object`|` `|
|`types`|`浏览器名称`|`Array`|` `|
|`osTypes`|`系统名称`|`Array`|` `|




