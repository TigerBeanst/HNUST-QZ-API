# 【必读】FAQ

{% hint style="danger" %}
再次重申，这并不是一个官方文档，强智和学校**随时**可能改 API 导致文档失效。
{% endhint %}

{% hint style="warning" %}
**在使用除了登录以外的所有 API 时，均需要在 Header 中设置 `token`，`token` 来自登录响应**
{% endhint %}

## API 传参类型？

由于 Java 等需要写明变量类型的语言存在，因此在写传参的数据类的时候，可能需要其变量类型。像密码这种就好说，必定是 string。但学号不一定，请自行测试是 string 还是 number。

{% hint style="info" %}
**在此文档中，所有 form-data 传参值我都标明为 string，但这并不代表一定是 string**
{% endhint %}

> **为什么会有这种顾虑？**
>
> 因为你永远不知道强智的程序员是怎么写的，毕竟像登录响应里的学号、生日啥的本身只能有数字的值，也都是 `"` 引号下的内容。在响应中都是字符串了，我无法保证传参时也是吧（

![](../.gitbook/assets/image%20%283%29.png)

