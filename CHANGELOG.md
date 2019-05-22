

### 1.2.1

- FIX:
  - ldap 账号登录失败，原因是因为禅道现在默认对密码进行 MD5 ，所以需要禁用这个行为，
    通过添加配置：`$config->notMd5Pwd = true;` 解决
  - ldap 测试账号服务器是否有效失败，发现是因为 js 中的 createLink 函数无法处理复杂的 GET 字符串引起的，
    使用 POST 请求解决了这个问题