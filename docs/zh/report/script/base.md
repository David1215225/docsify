# 脚本执行报告

## 快速导航

- [```[脚本执行报告]``` 筛选条件](#筛选条件)
- [```[脚本执行报告]``` 脚本列表](#脚本列表)

## 筛选条件

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "realweb",
  "action": "task",
  "op": "Task.runInfoConditions",
  "data": {
    "projectid": 6,
    "taskid": "wt2f503b369098962ffd416dba0bbb07",
    "type": "script"
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
|`taskid`|`任务ID`|`Y`|`String`|
|`type`|`类别`|`Y`|`String`|

* 返回参数

```json
{
  "data": {
    "objInfo": {
      "resultCategorys": [1, 13]
    }
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`String`|`返回的数据`|
|`objInfo`|`基本信息`|`Object`|` `|
|`resultCategorys`|`问题类型及状态`|`Array`|`-2待执行-1执行中0无结果1通过7未执行8超时9取消13脚本错误15环境异常17Http错误100失效`|

## 脚本列表

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "realweb",
  "action": "task",
  "op": "Task.scriptRunInfos",
  "data": {
    "page": 1,
    "pageSize": 20,
    "projectid": 6,
    "taskid": "wt2f503b369098962ffd416dba0bbb07"
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
|`taskid`|`任务ID`|`Y`|`String`|
|`page`|`当前页码`|`Y`|`Number`|
|`pageSize`|`每页条数`|`Y`|`Number`|

* 返回参数

```json
{
  "data": {
    "objInfo": {
      "total": 18,
      "passTotal": 1,
      "scriptRunInfos": {
        "totalRow": 18,
        "curPage": 1,
        "totalPage": 1,
        "pageSize": 20,
        "list": [
          {
            "finishTime": 1570784443102,
            "createtime": 1570784407792,
            "execStatus": 3,
            "errorCode": 42001,
            "subtaskid": "26e49fe39edf468cb9a5349e8eb41769",
            "startExecTime": 1570784409080,
            "webScript": {
              "scriptUrl": "https://testin-ee.oss-cn-hangzhou.aliyuncs.com/ZIP--1-0c3701e21a784f9e82a34bfd2e5a30b6.zip",
              "scriptid": 19468,
              "scriptTags": "",
              "scriptMd5": "45d30d12723cbb1af3c31b978cc6fb42",
              "scriptDescr": "测试脚本",
              "scriptType": 3,
              "scriptNo": 549681,
              "osType": 0,
              "orderNum": 1,
              "scriptName": "549681test.zip"
            },
            "errorMsg": "没有识别到数据",
            "resultCategory": 13,
            "subsubtaskid": "956575acc0034c8396fd8f59c2f073c2",
            "networkType": "wifi",
            "updatetime": 1570784449737,
            "projectid": 6,
            "taskid": "wt2f503b369098962ffd416dba0bbb07",
            "browserInfo": {
              "source": "c9ea7bae671d4e99a01455654ac6eb08",
              "osName": "Windows",
              "type": "Edge",
              "version": "44.17763.1.0"
            },
            "status": 1
          }
        ]
      },
      "failedTotal": 1
    }
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`String`|`返回的数据`|
|`objInfo`|`基本信息`|`Object`|` `|
|`total`|`总条数`|`Number`|` `|
|`passTotal`|`脚本通过数`|`Number`|` `|
|`failedTotal`|`未通过脚本数`|`Number`|` `|
|`scriptRunInfos`|`脚本列表统计`|`Object`|` `|
|`totalRow`|`总条数`|`Number`|` `|
|`curPage`|`当前页码`|`Number`|` `|
|`totalPage`|`总页数`|`Number`|` `|
|`pageSize`|`每页条数`|`Number`|` `|
|`list`|`脚本列表`|`Array`|` `|
|`webScript.scriptNo`|`脚本ID`|`Number`|` `|
|`webScript.scriptDescr`|`脚本描述`|`String`|` `|
|`browserInfo.type`|`浏览器名称`|`String`|` `|
|`browserInfo.version`|`浏览器版本`|`String`|` `|
|`resultCategory`|`状态`|`Number`|`-2待执行-1执行中0无结果1通过9取消8超时100失效`|
|`resultCategory`|`问题类型`|`Number`|`0无结果7未执行8超时9取消13脚本错误15环境异常17HTTP错误100失效`|
|`errorMsg`|`错误定位`|`String`|` `|
