---
description: django会不会默认给foreignkey建立index
---

# Django-django会不会默认给foreignkey建立index

## 使用Explain 

explain 看一下 select \* from xxx where xxx\_id=xxx 会不会用到

## 使用

sql console Li show index

## 结论

django会默认给foreign key建立index

