# 执行详情

## 快速导航

- [```[执行详情]``` 脚本步骤信息](#脚本步骤信息)
- [```[执行详情]``` 浏览器信息](#浏览器信息)
- [```[执行详情]``` 脚本执行概况](#脚本执行概况)
- [```[执行详情]``` 单独脚本步骤详情](#单独脚本步骤详情)
- [```[执行详情]``` 网络信息筛选条件](#网络信息筛选条件)
- [```[执行详情]``` 网络步骤信息](#网络步骤信息)

## 脚本步骤信息

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "op": "Report.scriptSteps",
  "mkey": "realweb",
  "action": "report",
  "data": {
    "projectid": 6,
    "subtaskid": "26e49fe39edf468cb9a5349e8eb41769",
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
|`taskid`|`任务ID`|`Y`|`String`|
|`subtaskid`|`子任务ID`|`Y`|`String`|
|`projectid`|`项目ID`|`Y`|`Number`|

* 返回参数

```json
{
  "msg": "成功",
  "op": "Report.scriptSteps",
  "mkey": "realweb",
  "code": 0,
  "data": {
    "objInfo": {
      "processMap": {
        "下载脚本": 1,
        "初始化图片控件": 1,
        "脚本解析": 1,
        "初始化任务": 1
      },
      "list": [
        {
          "scriptid": 19468,
          "reportDetails": [
            {
              "subsubtaskid": "956575acc0034c8396fd8f59c2f073c2"
            }
          ],
          "scriptNo": 549681,
          "orderNum": 1,
          "scriptSign": "549681_1",
          "scripts": [
            {
              "sequence": 2147483647,
              "callerStepid": 2147483647,
              "scriptTag": "549681-2147483647_2147483647",
              "testResult": 0,
              "callerScriptNo": 549681
            },
            {
              "sequence": 1,
              "scriptId": 19468,
              "fileSize": 1026,
              "scriptUpdateDesc": "",
              "scriptNo": 549681,
              "scriptmain": "{browsers:[{action:0,browsers:[],createtime:1.569554152776E12,ip:10.10.210.33,licences:1,location:浏览器Mac1号,osName:MacOS,osVersion:10.13.6,source:c9ea7bae671d4e99a01455654ac6eb08,state:0,status:0,type:Chrome,ucomid:t.pro.browser.02@testin.cn,updatetime:1.570607519401E12,version:76.0.3809.100}]}",
              "scriptName": "549681test.zip",
              "scriptCreateDesc": "测试脚本",
              "fileUrl": "https://testin-ee.oss-cn-hangzhou.aliyuncs.com/ZIP--1-0c3701e21a784f9e82a34bfd2e5a30b6.zip",
              "scriptTag": "549681",
              "fileMd5": "45d30d12723cbb1af3c31b978cc6fb42",
              "testResult": 2
            }
          ],
          "steps": [
            {
              "stepdesc": "初始化",
              "steptype": "scriptExceInit",
              "disable": 0,
              "stepname": "初始化",
              "stepid": 2147483647,
              "scriptSequence": 1,
              "stepimage": "",
              "describe": "",
              "testResult": 0
            },
            {
              "stepdesc": "10 秒",
              "steptype": "sleep",
              "checkRule": "none",
              "disable": 0,
              "stepname": "等待 : 10 秒",
              "stepid": 0,
              "scriptSequence": 1,
              "stepimage": "",
              "checkPointName": "",
              "describe": "",
              "testResult": 1
            },
            {
              "stepdesc": "点击【234】",
              "steptype": "clickAI",
              "checkRule": "none",
              "disable": 0,
              "stepname": "AI步骤 : 点击【234】",
              "stepid": 1,
              "scriptSequence": 1,
              "stepimage": "",
              "checkPointName": "",
              "describe": "",
              "testResult": 2
            },
            {
              "stepdesc": "访问[http://souhu.com/]",
              "steptype": "browser_launch",
              "checkRule": "none",
              "disable": 0,
              "stepname": " : 访问[http://souhu.com/]",
              "stepid": 2,
              "scriptSequence": 1,
              "stepimage": "",
              "checkPointName": "",
              "describe": "",
              "testResult": 0
            },
            {
              "stepdesc": "初始化被测脚本",
              "steptype": "init_initCurrentScript",
              "disable": 0,
              "stepname": "初始化被测脚本",
              "stepid": 0,
              "scriptSequence": 2147483647,
              "stepimage": "",
              "describe": "",
              "testResult": 1
            },
            {
              "stepdesc": "停止被测应用",
              "steptype": "init_forceStopStep",
              "disable": 0,
              "stepname": "停止被测应用",
              "stepid": 1,
              "scriptSequence": 2147483647,
              "stepimage": "",
              "describe": "",
              "testResult": 1
            }
          ],
          "taskid": "wt2f503b369098962ffd416dba0bbb07",
          "categorySummarys": [
            {
              "resultcategory": 13,
              "total": 6
            }
          ]
        }
      ],
      "preResult": true
    }
  },
  "apikey": "405b2e2ea35f6fe09a5004ce7b88cf7d",
  "action": "report"
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`String`|`返回的数据`|
|`objInfo`|`基本信息`|`Object`|` `|
|`processMap`|`初始化步骤`|`Object`|` `|
|`list`|`脚本执行步骤`|`Array`|` `|

## 浏览器信息

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "op": "Report.getBrowserInfo",
  "mkey": "realweb",
  "action": "report",
  "data": {
    "projectid": 6,
    "subtaskid": "26e49fe39edf468cb9a5349e8eb41769",
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
|`taskid`|`任务ID`|`Y`|`String`|
|`subtaskid`|`子任务ID`|`Y`|`String`|
|`projectid`|`项目ID`|`Y`|`Number`|

* 返回参数

```json
{
  "data": {
    "objInfo": {
      "ucomid": "t.pro.browser.01@testin.cn",
      "source": "c9ea7bae671d4e99a01455654ac6eb08",
      "osName": "Windows",
      "type": "Edge",
      "version": "44.17763.1.0"
    }
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`String`|`返回的数据`|
|`objInfo`|`基本信息`|`Object`|` `|
|`type`|`浏览器名称`|`String`|` `|
|`version`|`浏览器版本`|`String`|` `|
|`osName`|`操作系统`|`String`|` `|
|`osVersion`|`操作系统版本`|`String`|` `|

## 脚本执行概况

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "realweb",
  "action": "report",
  "op": "Report.scriptRunInfoSummary",
  "data": {
    "projectid": 6,
    "subtaskid": "26e49fe39edf468cb9a5349e8eb41769",
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
|`taskid`|`任务ID`|`Y`|`String`|
|`subtaskid`|`子任务ID`|`Y`|`String`|
|`projectid`|`项目ID`|`Y`|`Number`|

* 返回参数

```json
{
  "data": {
    "objInfo": {
      "unexecTotal": 0,
      "timeoutTotal": 0,
      "passTotal": 1,
      "failedTotal": 2,
      "timeConsume": 124771,
      "canceledTotal": 0,
      "resultCategory": 13,
      "taskDescr": "我的",
      "errorCode": 42001,
      "list": [
        {
          "resultCategory": 13,
          "errorCode": 42001,
          "subsubtaskid": "956575acc0034c8396fd8f59c2f073c2",
          "reportRunInfo": {
            "testProcesses": [
              {
                "stage": "preparation",
                "totalTime": 20,
                "name": "parseScript",
                "startTime": 1570784423671,
                "endTime": 1570784423691
              },
              {
                "stage": "preparation",
                "totalTime": 774,
                "name": "downloadScript",
                "startTime": 1570784423691,
                "endTime": 1570784424465
              },
              {
                "stage": "preparation",
                "totalTime": 15,
                "name": "initTask",
                "startTime": 1570784424496,
                "endTime": 1570784424511
              },
              {
                "stage": "preparation",
                "totalTime": 4,
                "name": "initComponentImg",
                "startTime": 1570784424511,
                "endTime": 1570784424515
              },
              {
                "stage": "init",
                "totalTime": 5,
                "name": "initCurrentScript",
                "startTime": 1570784424516,
                "endTime": 1570784424521
              },
              {
                "stage": "execute",
                "totalTime": 3263,
                "name": "startup",
                "startTime": 1570784424559,
                "endTime": 1570784427822
              },
              {
                "stage": "execute",
                "totalTime": 10737,
                "name": "execute",
                "startTime": 1570784427825,
                "endTime": 1570784438562
              },
              {
                "stage": "init",
                "totalTime": 2809,
                "name": "forceStopStep",
                "startTime": 1570784438562,
                "endTime": 1570784441371
              }
            ],
            "videoInfo": {
              "errorCode": 0
            },
            "errorCode": 42001,
            "ucomid": "t.pro.browser.01@testin.cn",
            "ucomVersion": "V3.4-20190918.2",
            "errorMsg": "没有识别到数据",
            "pfCode": 1005
          },
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
          "browserInfo": {
            "source": "c9ea7bae671d4e99a01455654ac6eb08",
            "osName": "Windows",
            "type": "Edge",
            "version": "44.17763.1.0"
          },
          "errorMsg": "没有识别到数据"
        }
      ]
    }
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`String`|`返回的数据`|
|`objInfo`|`基本信息`|`Object`|` `|
|`list`|` `|`Array`|` `|
|`webScript.scriptNo`|`脚本ID`|`Number`|` `|
|`webScript.scriptDescr`|`脚本描述`|`String`|` `|
|`resultCategory`|`状态`|`Number`|`-2待执行-1执行中0无结果1通过9取消8超时100失效`|
|`errorMsg`|`错误定位`|`String`|` `|

## 单独脚本步骤详情

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "op": "Report.stepdetail",
  "mkey": "realweb",
  "action": "report",
  "data": {
    "global": 1,
    "projectid": 6,
    "scriptTag": "549708",
    "stepid": 2,
    "subsubtaskid": "c8122debe1354c9a96df9a150497cb79",
    "subtaskid": "26e49fe39edf468cb9a5349e8eb41769",
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
|`global`|`获取包含脚本基本的信息`|`Y`|`Number`|
|`projectid`|`项目ID`|`Y`|`Number`|
|`scriptTag`|`脚本ID`|`Y`|`String`|
|`stepid`|`步骤id`|`Y`|`Number`|
|`subsubtaskid`|`子子任务ID`|`Y`|`String`|
|`subtaskid`|`子任务ID`|`Y`|`String`|
|`taskid`|`任务ID`|`Y`|`String`|

* 返回参数

```json
{
  "data": {
    "objInfo": {
      "result": {
        "stepinfo": {
          "extension": "{actionType:browser_launch,actualImage:step_1_1570784445101.jpg,consumedTime:25348毫秒,csvDataFilePath:,disable:false,resultStatus:0,stepDes: 访问[http://www.sohu.com/],stepIndex:1,stepInfo: 访问[http://www.sohu.com/]}",
          "imageKey": "step_1_1570784445101.jpg",
          "stepId": 0,
          "errorCode": 0,
          "skip": 0,
          "performanceNavigation": "https://testin-ee.oss-cn-hangzhou.aliyuncs.com/TXT--1-e6947761a7bc48f580ba1119072058fc.txt",
          "performanceTiming": "https://testin-ee.oss-cn-hangzhou.aliyuncs.com/TXT--1-59d8338c20ab4dca841266920a139f4b.txt",
          "network": false,
          "errorMsg": "通过",
          "descr": "访问[http://www.sohu.com/]",
          "similarity": 0,
          "resultCategory": 1,
          "action": "browser_launch",
          "startTime": 1570784444869,
          "endTime": 1570784470217,
          "networkStrength": 0,
          "checkinfo": {
            "scriptDescr": "访问[http://www.sohu.com/]",
            "name": "",
            "resultCategory": 1,
            "rule": "none"
          },
          "performanceEntries": "https://testin-ee.oss-cn-hangzhou.aliyuncs.com/TXT--1-6ebbdaca533142af8385ce039478e819.txt"
        }
      }
    }
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`String`|`返回的数据`|
|`objInfo`|`基本信息`|`Object`|` `|
|`result`|` `|`Object`|` `|
|`stepnfo.errorMsg`|`步骤状态`|`String`|` `|
|`stepnfo.startTime`|`开始时间`|`timestamp`|` `|
|`stepnfo.endTime`|`结束时间`|`timestamp`|` `|
|`stepnfo.descr`|`描述`|`String`|` `|

## 网络信息筛选条件

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "realweb",
  "action": "report",
  "op": "Report.performanceCondition",
  "data": {
    "projectid": 6,
    "scriptTag": "549708",
    "stepid": 0,
    "subsubtaskid": "c8122debe1354c9a96df9a150497cb79",
    "subtaskid": "26e49fe39edf468cb9a5349e8eb41769",
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
|`taskid`|`任务ID`|`Y`|`String`|
|`subtaskid`|`子任务ID`|`Y`|`String`|
|`projectid`|`项目ID`|`Y`|`Number`|
|`scriptTag`|`脚本ID`|`Y`|`String`|
|`stepid`|`步骤id`|`Y`|`Number`|

* 返回参数

```json
{
  "data": {
    "objInfo": {
      "statusCodes": [
        200,
        0
      ],
      "initiatorTypes": [
        "navigation",
        "link",
        "img",
        "script",
        "css",
        "xmlhttprequest",
        "iframe"
      ]
    }
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`String`|`返回的数据`|
|`objInfo`|`基本信息`|`Object`|` `|
|`statusCodes`|`状态码`|`Array`|` `|
|`initiatorTypes`|`资源类型`|`Array`|` `|


## 网络步骤信息

* 地址: `http://openapi.pro.testin.cn/`
* 演示地址: 无
* 请求方式: POST

* 请求参数

```json
{
  "mkey": "realweb",
  "action": "report",
  "op": "Report.stepInternetInfo",
  "data": {
    "projectid": 6,
    "scriptTag": "549708",
    "stepid": 0,
    "subsubtaskid": "c8122debe1354c9a96df9a150497cb79",
    "subtaskid": "26e49fe39edf468cb9a5349e8eb41769",
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
|`taskid`|`任务ID`|`Y`|`String`|
|`subtaskid`|`子任务ID`|`Y`|`String`|
|`projectid`|`项目ID`|`Y`|`Number`|
|`scriptTag`|`脚本ID`|`Y`|`String`|
|`stepid`|`步骤id`|`Y`|`Number`|

* 返回参数

```json
{
  "data": {
    "list": [
      {
        "requestTime": 1570784446199,
        "transferSize": 0,
        "method": "GET",
        "serverIPAddress": "221.179.177.38",
        "requestConsume": 80.31,
        "requestDetail": {
          "receiveTime": 42.13,
          "onloadTime": 0.1,
          "resHeaderSize": 334,
          "firstPkgTime": 31.63,
          "resBodySize": 46294,
          "domloadTime": 24835.06,
          "reqStartTime": 1570784445130,
          "tcpTime": 0.39,
          "reqBodySize": 0,
          "url": "http://www.sohu.com/",
          "reqHeaderSize": 441,
          "resEndTime": 1570784445208
        },
        "url": "http://s.go.sohu.com/adgtr/?callback=jQuery112401484684985924689_1570784446032&itemspaceid=15539&sf=0&pgid=ed20682d-0134-171d-1037-84763ca008dd&newschn=1000000000&smuid=&newsid=&subid=&appid=pcnews&yyid=&adsrc=13&adps=3000250&turn=3&maxreads=1&multichn=1000000000&_=1570784446033",
        "statusCode": 200,
        "initiatorType": "script"
      }
    ]
  }
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`data`|`参数对象`|`String`|`返回的数据`|
|`list`|`基本信息`|`Object`|` `|
|`requestTime`|`请求时间`|`timestamp`|` `|
|`url`|`请求地址`|`String`|` `|
|`statusCode`|`状态码`|`Number`|` `|
|`initiatorType`|`文件类型`|`String`|` `|
|`method`|`请求方式`|`String`|` `|
|`transferSize`|`文件大小`|`Number`|` `|
|`reqStartTime`|`请求开始时间`|`timestamp`|` `|
|`resEndTime`|`响应结束时间`|`timestamp`|` `|
|`reqHeaderSize`|`请求头`|`Number`|` `|
|`reqBodySize`|`请求体`|`Number`|` `|
|`resHeaderSize`|`响应头`|`Number`|` `|
|`resBodySize`|`响应体`|`Number`|` `|
|`redirectTime`|`重定向时间`|`Number`|` `|
|`checkCacheTime`|`检查缓存`|`Number`|` `|
|`dnsTime`|`DNS解析`|`Number`|` `|
|`tcpTime`|`建立连接`|`Number`|` `|
|`sslTime`|`SSL/TLS`|`Number`|` `|
|`firstPkgTime`|`首包时间`|`Number`|` `|
|`receiveTime`|`接受数据`|`Number`|` `|
|`domloadTime`|`解析 DOM 树结构`|`Number`|` `|
|`onloadTime`|`onload事件`|`Number`|` `|

