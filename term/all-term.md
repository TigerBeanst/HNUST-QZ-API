# 获取所有学期列表

{% api-method method="post" host="http://kdfw.hnust.edu.cn/bbxyhd" path="/semesterList" %}
{% api-method-summary %}
获取所有学期列表
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter type="string" name="token" required=true %}
你在登录 API 处获得的 token 字段
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
这里很奇怪，我 2017 年入学，从 2017 开始没问题。但是这愣是拖到了 2024 年……（不过在这套 API 里奇怪的东西多了去了（跑
{% endapi-method-response-example-description %}

```yaml
{
  "code": "1",
  "Msg": "success",
  "data": [
    {
      "semesterId": "2023-2024-2",
      "semesterName": "2023-2024-2"
    },
    {
      "semesterId": "2023-2024-1",
      "semesterName": "2023-2024-1"
    },
    {
      "semesterId": "2022-2023-2",
      "semesterName": "2022-2023-2"
    },
    {
      "semesterId": "2022-2023-1",
      "semesterName": "2022-2023-1"
    },
    {
      "semesterId": "2021-2022-2",
      "semesterName": "2021-2022-2"
    },
    {
      "semesterId": "2021-2022-1",
      "semesterName": "2021-2022-1"
    },
    {
      "semesterId": "2020-2021-2",
      "semesterName": "2020-2021-2"
    },
    {
      "semesterId": "2020-2021-1",
      "semesterName": "2020-2021-1"
    },
    {
      "semesterId": "2019-2020-2",
      "semesterName": "2019-2020-2"
    },
    {
      "semesterId": "2019-2020-1",
      "semesterName": "2019-2020-1"
    },
    {
      "semesterId": "2018-2019-2",
      "semesterName": "2018-2019-2"
    },
    {
      "semesterId": "2018-2019-1",
      "semesterName": "2018-2019-1"
    },
    {
      "semesterId": "2017-2018-2",
      "semesterName": "2017-2018-2"
    },
    {
      "semesterId": "2017-2018-1",
      "semesterName": "2017-2018-1"
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



