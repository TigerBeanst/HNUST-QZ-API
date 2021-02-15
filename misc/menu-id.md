---
description: 此页面可以跳过，因为意义不大。
---

# 获取菜单 ID

移动版教务系统在部分情况下需要携带菜单 ID 才可继续获得子菜单 ID。

虽然我觉得这个 API 对于我们这种**有目的性地使用**（指直接请求到子菜单对应的 API）的时候没有多大意义，但是既然网页实际请求了，在这里也做一下记录。

**举个例子**，在移动版教务上点击「成绩」，页面会先向获取菜单 ID 的 API 请求所有菜单（主要是需要它们对应的 `i_id`，然后再向另一个 API 请求其子菜单）。

{% hint style="info" %}
在这个例子中，父菜单「成绩」拥有子菜单「学期考试成绩」和「等级考试成绩」
{% endhint %}

{% api-method method="post" host="http://kdfw.hnust.edu.cn/bbxyhd" path="/FindSch\_Int" %}
{% api-method-summary %}
获取学校父菜单 ID
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
{% api-method-parameter name="xx0101id" type="string" required=true %}
10534  （湖南科技大学的院校代码）
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=false %}
0    （此值似乎是可选的，如果不加似乎会带上一堆教师端的菜单）
{% endapi-method-parameter %}

{% api-method-parameter name="isqy" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="key" type="string" required=false %}
qzkj
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "msg": "success",
    "code": 1,
    "data": [
        {
            "is_home": "1",
            "i_id": "3F97250FB6474E78B80F203E8F7615E3",
            "isqy": "1",
            "url": "xs_bjkb",
            "name": "班级课表",
            "schoolname": "湖南科技大学本部",
            "id": "F7203D5FCA204EECA981620427FAEDC0"
        },
        {
            "is_home": "0",
            "i_id": "A79EC55C55F15657E0530100007F9B61",
            "isqy": "1",
            "url": "js_pyfa_zg",
            "name": "培养方案总纲",
            "schoolname": "湖南科技大学本部",
            "id": "565BAEFEEEA54FFA95220ECA25D39988"
        },
        {
            "is_home": "0",
            "i_id": "A79EC55C55F25657E0530100007F9B61",
            "isqy": "1",
            "url": "js_pyfa_zy",
            "name": "专业培养方案",
            "schoolname": "湖南科技大学本部",
            "id": "20815A7C35174B5A8AC0019296505D02"
        },
        {
            "is_home": "0",
            "i_id": "A79EC55C55F35657E0530100007F9B61",
            "isqy": "1",
            "url": "js_pyfa_zyjxjc",
            "name": "专业教学进程",
            "schoolname": "湖南科技大学本部",
            "id": "7FE36CB332F940128F0E37074FB73233"
        },
        {
            "is_home": "0",
            "i_id": "A79EC55C55F45657E0530100007F9B61",
            "isqy": "1",
            "url": "js_pyfa_jxjh",
            "name": "教学计划 ",
            "schoolname": "湖南科技大学本部",
            "id": "E649F0362C6A413292CBDA8C1D1EED88"
        },
        {
            "is_home": "0",
            "i_id": "A79EC55C55F65657E0530100007F9B61",
            "isqy": "1",
            "url": "/teacher/getCjxgxx",
            "name": "成绩修改",
            "schoolname": "湖南科技大学本部",
            "id": "9D0B970F0F9D404E858E1A24FBCEA3B7"
        },
        {
            "is_home": "0",
            "i_id": "A79EC55C55FA5657E0530100007F9B61",
            "isqy": "1",
            "url": "xs_xjyd",
            "name": "学籍异动 ",
            "schoolname": "湖南科技大学本部",
            "id": "AB0358AF61C8487FA31584B8A14BB0F4"
        },
        {
            "is_home": "0",
            "i_id": "A79EC55C55FB5657E0530100007F9B61",
            "isqy": "1",
            "url": "xs_xjyj",
            "name": "学籍预警 ",
            "schoolname": "湖南科技大学本部",
            "id": "A52E6AD11E82427BA23DD66A63E84AB2"
        },
        {
            "is_home": "0",
            "i_id": "A79EC55C55FC5657E0530100007F9B61",
            "isqy": "1",
            "url": "xs_cj_xq",
            "name": "学期考试成绩 ",
            "schoolname": "湖南科技大学本部",
            "id": "72E26E244AD74E899FFCE564C139BF5F"
        },
        {
            "is_home": "0",
            "i_id": "A79EC55C55FD5657E0530100007F9B61",
            "isqy": "1",
            "url": "xs_cj_dj",
            "name": "等级考试成绩 ",
            "schoolname": "湖南科技大学本部",
            "id": "3D4E7B6B16B740568365EED49108A653"
        },
        {
            "is_home": "0",
            "i_id": "A79EC55C55FF5657E0530100007F9B61",
            "isqy": "1",
            "url": "xs_pyfa_jxjd",
            "name": "教学进度 ",
            "schoolname": "湖南科技大学本部",
            "id": "3EC4B5F2D5AA48F6A2B0435E13227D33"
        },
        {
            "is_home": "0",
            "i_id": "A79EC55C56005657E0530100007F9B61",
            "isqy": "1",
            "url": "xs_pyfa_zxjh",
            "name": "执行计划 ",
            "schoolname": "湖南科技大学本部",
            "id": "CE0562287C3E4BEABDE681CF916743F8"
        },
        {
            "is_home": "0",
            "i_id": "A79EC55C56015657E0530100007F9B61",
            "isqy": "1",
            "url": "xs_pyfa_mx",
            "name": "培养方案明细 ",
            "schoolname": "湖南科技大学本部",
            "id": "4791C5FAE60143C38CD3D3FACE428A04"
        },
        {
            "is_home": "0",
            "i_id": "A8311622AA255EE2E0530100007F0BC2",
            "isqy": "1",
            "url": "js_jxpj_jxxfpc",
            "name": "教学学风评测",
            "schoolname": "湖南科技大学本部",
            "id": "05CE134E3D7544D0AF7821F253E6E4DD"
        },
        {
            "is_home": "0",
            "i_id": "A8311622AA275EE2E0530100007F0BC2",
            "isqy": "1",
            "url": "js_jxpj_gzlcx",
            "name": "工作量查询",
            "schoolname": "湖南科技大学本部",
            "id": "AEB1CF77FA374523AF6973F618FEE410"
        },
        {
            "is_home": "0",
            "i_id": "A8311622AA285EE2E0530100007F0BC2",
            "isqy": "1",
            "url": "js_jxpj_jxpj",
            "name": "教学评价",
            "schoolname": "湖南科技大学本部",
            "id": "315CF11B61D640209DC171474B9611C5"
        },
        {
            "is_home": "1",
            "i_id": "A1BA71608C47653AE0530100007F3E11",
            "isqy": "1",
            "url": "xs_cj",
            "name": "成绩",
            "schoolname": "湖南科技大学本部",
            "id": "5B3FDC63707F4033B9D2944AC42AABAE"
        },
        {
            "is_home": "1",
            "i_id": "A1BA71608C48653AE0530100007F3E11",
            "isqy": "1",
            "url": "xs_xjgl",
            "name": "学籍管理",
            "schoolname": "湖南科技大学本部",
            "id": "5FAF6382D8A14A2D867D3D035A15EB1C"
        },
        {
            "is_home": "1",
            "i_id": "A1BA71608C49653AE0530100007F3E11",
            "isqy": "1",
            "url": "xs_ksap",
            "name": "考试安排",
            "schoolname": "湖南科技大学本部",
            "id": "8766CB0EB8224556A297109B9A9E783F"
        },
        {
            "is_home": "1",
            "i_id": "A1BA71608C4B653AE0530100007F3E11",
            "isqy": "1",
            "url": "xs_djksbm",
            "name": "等级考试报名",
            "schoolname": "湖南科技大学本部",
            "id": "51B44F0B4948490A897555632F1F5492"
        },
        {
            "is_home": "1",
            "i_id": "A1BA71608C4C653AE0530100007F3E11",
            "isqy": "1",
            "url": "xs_kxjs",
            "name": "空闲教室",
            "schoolname": "湖南科技大学本部",
            "id": "79860E8C818F40828C34164D9AB820E5"
        },
        {
            "is_home": "1",
            "i_id": "A1BA71608C4D653AE0530100007F3E11",
            "isqy": "1",
            "url": "xs_pyfa",
            "name": "培养方案",
            "schoolname": "湖南科技大学本部",
            "id": "4F72A9D5236845A9867873873C3B520D"
        },
        {
            "is_home": "1",
            "i_id": "A1BA71608C4E653AE0530100007F3E11",
            "isqy": "1",
            "url": "xs_xspj",
            "name": "学生评教",
            "schoolname": "湖南科技大学本部",
            "id": "5C65DF1CBF6143E497F6A82EB38FC4B1"
        },
        {
            "is_home": "1",
            "i_id": "A1BA71608C4F653AE0530100007F3E11",
            "isqy": "1",
            "url": "xs_xk",
            "name": "选课",
            "schoolname": "湖南科技大学本部",
            "id": "C14D0C18215E44CDA9027A7C6C4AC6F0"
        },
        {
            "is_home": "1",
            "i_id": "A1BA71608C50653AE0530100007F3E11",
            "isqy": "1",
            "url": "xs_kcb",
            "name": "课程表",
            "schoolname": "湖南科技大学本部",
            "id": "444DFF76ED30486FAD39C79078C5E31A"
        },
        {
            "is_home": "1",
            "i_id": "A1BA71608C51653AE0530100007F3E11",
            "isqy": "1",
            "url": "xs_jc",
            "name": "教材",
            "schoolname": "湖南科技大学本部",
            "id": "87D56276C5EF48D9B9CCFB78311B02F3"
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

参数中的 `xx0101id` 实际上是湖南科技大学的院校代码，`key` 是`强智科技`的缩写。

在上面可以找到「成绩」的`i_id` 是`A1BA71608C47653AE0530100007F3E11` 。因此我们可以向其子菜单 API 请求。

{% api-method method="post" host="http://kdfw.hnust.edu.cn/bbxyhd" path="/FindSch\_Submenu" %}
{% api-method-summary %}
获取学校子菜单 ID
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="I\_ID" type="string" required=true %}
父菜单中对应的 i\_id。例如上面的成绩的 id 是 A1BA71608C47653AE0530100007F3E11，此处就可以直接传入这个字符串
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter type="string" name="token" required=true %}
你在登录 API 处获得的 token 字段
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

{% tabs %}
{% tab title="成功" %}
```yaml
{
  "code": "1",
  "Msg": "成功！",
  "data": [
    {
      "is_home": "0",
      "type": "0",
      "sort_number": "112",
      "i_id": "A79EC55C55FC5657E0530100007F9B61",
      "url": "xs_cj_xq",
      "name": "学期考试成绩 "
    },
    {
      "is_home": "0",
      "type": "0",
      "sort_number": "113",
      "i_id": "A79EC55C55FD5657E0530100007F9B61",
      "url": "xs_cj_dj",
      "name": "等级考试成绩 "
    }
  ]
}
```
{% endtab %}

{% tab title="失败" %}
{% code title="没想到吧，这 b 还是成功返回嗷。只能通过判断 data 长度来判断是否成功了。" %}
```yaml
{
    "code": "1",
    "Msg": "成功！",
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



