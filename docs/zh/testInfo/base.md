# 基础信息相关

## 快速导航

- [```[基础信息部分]``` 数据源信息](#数据源信息)
- [```[基础信息部分]``` 用户邮箱列表](#用户邮箱列表)
- [```[基础信息部分]``` 创建任务信息](#创建任务信息)


## 数据源信息

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "script",
  "action": "script",
  "op": "DataSource.list",
  "data": {
    "projectId": 6,
    "type": 1
  }
}
```

|字段|说明|必填|类型|
|---|---|---|---|
|`mkey`|` `|`Y`|`String`|
|`action`|` `|`Y`|`String`|
|`op`|`唯一标识`|`Y`|`String`|
|`data`|`参数对象`|`Y`|`String`|
|`projectid`|`项目ID`|`Y`|`Number`|
|`type`|` `|`Y`|`Number`|

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

## 用户邮箱列表

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "usermanager",
  "action": "user",
  "op": "User.getProjectUserList",
  "data": {
    "eid": "1",
    "page": 1,
    "pageSize": 1000,
    "projectid": 6,
    "status": 1
  }
}
```

|字段|说明|必填|类型|
|---|---|---|---|
|`mkey`|` `|`Y`|`String`|
|`action`|` `|`Y`|`String`|
|`op`|`唯一标识`|`Y`|`String`|
|`data`|`参数对象`|`Y`|`String`|
|`projectid`|`项目ID`|`Y`|`Number`|
|`eid`|` `|`Y`|`String`|
|`page`|`当前页码`|`Y`|`Number`|
|`pageSize`|`每页条数`|`Y`|`Number`|
|`status`|` `|`Y`|`Number`|

* 返回参数

```json
{
  "data": {
    "totalRow": 80,
    "totalPage": 1,
    "pageSize": 1000,
    "page": 1,
    "list": [
      {
        "name": "甘海",
        "email": "ganhai@testin.cn"
      }
    ]
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`Object`|`返回的数据`|
|`totalRow`|`总条数`|`Number`|` `|
|`totalPage`|`总页数`|`Number`|` `|
|`pageSize`|`每页条数`|`Number`|` `|
|`page`|`当前页码`|`Number`|` `|
|`name`|`用户姓名`|`String`|` `|
|`email`|`邮箱`|`String`|` `|

## 创建任务信息

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "realweb",
  "action": "task",
  "op": "Task.create",
  "data": {
    "bizCode": 4100,
    "browsers": [
      {
        "deviceSign": "Windows_Firefox_69.0",
        "osName": "Windows",
        "source": "c9ea7bae671d4e99a01455654ac6eb08",
        "type": "Firefox",
        "version": "69.0"
      }
    ],
    "projectid": 6,
    "paramSource": 55,
    "paramSourceName": "数据源name",
    "scripts": [
      {
        "scriptNo": 549681,
        "scriptid": 19468
      }
    ],
    "taskDescr": "11111"
  }
}
```

|字段|说明|必填|类型|
|---|---|---|---|
|`mkey`|` `|`Y`|`String`|
|`action`|` `|`Y`|`String`|
|`op`|`唯一标识`|`Y`|`String`|
|`data`|`参数对象`|`Y`|`String`|
|`projectid`|`项目ID`|`Y`|`Number`|
|`browsers`|`浏览器信息`|`Y`|`Array`|
|`paramSource`|`数据源ID`|`N`|`Number`|
|`paramSourceName`|`数据源名称`|`N`|`String`|
|`scripts`|`所选脚本信息`|`Y`|`Array`|
|`taskDescr`|`任务名称`|`Y`|`String`|

* 返回参数

```json
{
  "data": {
    "result": "wt659f3b7b11889668b0616dbeb862e5"
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`Object`|`返回的数据`|
|`result`|`任务ID`|`String`|` `|
