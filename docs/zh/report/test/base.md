# 测试概况

## 快速导航

- [```[测试概况]``` 任务信息](#任务信息)
- [```[测试概况]``` 图表信息](#图表信息)
- [```[测试概况]``` 报告总结](#报告总结)

## 任务信息

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "realweb",
  "action": "task",
  "op": "Task.detail",
  "data": {
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

* 返回参数

```json
{
  "data": {
    "objInfo": {
      "execStatus": 3,
      "testType": 1,
      "startExecTime": 1570784409080,
      "paramSourceName": "测试123",
      "scripts": [],
      "expiretime": 172800000,
      "finishTime": 1570786972693,
      "createtime": 1570784393991,
      "userName": "甘海",
      "summarize": "1234567890",
      "browsers": [],
      "taskDescr": "我的",
      "testResult": 2,
      "execStandard": "normal",
      "updatetime": 1570786989193,
      "status": 1
    }
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`String`|`返回的数据`|
|`objInfo`|`基本信息`|`Object`|` `|
|`execStatus`|`任务状态`|`Number`|`0待执行1执行中3已完成5已取消6已超时`|
|`userName`|`提测人`|`String`|` `|
|`createtime`|`创建时间`|`timestamp`|` `|
|`finishTime`|`完成时间`|`timestamp`|` `|
|`browsers`|`浏览器信息`|`Array`|` `|
|`scripts`|`脚本信息`|`Array`|` `|
|`paramSourceName`|`数据源信息`|`String`|` `|
|`summarize`|`报告总结`|`String`|` `|

## 图表信息

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "realweb",
  "action": "report",
  "op": "Report.taskSummary",
  "data": {
    "keywords": [
      "performanceSummary",
      "categorySummary"
    ],
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
|`keywords`|` `|`Y`|`Array`|
|`projectid`|`项目ID`|`Y`|`Number`|
|`taskid`|`任务ID`|`Y`|`String`|

* 返回参数

```json
{
  "data": {
    "objInfo": {
      "browserSystemSummary": [
        {
          "val": 6,
          "name": "MacOS"
        },
        {
          "val": 12,
          "name": "Windows"
        }
      ],
      "scriptCategorySummary": [
        {
          "val": 6,
          "resultCategory": 1
        },
        {
          "val": 12,
          "resultCategory": 13
        }
      ],
      "browserProblemSummary": [
        {
          "val": 3,
          "type": "Safari",
          "version": "12.1.2(14607.3.9)"
        },
        {
          "val": 6,
          "children": [
            {
              "val": 3,
              "type": "Chrome",
              "version": "76.0.3809.132"
            }
          ],
          "type": "Chrome"
        }
      ],
      "projectid": 6,
      "taskid": "wt2f503b369098962ffd416dba0bbb07"
    }
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`String`|`返回的数据`|
|`objInfo`|`基本信息`|`Object`|` `|
|`browserSystemSummary`|`系统问题统计`|`Array`|``|
|`scriptCategorySummary`|`脚本问题统计`|`Array`|` `|
|`browserProblemSummary`|`浏览器问题统计`|`Array`|` `|
|`projectid`|`项目ID`|`Number`|` `|
|`taskid`|`任务ID`|`String`|` `|

## 报告总结

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "realweb",
  "action": "task",
  "op": "Task.modify",
  "data": {
    "projectid": 6,
    "summarize": "1234567890发发发",
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
|`summarize`|`总结信息`|`N`|`String`|

* 返回参数

```json
{
  "data": {
    "result": 1
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`String`|`返回的数据`|
|`result`|`保存状态`|`Number`|`1成功`|
