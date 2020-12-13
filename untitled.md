---
description: 'AssertionError: 301 != 405'
---

# Tests for accounts API报错

写好了/accounts/tests.py，使用`python manage.py test`命令，来看看测试成果吧。

Unfortunately，遇到了报错：`FAILED (failures=2)`，不要惊慌我们来看一看报错信息：

![terminal&#x62A5;&#x9519;&#x4FE1;&#x606F;](.gitbook/assets/tu-pian-%20%288%29.png)

根据报错信息`AssertionError: 301 != 405`，我们要知道，http状态码301是作用是定向跳转提示。这个报错说明，我们没有跳转到原先我们设定好的url，因此没有报我们预先设置的报错状态码405。

因此我们根据错误提示，去/accounts/tests.py中去看看第72行和第89行。

![/accounts/testy.py line72](.gitbook/assets/tu-pian-%20%287%29.png)



![/accounts/testy.py line89](.gitbook/assets/tu-pian-%20%2810%29.png)

通过代码，我们可以知道，这两个报错涉及到的部分分别是logout和signup，让我们回看一下这两个部分的url：

![/accounts/tests.py](.gitbook/assets/tu-pian-%20%2812%29.png)

发现果然是url写错了，少加了“/”，让我们添加上去看看效果吧！

![/accounts/tests.py](.gitbook/assets/tu-pian-%20%2811%29.png)

再次运行`python manage.py test`看看：

![terminal&#x754C;&#x9762;](.gitbook/assets/tu-pian-%20%289%29.png)

Congratulation！！！

