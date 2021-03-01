# 获取选课列表

## 选课步骤

{% hint style="info" %}
1. 获取选课大类（某一次选课，一般班级年级通知群发说要选课了就可以认为是一次大类）
2. 获取选课小类（这次大类里面，要选公选课还是其他类别的blablabla）
3. 获取选课列表
4. 选课
5. （退选）
{% endhint %}

{% api-method method="post" host="http://kdfw.hnust.edu.cn/jsxsd" path="/qzapp/wxgetKcList" %}
{% api-method-summary %}
获取选课列表
{% endapi-method-summary %}

{% api-method-description %}
此接口携带参数较多，但大部分**可能**没啥用，因为压根没传参。
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
你在登录 API 处获得的 token 字段
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="classificationCode" required=true type="string" %}
在「获取选课小类」中可以得到的值
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="rotationId" required=true %}
在「获取选课大类」中可以得到的值，应该是每个人独一无二
{% endapi-method-parameter %}

{% api-method-parameter name="sessionTime" type="string" required=true %}
时间戳，可能是从「获取选课小类」中获得的
{% endapi-method-parameter %}

{% api-method-parameter name="compulsorySemester" required=true type="string" %}
默认值为 false，不清楚作用
{% endapi-method-parameter %}

{% api-method-parameter name="compulsorySelection" required=true type="string" %}
默认值为 false，不清楚作用
{% endapi-method-parameter %}

{% api-method-parameter name="compulsoryGrades" required=true type="string" %}
默认值为 false，不清楚作用
{% endapi-method-parameter %}

{% api-method-parameter name="selectionGrades" required=true type="string" %}
默认值为 false，不清楚作用
{% endapi-method-parameter %}

{% api-method-parameter name="departmentCurriculum" type="string" required=true %}
默认值为 false，不清楚作用
{% endapi-method-parameter %}

{% api-method-parameter name="courseQualification" type="string" required=true %}
默认值为 true，不清楚作用
{% endapi-method-parameter %}

{% api-method-parameter name="courseId" type="string" %}
接口携带了这个参数，但是并没有传值
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="noticeId" %}
接口携带了这个参数，但是并没有传值
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="splitIdentification" %}
接口携带了这个参数，但是并没有传值
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="courseInformation" %}
接口携带了这个参数，但是并没有传值
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="classTeacher" %}
接口携带了这个参数，但是并没有传值
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="classWeek" %}
接口携带了这个参数，但是并没有传值
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="classSessions" %}
接口携带了这个参数，但是并没有传值
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="filteringConflicts" %}
接口携带了这个参数，但是并没有传值
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="restrictedSelection" %}
接口携带了这个参数，但是并没有传值
{% endapi-method-parameter %}

{% api-method-parameter name="fullCourse" type="string" %}
接口携带了这个参数，但是并没有传值
{% endapi-method-parameter %}

{% api-method-parameter name="generalCourseCategories" type="string" required=false %}
接口携带了这个参数，但是并没有传值
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
  "data": [
    ...
    {
      "courseName": "（课程名称 eg：插花艺术）",
      "period": "（学时 eg：24）",
      "groupName": "",
      "splitIdentification": "",
      "courseNumber": "（课程序号 eg：2002210015）",
      "classPlace": "（上课地点 eg：第八教学楼4-4）",
      "classTeacher": "（上课教师 eg：汪琼）",
      "credit": "（学分 eg：1.5）",
      "courseId": "（每个人独一无二的 id）",
      "noticeId": "（看样子应该是通知用的，一串数字）",
      "classTime": "（上课时间 eg：4-15周 星期二 9-10节）"
    }
    ...
  ],
  "runTime": ""
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

