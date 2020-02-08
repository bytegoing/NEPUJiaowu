# 东北石油大学 湖南强智教务系统 学生API

## 登录相关
- /verifycode.servlet
  - 方法: GET
  - 作用: 获取验证码图片
- /Logon.do?method=logon
  - 方法: POST
  - 表单加密方式: application/x-www-form-urlencoded
  - 作用: 用于登录，在浏览器会存储cookie.

    数据名 | 作用 | 备注
    -|-|-
    USERNAME|用户名|
    PASSWORD|密码|
    RANDOMCODE|验证码|
    useDogCode|未知|需传入null

- /Logon.do?method=logonBySSO
  - 方法: POST
  - 作用: 需要在登录成功后访问一次,否则会出现错误。


## 学生选课
- /tkglAction.do
  - 方法: GET
  - 作用: 学生选课子模块
    - 01:课表信息(本接口无法查询上课地点,如有需要请使用02-b接口)
    本接口返回一个HTML页面,其中是当前登录人某学期的简略课表信息.

    数据名 | 作用 | 备注
    -|-|-
    method|调用的功能名称|应为goListKbByXs
    xnxqh|需要查询的学期情况|例: 2018-2019-1
    zc|周数|例: 1

    - 02:选课管理
      - a.选择课程
      暂缺
      - b.查询已选课程(此接口可用来查询课表具体上课地点)
        - 本接口返回一个HTML页面,显示了当前登录人某学期的所有已选课程信息.可以根据需要提取数据.
      
      数据名 | 作用 | 备注
      -|-|-
      method|调用的功能名称|应为toFindxsyxkc
      xnxq01id|学年学期名称|例: 2018-2019-1

      - c.查询退选课程
        - 本接口返回一个HTML页面,显示了当前登录人某学期的所有退选课程信息.可以根据需要提取数据.

      数据名 | 作用 | 备注
      -|-|-
      method|调用的功能名称|应为findxswxxx
      xnxq01id|学年学期名称|例: 2018-2019-1

