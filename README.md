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

这时候，我们在



