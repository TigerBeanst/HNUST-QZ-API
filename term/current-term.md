# 获取当前学期

{% api-method method="post" host="http://kdfw.hnust.edu.cn/bbxyhd" path="/currentTerm" %}
{% api-method-summary %}
获取当前学期
{% endapi-method-summary %}

{% api-method-description %}
此处只需要在 Header 里附带 token 就行
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" required=true type="string" %}
你在登录 API 处获得的 token 字段
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```yaml
{
  "code": "1",
  "Msg": "success",
  "data": [
    {
      "semesterId": "2020-2021-1",
      "semesterName": "2020-2021-1"
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



