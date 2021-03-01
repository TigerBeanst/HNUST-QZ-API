# 获取本学期个人单周课表

{% hint style="info" %}
在本接口中，你可能需要传入 `kbjcmsid`，请在「获取课表 ID」中得到对应的值
{% endhint %}

{% hint style="warning" %}
此接口似乎只能每次拿到某一周的课表，不能一次性拿到全部。

可以考虑配合「获取本学期上课周数」进行遍历。
{% endhint %}

{% page-ref page="schedule-id.md" %}

{% page-ref page="schedule-all.md" %}

{% api-method method="post" host="http://kdfw.hnust.edu.cn/bbxyhd" path="/student/curriculum" %}
{% api-method-summary %}
获取本学期个人单周课表
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
{% api-method-parameter name="kbjcmsid" type="string" required=false %}
可选。在上一节「获取课表 ID」中拿到的值
{% endapi-method-parameter %}

{% api-method-parameter name="week" type="string" %}
周次。可选，**若不携带则默认第一周。不携带时可同时不携带 kbjcmsid。**值示例：1，2，3
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
 这是一个比较完整的返回示例
{% endapi-method-response-example-description %}

```yaml
{
  "Msg": "success~",
  "code": "1",
  "data": [
    {
      "date": [
        {
          "xqmc": "一",
          "mxrq": "2021-03-01",
          "zc": "1",
          "xqid": "1"
        },
        {
          "xqmc": "二",
          "mxrq": "2021-03-02",
          "zc": "1",
          "xqid": "2"
        },
        {
          "xqmc": "三",
          "mxrq": "2021-03-03",
          "zc": "1",
          "xqid": "3"
        },
        {
          "xqmc": "四",
          "mxrq": "2021-03-04",
          "zc": "1",
          "xqid": "4"
        },
        {
          "xqmc": "五",
          "mxrq": "2021-03-05",
          "zc": "1",
          "xqid": "5"
        },
        {
          "xqmc": "六",
          "mxrq": "2021-03-06",
          "zc": "1",
          "xqid": "6"
        }
      ],
      "item": [
        {
          "jx0408id": "（个人独一无二的id）",
          "classWeek": "1-14",
          "courseName": "操作系统",
          "isRepeatCode": "0",
          "teacherName": "朱彬",
          "buttonCode": "0",
          "startTime": "08:00",
          "endTIme": "09:40",
          "location": "第五教学楼405",
          "classWeekDetails": ",1,2,3,4,5,6,7,8,9,10,11,12,13,14,",
          "classTime": "10102",
          "coursesNote": 2
        },
        {
          "jx0408id": "（个人独一无二的id）",
          "classWeek": "1-14",
          "courseName": "毛泽东思想和中国特色社会主义理论体系概论",
          "isRepeatCode": "0",
          "teacherName": "管桂翠",
          "buttonCode": "0",
          "startTime": "14:30",
          "endTIme": "16:10",
          "location": "第五教学楼1-1",
          "classWeekDetails": ",1,2,3,4,5,6,7,8,9,10,11,12,13,14,",
          "classTime": "10506",
          "coursesNote": 2
        },
        {
          "jx0408id": "（个人独一无二的id）",
          "classWeek": "1-10",
          "courseName": "大学英语(4)",
          "isRepeatCode": "0",
          "teacherName": "任日方",
          "buttonCode": "0",
          "startTime": "10:00",
          "endTIme": "11:40",
          "location": "第五教学楼306",
          "classWeekDetails": ",1,2,3,4,5,6,7,8,9,10,",
          "classTime": "20304",
          "coursesNote": 2
        },
        {
          "jx0408id": "（个人独一无二的id）",
          "classWeek": "1-8",
          "courseName": "Internet与Web编程A",
          "isRepeatCode": "0",
          "teacherName": "周付章",
          "buttonCode": "0",
          "startTime": "19:30",
          "endTIme": "21:10",
          "location": "第五教学楼2-2",
          "classWeekDetails": ",1,2,3,4,5,6,7,8,",
          "classTime": "20910",
          "coursesNote": 2
        },
        {
          "jx0408id": "（个人独一无二的id）",
          "classWeek": "1-14",
          "courseName": "操作系统",
          "isRepeatCode": "0",
          "teacherName": "朱彬",
          "buttonCode": "0",
          "startTime": "08:00",
          "endTIme": "09:40",
          "location": "第五教学楼405",
          "classWeekDetails": ",1,2,3,4,5,6,7,8,9,10,11,12,13,14,",
          "classTime": "30102",
          "coursesNote": 2
        },
        {
          "jx0408id": "（个人独一无二的id）",
          "classWeek": "1-14",
          "courseName": "毛泽东思想和中国特色社会主义理论体系概论",
          "isRepeatCode": "0",
          "teacherName": "管桂翠",
          "buttonCode": "0",
          "startTime": "16:30",
          "endTIme": "18:10",
          "location": "第五教学楼1-1",
          "classWeekDetails": ",1,2,3,4,5,6,7,8,9,10,11,12,13,14,",
          "classTime": "30708",
          "coursesNote": 2
        },
        {
          "jx0408id": "（个人独一无二的id）",
          "classWeek": "1-8",
          "courseName": "数字系统设计A",
          "isRepeatCode": "0",
          "teacherName": "余庆春",
          "buttonCode": "0",
          "startTime": "19:30",
          "endTIme": "21:10",
          "location": "第五教学楼509",
          "classWeekDetails": ",1,2,3,4,5,6,7,8,",
          "classTime": "30910",
          "coursesNote": 2
        },
        {
          "jx0408id": "（个人独一无二的id）",
          "classWeek": "1-8",
          "courseName": "Internet与Web编程A",
          "isRepeatCode": "0",
          "teacherName": "周付章",
          "buttonCode": "0",
          "startTime": "08:00",
          "endTIme": "09:40",
          "location": "第五教学楼3-1",
          "classWeekDetails": ",1,2,3,4,5,6,7,8,",
          "classTime": "40102",
          "coursesNote": 2
        },
        {
          "jx0408id": "（个人独一无二的id）",
          "classWeek": "1-10",
          "courseName": "大学英语(4)",
          "isRepeatCode": "0",
          "teacherName": "任日方",
          "buttonCode": "0",
          "startTime": "16:30",
          "endTIme": "18:10",
          "location": "第五教学楼306",
          "classWeekDetails": ",1,2,3,4,5,6,7,8,9,10,",
          "classTime": "40708",
          "coursesNote": 2
        },
        {
          "jx0408id": "（个人独一无二的id）",
          "classWeek": "1-8",
          "courseName": "数字系统设计A",
          "isRepeatCode": "0",
          "teacherName": "余庆春",
          "buttonCode": "0",
          "startTime": "10:00",
          "endTIme": "11:40",
          "location": "第五教学楼509",
          "classWeekDetails": ",1,2,3,4,5,6,7,8,",
          "classTime": "50304",
          "coursesNote": 2
        },
        {
          "jx0408id": "（个人独一无二的id）",
          "classWeek": "1-4",
          "courseName": "操作系统",
          "isRepeatCode": "0",
          "teacherName": "朱彬",
          "buttonCode": "0",
          "startTime": "14:30",
          "endTIme": "16:10",
          "location": "第五教学楼401",
          "classWeekDetails": ",1,2,3,4,",
          "classTime": "50506",
          "coursesNote": 2
        }
      ],
      "week": 1,
      "weekday": "一"
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



