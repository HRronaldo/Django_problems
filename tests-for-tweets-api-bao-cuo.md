---
description: 'KeyError: ''id'''
---

# Tests for tweets API报错

写完了/tweets/api/tests.py 后，快来测试一下试试，运行`python manage.py test` 发现报错：self.assertEqual\(response.data\['user'\]\['id'\], self.user1.id\) KeyError: 'id' 

![terminal&#x62A5;&#x9519;&#x4FE1;&#x606F;](.gitbook/assets/tu-pian-%20%2823%29.png)

不要惊慌，让我们去/tweets/api/tests.py 中去看看吧

![/tweets/api/tests.py](.gitbook/assets/tu-pian-%20%2824%29.png)

发现这里写的是没有问题的，可是却有报错说是`KeyError: 'id'` 通常情况我们找问题从views.py 开始找起。

因为报错的是test\_create\_api，因此我们直接定位到定义create：

![/tweets/api/views.py](.gitbook/assets/tu-pian-%20%2820%29.png)

我们根据报错信息`self.assertEqual(response.data['user']['id'], self.user1.id)` 定位到第58行Response，按住Ctrl 点击TweetSerializer：

![/tweets/api/serializers.py](.gitbook/assets/tu-pian-%20%2822%29.png)

直接跳转到/tweets/api/serializers.py 的TweetSerialzier 发现这里的user 是引入的UserSerialzier 别担心，让我们再来一次，按住Ctrl 点击UserSerializer：

![/accounts/api/serializers.py](.gitbook/assets/tu-pian-%20%2819%29.png)

发现原来问题在这里呀！  
果然，fields 没有`'id'`，让我们赶紧添加上去。

![/accounts/api/serializers.py](.gitbook/assets/tu-pian-%20%2825%29.png)

这下，在运行一次tests.py 试试：`python manage.py test`

![terminal](.gitbook/assets/tu-pian-%20%2821%29.png)

Congratulation！！！



