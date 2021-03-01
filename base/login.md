---
description: 查阅前请先阅读 必读 FAQ
---

# 用户登录 - 获得 token

{% api-method method="post" host="http://kdfw.hnust.edu.cn/bbxyhd" path="/login" %}
{% api-method-summary %}
用户登录
{% endapi-method-summary %}

{% api-method-description %}
虽然请求的是 `POST` 但是实际上……内容也可以从 URL 参数里拿，即你也可以用 GET 请求它（吐了
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-form-data-parameters %}
{% api-method-parameter name="userNo" type="string" required=true %}
学号
{% endapi-method-parameter %}

{% api-method-parameter name="pwd" type="string" required=true %}
密码
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% tabs %}
{% tab title="成功" %}
{% code title="另外，这 data 下的数字似乎也都是字符串类型。。。。" %}
```yaml
{
    "code":"1",
    "Msg":"登录成功！",
    "data":{
        "birthday":"（出生日期 eg：19260817）",
        "academyName":"（学院）",
        "userNo":"（学号）",
        "entranceYear":"（入学年份/级 eg：2017）",
        "clsName":"（年级专业班级 eg：17芜湖1班）",
        "name":"（姓名）",
        "userType":"2",
        "token":"（TOKEN）"
    }
}
```
{% endcode %}
{% endtab %}

{% tab title="失败" %}
{% code title="为什么还有一个200？因为 TM 的就算失败了状态码也是 200" %}
```yaml
{
    "code": "0",
    "Msg": "该帐号不存在或密码错误！",
    "data": {}
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="success" %}
**学号密码正确的情况下，返回的 `token` 需要存下来，后续请求都需要带上它。**
{% endhint %}

下面是一个例子，后续都是类似的用法

![](../.gitbook/assets/image%20%282%29.png)

## 登录后数据存储

在上面 API 登录完成后，页面会向浏览器中写入以下内容进会话存储（sessionStorage）

| 密钥 | 值 |
| :---: | :--- |
| userInfo | 与登录 API 的响应中 data 部分的内容一致 |
| Identity | 2 （猜测应该是判断老师学生的） |
| schoolCode | 10534 （10534 是湖科大的院校代码） |
| ApiPro | undefined （大概是没加钱上高级 API） |
| isNeedLogout | 1 （令人迷惑，为什么登录状态下是1……没搞懂，猜测可能是修改密码后用的？） |
| homeMenuList | 包含有首页显示模块的 JSON，可以在 [基础-获取菜单ID](https://kdjw.docs.jakting.com/base/menu-id) 中找到 |
| menuSave | 1 |
| ifSelect | 0 |
| SelectUrl | [http://kdfw.hnust.edu.cn/jsxsd](http://kdfw.hnust.edu.cn/jsxsd)   （此处是 PC 版教务网的地址） |
| Token | ¯\\_\(ツ\)\_/¯ |



