---
description: 'FAIL: test_create_with_files (tweets.api.tests.TweetAPITests)'
---

# SimpleUploadedFile报错

FAIL: test\_create\_with\_files \(tweets.api.tests.TweetAPITests\)

在文件上传的测试中，一个 SimpleUploadedFile一旦被上传之后，第二次再用，内容就是空的，会导致出错：

![terminal&#x62A5;&#x9519;&#x4FE1;&#x606F;](.gitbook/assets/tu-pian-%20%2832%29.png)

错误写法：

![tests.py](.gitbook/assets/tu-pian-%20%2831%29.png)

正确写法：

![tests.py](.gitbook/assets/tu-pian-%20%2834%29.png)





