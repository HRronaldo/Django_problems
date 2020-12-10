---
description: '"GET /api/accounts/ HTTP/1.1" 404 4509'
---

# Signin & Signup

## 场景

写完signin & signup 之后，迫不及待的想在browser进去试试。突然发现报错："GET /api/accounts/ HTTP/1.1" 404 4509

往上看了看，发现："GET /api/accounts/ HTTP/1.1" 404 4509

![terminal&#x4E2D;&#x7684;&#x62A5;&#x9519;&#x4FE1;&#x606F;](.gitbook/assets/tu-pian-%20%282%29.png)

## 思路

碰到404报错，首先想的就是页面找不到了，那就去看看url有没有写错吧~

/twitter/urls.py

![/twitter/urls.py](.gitbook/assets/tu-pian-%20%281%29.png)

发现router有accounts且写的没问题，推断应该不是忘记写url了。

这时候，我们在去看一眼browser的页面：

![browser: http://127.0.0.1:8000/api/accounts/](.gitbook/assets/tu-pian-%20%283%29.png)

仔细阅读下面的5-10，发现原来accounts应该这么用：  
例如：accounts/login/

那就来尝试一下accounts/login/ ：

![browser: http://127.0.0.1:8000/api/accounts/login/](.gitbook/assets/tu-pian-%20%284%29.png)

Unfortunately，又遇到了另一个报错AssertionError（当assert断言条件为假的时候抛出的异常）

阅读一下报错信息：“The field 'emial' was declared on serializer SignupSerializer, but has not been included in the 'fields' option. ”意思是：字段“ emial”已在序列化程序SignupSerializer上声明，但未包含在“ fields”选项中。

此时，让我们回到serializers.py中

![/accounts/api/serializers.py](.gitbook/assets/tu-pian-%20%285%29.png)

发现，fields中明明有email ，为什么会报这个错呢？  
哦~~~原来如此，发现是拼写错误，将email拼写成了emial，更改+保存，迫不及待的再进入browser试试。





