---
description: 'KeyError: ''id'''
---

# Tests for tweets API报错

写完了/tweets/api/tests.py 后，快来测试一下试试，运行`python manage.py test` 发现报错：self.assertEqual\(response.data\['user'\]\['id'\], self.user1.id\) KeyError: 'id' 

![terminal&#x62A5;&#x9519;&#x4FE1;&#x606F;](.gitbook/assets/tu-pian-%20%2819%29.png)

不要惊慌，让我们去/tweets/api/tests.py 中去看看吧

![/tweets/api/tests.py](.gitbook/assets/tu-pian-%20%2820%29.png)

发现这里写的是没有问题的，报错说是KeyError: 'id' 

