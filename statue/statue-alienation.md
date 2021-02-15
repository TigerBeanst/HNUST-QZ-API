# 获取学籍异动

{% hint style="danger" %}
此文档目前不可用。

虽然有对应的 API 地址，但目前并不知道学籍异动的数据格式是怎样的，等待补充。
{% endhint %}

{% api-method method="post" host="http://kdfw.hnust.edu.cn/bbxyhd" path="/student/statueAlienation" %}
{% api-method-summary %}
获取学籍异动
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter type="string" name="token" required=true %}
你在登录 API 处获得的 token 字段
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```yaml
{
  "Msg": "success",
  "code": "1",
  "data": []
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



