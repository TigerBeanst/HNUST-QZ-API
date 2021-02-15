# 获取教材信息

{% hint style="warning" %}
此文档目前也许不可用。

**可能是由于目前并没有对接相关内容，因为相关内容可以在 PC 版教务网访问到。**

虽然有对应的 API 地址，但目前并不知道教材信息的数据格式是怎样的，等待补充。
{% endhint %}

{% api-method method="post" host="http://kdfw.hnust.edu.cn/jsxsd" path="/student/teachingMaterial" %}
{% api-method-summary %}
获取教材信息
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
A你在登录 API 处获得的 token 字段
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="courseName" type="string" required=false %}
课程名称
{% endapi-method-parameter %}

{% api-method-parameter name="nameOrAuthor" type="string" required=false %}
书名或作者名
{% endapi-method-parameter %}

{% api-method-parameter name="semester" type="string" %}
可从学期 API 中获得。eg：2020-2021-1
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% tabs %}
{% tab title="成功" %}
```yaml
（未知）
```
{% endtab %}

{% tab title="当前无数据" %}
```yaml
{
    "Msg": "未查询到教材信息~",
    "code": "1",
    "data": []
}
```
{% endtab %}
{% endtabs %}
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



