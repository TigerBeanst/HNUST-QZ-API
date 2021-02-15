# 获取选课数据

{% hint style="danger" %}
此文档目前不可用。

虽然有对应的 API 地址，但目前并不知道选课的数据格式是怎样的，等待补充。
{% endhint %}

{% api-method method="post" host="http://kdfw.hnust.edu.cn/jsxsd" path="/qzapp/wxgetXklc" %}
{% api-method-summary %}
获取选课数据
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```yaml
{
  "errorCode": "success",
  "errorMessage": "success",
  "errorMessageParam": [],
  "data": [],
  "runTime": ""
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



