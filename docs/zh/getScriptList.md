# 脚本列表

> 根据脚本集合中获取的到的脚本集合来获取脚本列表

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "script",
  "action": "script",
  "op": "Script.listScriptFile",
  "data": {
    "pageSize": 20,
    "projectid": 6,
    "scriptNos": [
      542858,
      543308,
      549708
    ],
    "scriptType": 3,
    "startPageNo": 1
  }
}
```

|字段|说明|必填|类型|
|---|---|---|---|
|`mkey`|` `|`Y`|`String`|
|`action`|` `|`Y`|`String`|
|`op`|`唯一标识`|`Y`|`String`|
|`data`|`参数对象`|`Y`|`String`|
|`pageSize`|`每页显示条数`|`Y`|`Number`|
|`projectid`|`项目ID`|`Y`|`Number`|
|`scriptNos`|`脚本ID集合`|`Y`|`Array`|
|`scriptType`|`web端`|`Y`|`Number`|
|`startPageNo`|`页码`|`Y`|`Number`|

* 返回参数

```json
{
  "data": {
    "totalRow": 48,
    "totalPage": 3,
    "pageSize": 20,
    "page": 1,
    "list": [
      {
        "scriptNo": 549681,
        "scriptmain": "{browsers:[{action:0,browsers:[],createtime:1.569554152776E12,ip:10.10.210.33,licences:1,location:浏览器Mac1号,osName:MacOS,osVersion:10.13.6,source:c9ea7bae671d4e99a01455654ac6eb08,state:0,status:0,type:Chrome,ucomid:t.pro.browser.02@testin.cn,updatetime:1.570607519401E12,version:76.0.3809.100}]}",
        "scriptCreateDesc": "测试脚本",
        "fileinfo": {
          "uploadUserName": "甘海"
        },
        "scriptUpdateTime": 1570607548091
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
|`page`|`当前页`|`Number`|` `|
|`list`|`所需数据`|`Array`|` `|
|`scriptNo`|`脚本ID`|`Number`|` `|
|`scriptmain`|`浏览器信息`|`String`|`浏览器版本型号和系统`|
|`scriptCreateDesc`|`脚本描述`|`String`|` `|
|`fileinfo`|`操作脚本用户信息`|`Object`|`uploadUserName：更新人`|
|`scriptUpdateTime`|`更新时间`|`timestemp`|` `|

