# 获取教学进度

{% hint style="warning" %}
获取教学进度时，你需要传入「学期」。

可以在 **获取当前学期** 和 **获取所有学期列表** 两个 API 中获得对应的字符串。
{% endhint %}

{% page-ref page="../term/current-term.md" %}

{% page-ref page="../term/all-term.md" %}

{% api-method method="post" host="http://kdfw.hnust.edu.cn/bbxyhd" path="/student/teachingProgress" %}
{% api-method-summary %}
获取教学进度
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

{% api-method-form-data-parameters %}
{% api-method-parameter name="semester" type="string" %}
可从学期 API 中获得。eg：2020-2021-1  
此处有些迷惑，即使不传此参数也可能会显示数据，预计**可能是默认当前学期**。
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
{
    "Msg": "success",
    "code": "1",
    "data": [
        {
            "ProgressName": "专业实习",
            "Week": "第1周"
        },
        {
            "ProgressName": "专业实习",
            "Week": "第2周"
        }
    ]
}
```
{% endtab %}

{% tab title="学期有误" %}
```yaml
{
  "Msg": "当前学年学期还没有教学进度!",
  "code": "1",
  "data": "[]"
}
```
{% endtab %}
{% endtabs %}
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



