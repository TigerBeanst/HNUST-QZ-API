# 获取学期考试成绩

{% hint style="warning" %}
在获取学期考试成绩时，你需要传入「学期」。

可以在 **获取当前学期** 和 **获取所有学期列表** 两个 API 中获得对应的字符串。
{% endhint %}

{% page-ref page="../term/current-term.md" %}

{% page-ref page="../term/all-term.md" %}

{% hint style="info" %}
官方在请求学期考试成绩 API 前，也按顺序（当前 → 所有）访问了上面两个提到的 API。
{% endhint %}

{% api-method method="post" host="http://kdfw.hnust.edu.cn/bbxyhd" path="/student/termGPA" %}
{% api-method-summary %}
获取学期考试成绩
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
{% api-method-parameter name="type" type="string" required=false %}
1   （未知的一个参数，改成 2 好像结果一样）
{% endapi-method-parameter %}

{% api-method-parameter name="semester" required=true type="string" %}
可从学期 API 中获得。eg：2020-2021-1
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
有效总学分/总学分绩点/平均学分绩点 似乎是从入学到实际目前的，应该不是指入学到查询学期。
{% endapi-method-response-example-description %}

```yaml
{
    "Msg": "success",
    "code": "1",
    "data": [
        {
            "studentID": "（学号）",
            "xqgpa": [],
            "achievement": [
                ...
                {
                    "curriculumAttributes": "（课程属性：必修/选修 等）",
                    "courseName": "（课程名称）",
                    "courseNature": "（课程性质：公共基础课/通识教育课/学科基础课/专业课 等）",
                    "examinationNature": "（考试性质：正常考试 等）",
                    "credit": （学分：难得的让数字以 number 返回）,
                    "cj0708id": "（应该是用来辨认特定学生的）",
                    "fraction": "（成绩：具体分数/优良中 等）"
                },
                ...
            ],
            "name": "（姓名）",
            "yxzxf": "（大概是有效总学分）",
            "zxfjd": "（大概是总学分绩点）",
            "pjxfjd": "（平均学分绩点）"
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

