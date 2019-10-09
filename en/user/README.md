# loginFunction

 total-address: /mobile/user
* address: ` /login`
* demo-address: [http://localhost:8899/mobile/user/login?user=zhangsan&password=123456](http://localhost:8899/mobile/user/login?user=zhangsan&password=123456)
* methods: POST

* request field

|field|instructions|mandatory|type|
|---|---|---|---|
|`username`|`username`|`Y`|`String`|
|`password`|`password`|`Y`|`String`|

* response params

```json
{
  "status": 1,
  "msg": "success"
}
```

* response field

|field|instructions|type|note|
|---|---|---|---|
|`status`|`status code`|`Number`|`1success`|
|`msg`|`Status codes correspond to information`|`String`|`Success or failure information`|

