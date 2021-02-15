# 获取执行计划

{% api-method method="post" host="http://kdfw.hnust.edu.cn/bbxyhd" path="/student/executionPlan" %}
{% api-method-summary %}
获取执行计划
{% endapi-method-summary %}

{% api-method-description %}
此 API 应该是可以获取 **直到当前学期** / **所有学期（包括以后）**的课程计划
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter type="string" name="token" required=true %}
你在登录 API 处获得的 token 字段
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="semester" type="string" required=false %}
可从学期 API 中获得。eg：2020-2021-1  
未携带此参数的话，大概是获取直到当前学期的执行计划
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
      "TOTALHOURS": （学时：例如 38，number 类型）,
      "SEMESTER": 4,
      "CREDIT": （学分：例如 2，number 类型）,
      "WHETHERTOTEST": "（是否要测试：例如 是）",
      "COURSESYSTEM": "（课程类型：例如 公共基础课）",
      "OPENSEMESTER": "（开展学期：例如 2020-2021-1）",
      "COURSEATTRIBUTE": "（课程属性：必修/选修）",
      "COURSEUNITS": "（课程隶属学院：例如 招生就业处（创新创业学院））",
      "EVALUATIONMODE": "（考试方式：例如 考查、考试）",
      "COURSENAME": "（课程名称：例如 就业指导）",
      "COURSECODE": "（课程代码：例如 000000040）"
    },
    ...
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



