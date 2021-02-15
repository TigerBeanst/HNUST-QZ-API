# 获取等级考试成绩

{% api-method method="post" host="http://kdfw.hnust.edu.cn/bbxyhd" path="/student/socialTestScores" %}
{% api-method-summary %}
获取等级考试成绩
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
    "Msg": "success",
    "code": "1",
    "data": [
        ...
        {
            "date": "（考试日期：例如 2018-12-15）",
            "courseName": "（考试名称：例如 全国大学英语四六级考试）",
            "socialExaminationGradeName": "（社会考试名称：例如 CET6/湖南省普通话测试）",
            "skcjid": "（应该是用来辨认特定学生的）",
            "writtenTestScore": "（笔试成绩：似乎都是 0）",
            "admissionTicketNumber": "（准考证号码：系统估计没记录，直接显示 暂无）",
            "practiceScore": "（实践分数：似乎都是 0）",
            "overallResult": "（最终分数：也就是你这场考试最后看的分数）"
        },
        ...
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



