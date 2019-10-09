# 登陆功能

 总路径: /mobile/user
* 地址: ` /login`
* 演示地址: [http://localhost:8899/mobile/user/login?user=zhangsan&password=123456](http://localhost:8899/mobile/user/login?user=zhangsan&password=123456)
* 请求方式: POST

* 请求参数

|字段|说明|必填|类型|
|---|---|---|---|
|`username`|`用户名`|`Y`|`String`|
|`password`|`密码`|`Y`|`String`|

* 返回参数

```json
{
  "status": 1,
  "msg": "success"
}
```

* 返回字段说明

|字段|说明|字段类型|备注|
|---|---|---|---|
|`status`|`状态码`|`Number`|`1表示成功`|
|`msg`|`状态码对应信息`|`String`|`成功或失败信息`|

