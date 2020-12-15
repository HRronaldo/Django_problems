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

![terminal&#x62A5;&#x9519;&#x4FE1;&#x606F;](.gitbook/assets/tu-pian-%20%2828%29.png)

发现这是views.py 中的问题，让我们去/newsfeeds/api/views.py 中看看：

![/newsfeeds/api/views.py](.gitbook/assets/tu-pian-%20%2827%29.png)

发现果然，这里最后的user颜色和别的



