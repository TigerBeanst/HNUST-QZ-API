# 获取本学期上课周数

{% api-method method="post" host="http://kdfw.hnust.edu.cn/bbxyhd" path="/teachingWeek" %}
{% api-method-summary %}
获取本学期上课周数
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
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
      "week": "1"
    },
    {
      "week": "2"
    },
    {
      "week": "3"
    },
    {
      "week": "4"
    },
    {
      "week": "5"
    },
    {
      "week": "6"
    },
    {
      "week": "7"
    },
    {
      "week": "8"
    },
    {
      "week": "9"
    },
    {
      "week": "10"
    },
    {
      "week": "11"
    },
    {
      "week": "12"
    },
    {
      "week": "13"
    },
    {
      "week": "14"
    },
    {
      "week": "15"
    },
    {
      "week": "16"
    },
    {
      "week": "17"
    },
    {
      "week": "18"
    },
    {
      "week": "19"
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



