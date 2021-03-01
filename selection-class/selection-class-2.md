# 获取选课小类

## 选课步骤

{% hint style="info" %}
1. 获取选课大类（某一次选课，一般班级年级通知群发说要选课了就可以认为是一次大类）
2. 获取选课小类（这次大类里面，要选公选课还是其他类别的blablabla）
3. 获取选课列表
4. 选课
5. （退选）
{% endhint %}

{% api-method method="post" host="http://kdfw.hnust.edu.cn/jsxsd" path="/qzapp/wxinitXscache" %}
{% api-method-summary %}
获取选课小类
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

{% api-method-form-data-parameters %}
{% api-method-parameter name="rotationId" type="string" required=true %}
 在「获取选课大类」中可以得到的值，应该是每个人独一无二
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
有些字段我搞不太懂其意义，请自己探索
{% endapi-method-response-example-description %}

```yaml
{
    "errorCode": "success",
    "errorMessage": "success",
    "errorMessageParam": [],
    "data": {
        "classificationList": [
            {
                "classificationCode": "（课程代号 eg：06）",
                "classificationName": "（课程分类 eg：公选课选课）"
            }
        ],
        "compulsoryGrades": "false",
        "departmentCurriculum": "false",
        "sessionTime": "（当前时间的时间戳，13位 eg：1614580687099）",
        "selectionGrades": "false",
        "compulsorySemester": "false",
        "compulsorySelection": "false",
        "courseQualification": "true"
    },
    "runTime": ""
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



