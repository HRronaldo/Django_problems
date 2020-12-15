---
description: 'AttributeError: ''NoneType'' object has no attribute ''user'''
---

# NewsFeeds views.py报错

`"GET /api/newsfeeds/ HTTP/1.1" 500 92540`

写完一个app 的views.py 在配置好url后，总是想在browser 中看看界面。

在写好了NewsFeeds 的views.py 后，运行`python manage.py runserver` 看看界面：

![http://127.0.0.1:8000/api/newsfeeds/](.gitbook/assets/tu-pian-%20%2826%29.png)

发现报错：AttributeError: 'NoneType' object has no attribute 'user'  
这个错误的意思是：属性错误，NoneType对象没有user属性。

别担心，让我们看看terminal 的报错信息：

![terminal&#x62A5;&#x9519;&#x4FE1;&#x606F;](.gitbook/assets/tu-pian-%20%2829%29.png)

发现这是views.py 中的问题，让我们去/newsfeeds/api/views.py 中看看：

![/newsfeeds/api/views.py](.gitbook/assets/tu-pian-%20%2828%29.png)

发现果然，像报错信息里说的那样，第13行，这里最后的user颜色和别的代码颜色都不一样

仔细看看代码，哦~原来是前面写错了，这里应该是`self.request.user`，我们需要的是这个请求的user，但是不小心写成了queryset，这说明光用tab 联想写习惯了也是会有问题滴。

让我们修改一下试试

![/newsfeeds/api/views.py](.gitbook/assets/tu-pian-%20%2830%29.png)

运行一下：

![http://127.0.0.1:8000/api/newsfeeds/](.gitbook/assets/tu-pian-%20%2827%29.png)

果然成功啦！

