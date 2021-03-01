# 获取选课大类

## 选课步骤

{% hint style="info" %}
1. 获取选课大类（某一次选课，一般班级年级通知群发说要选课了就可以认为是一次大类）
2. 获取选课小类（这次大类里面，要选公选课还是其他类别的blablabla）
3. 获取选课列表
4. 选课
5. （退选）
{% endhint %}

{% api-method method="post" host="http://kdfw.hnust.edu.cn/jsxsd" path="/qzapp/wxgetXklc" %}
{% api-method-summary %}
获取选课大类
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
  "errorCode": "success",
  "errorMessage": "success",
  "errorMessageParam": [],
  "data": [
        {
            "dailycourseselection": "（每天选课时间 eg：不控制）",
            "conflictselection": "（允许冲突选课 eg：否）",
            "semesterid": "（学期 eg：2020-2021-2）",
            "courseselectioncontrol": "（选课控制 eg：可选可退）",
            "preselectedcourses": "（预置课是否可退 eg：否）",
            "rotationname": "（选课名称 eg：通识教育课选课（第一轮））",
            "drawlots": "（选课抽签 eg：未启用）",
            "populationcontrol": "（教学班选课人数 eg：控制)",
            "creditcontrol": null,
            "rotationid": "(大概是每个人特有的 id ！！此值将将在「获取选课小类」中使用到)",
            "courseselectiontime": "（选课时间起止 eg：2021-03-01 12:00~2021-03-09 23:59）"
        }
    ],
  "runTime": ""
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



