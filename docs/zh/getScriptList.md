# 脚本列表

> 根据脚本集合中获取的到的脚本集合来获取脚本列表

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "apikey": "xxxxxxxxxxxxxx",
  "timestamp": 1570691370162,
  "sid": "xxxxxxxxxxxxxx",
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
|`pageSize`|`每页显示条数`|`Y`|`Number`|
|`projectid`|`项目ID`|`Y`|`Number`|
|`scriptNos`|`脚本ID集合`|`Y`|`Array`|
|`scriptType`|`web端`|`Y`|`Number`|
|`startPageNo`|`页码`|`Y`|`Number`|
|`sig`|`用户信息`|`Y`|`String`|

* 返回参数

```json
{
  "msg": "成功",
  "op": "Script.listScriptFile",
  "mkey": "script",
  "code": 0,
  "data": {
    "totalRow": 48,
    "totalPage": 3,
    "pageSize": 20,
    "page": 1,
    "list": [
      {
        "scriptUpdateType": 0,
        "scriptUpdateDesc": "",
        "taginfos": "",
        "scriptUpdateTime": 1570607548091,
        "ostype": 0,
        "scriptFromType": 1,
        "type": 3,
        "scriptUpdateUserid": 2198,
        "scriptid": 19468,
        "declareVars": "{browsers:[{action:0,browsers:[],createtime:1.569554152776E12,ip:10.10.210.33,licences:1,location:浏览器Mac1号,osName:MacOS,osVersion:10.13.6,source:c9ea7bae671d4e99a01455654ac6eb08,state:0,status:0,type:Chrome,ucomid:t.pro.browser.02@testin.cn,updatetime:1.570607519401E12,version:76.0.3809.100}]}",
        "build": 3,
        "imageurl": "",
        "scriptNo": 549681,
        "scriptCreateUser": 2198,
        "fileinfo": {
          "createUserId": 2198,
          "expireTime": 0,
          "size": 1026,
          "createTime": 1570607548073,
          "uploadUserName": "甘海",
          "fileUrl": "https://testin-ee.oss-cn-hangzhou.aliyuncs.com/ZIP--1-0c3701e21a784f9e82a34bfd2e5a30b6.zip",
          "isdelete": 0,
          "filemd5": "45d30d12723cbb1af3c31b978cc6fb42",
          "type": 0,
          "fileId": 24415320
        },
        "scriptName": "549681test.zip",
        "scriptmain": "{browsers:[{action:0,browsers:[],createtime:1.569554152776E12,ip:10.10.210.33,licences:1,location:浏览器Mac1号,osName:MacOS,osVersion:10.13.6,source:c9ea7bae671d4e99a01455654ac6eb08,state:0,status:0,type:Chrome,ucomid:t.pro.browser.02@testin.cn,updatetime:1.570607519401E12,version:76.0.3809.100}]}",
        "scriptCreateDesc": "测试脚本",
        "adapterversionname": "",
        "projectId": 6,
        "scriptCreateTime": 1570607548091,
        "adapterversioncode": "",
        "channelId": ""
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
|`totalRow`|`总条数`|`Number`|` `|
|`totalPage`|`总页数`|`Number`|` `|
|`pageSize`|`每页条数`|`Number`|` `|
|`page`|`当前页`|`Number`|` `|
|`list`|`所需数据`|`Number`|` `|
|`apikey`|`密钥`|`String`|` `|
|`action`|` `|`String`|` `|

