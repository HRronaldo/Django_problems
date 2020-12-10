---
description: from rest_framework import permissions
---

# DRF\_permissions

from rest\_framework import permissions

## 为什么要import permissions？

原因：  
通常，仅进行身份验证或标识不足以获取信息或代码。 为此，请求访问的实体必须具有授权。\(原文：Authentication or identification by itself is not usually sufficient to gain access to information or code. For that, the entity requesting access must have authorization.）

就像authentication（身份验证）和throttling（限制），permissions（权限）确定是否应该授予或拒绝请求访问权限。

permissions（权限）用于授予或拒绝不同类别的用户对API不同部分的访问。

最简单的许可方式是允许访问任何**经过身份验证**的用户，并拒绝访问任何未经身份验证的用户。 这对应REST中的`IsAuthenticated`。

稍微不太严格的权限样式将是允许对经过身份验证的用户进行完全访问，但允许对未经身份验证的用户进行只读访问。 这对应REST中的`IsAuthenticatedOrReadOnly`。



