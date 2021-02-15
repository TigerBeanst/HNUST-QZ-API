# 获取学籍预警

{% hint style="info" %}
**此 API 有些迷惑。**

它对每个学期会产生若干个条目，即使对应的学生在对应的学期并没有被学籍预警过，而且这些条目的预警内容实际为空。

而且这些条目数量未知，不清楚对应关系是什么。
{% endhint %}

{% api-method method="post" host="http://kdfw.hnust.edu.cn/bbxyhd" path="/student/statueWaring" %}
{% api-method-summary %}
获取全部学籍预警
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
{% api-method-parameter name="isCurrent" type="string" required=false %}
当此字段为 1 时，将返回**当前学期**的学籍预警；  
若不携带此字段或不为 1 时，将返回**所有学期**的预警
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```yaml
{
    "Msg": "success",
    "code": "1",
    "data": [
        ...
        {
            "warningName": "（警告名称：例如 19-20学年学分清理）",
            "semester": "（学期：例如 2020-2021-1）",
            "majorName": "（专业名称）",
            "warningId": "（应该是用来辨认特定学生的）",
            "resultName": "（预警内容）"
        },
        ...
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

`resultName` 示例：

* 一学期未取得学分大于或等于1/3小于2/3
* 留级
* 警示

{% api-method method="post" host="http://kdfw.hnust.edu.cn/bbxyhd" path="/student/warningDetail" %}
{% api-method-summary %}
获取特定学籍预警详情
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
{% api-method-parameter required=true name="warningId" type="string" %}
警告 ID，可在上一个 API 中获取
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
            "warningName": "（警告名称：例如 19-20学年学分清理）",
            "semester是警告": "（学期：例如 2020-2021-1）",
            "majorName": "（专业名称）",
            "warningId": "（应该是用来辨认特定学生的）",
            "resultName": "（预警内容）"
        }
    ]
}
```
{% endtab %}

{% tab title="失败" %}
{% code title="震惊，强智程序员终于没有在这种情况下还判定成功了！这里是不携带 warningId 的情况。" %}
```yaml
{
    "Msg": "error!服务器内部错误~",
    "code": "0",
    "data": []
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

`resultName` 示例：

* 一学期未取得学分大于或等于1/3小于2/3
* 留级
* 警示

