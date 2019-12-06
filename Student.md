# 东北石油大学 湖南强智教务系统 学生API

- /verifycode.servlet
  - 方法: GET
  - 作用: 获取验证码图片
- /Logon.do?method=logon
  - 方法: POST
  - 表单加密方式: application/x-www-form-urlencoded
  - 作用: 用于登录，在浏览器会存储cookie.

    表单元素 | 作用 | 备注
    -|-|-
    USERNAME|用户名|
    PASSWORD|密码|
    RANDOMCODE|验证码|
    x|不明|调用时68
    y|不明|调用时14
