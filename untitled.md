---
description: 'AssertionError: 301 != 405'
---

# Tests for accounts API报错

写好了/accounts/tests.py，使用`python manage.py test`命令，来看看测试成果吧。

Unfortunately，遇到了报错：`FAILED (failures=2)`，不要惊慌我们来看一看报错信息：

![terminal&#x62A5;&#x9519;&#x4FE1;&#x606F;](.gitbook/assets/tu-pian-%20%287%29.png)

根据报错信息`AssertionError: 301 != 405`，我们要知道，http状态码301是作用是定向跳转提示。这个报错说明，我们没有跳转到原先我们设定好的url，因此没有报我们预先设置的报错状态码405。



