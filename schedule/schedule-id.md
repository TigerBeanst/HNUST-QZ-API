# 获取课表ID

{% hint style="info" %}
在获取单周课表时，需要传入此接口中得到的 `kbjcmsid`
{% endhint %}

{% api-method method="post" host="http://kdfw.hnust.edu.cn/bbxyhd" path="/Get\_sjkbms" %}
{% api-method-summary %}
获取课表ID
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
  "msg": "success",
  "code": 1,
  "data": [
    {
      "mrms": "1",
      "kbjcmsid": "（所需的 id 内容）",
      "kbjcmsmc": "默认节次模式"
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



