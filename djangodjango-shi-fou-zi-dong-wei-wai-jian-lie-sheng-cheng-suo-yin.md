---
description: django是否自动为外键列生成索引
---

# Django-django是否自动为外键列生成索引

## Django是自动为外键生成索引，还是仅取决于基础数据库策略？

取决于 db\_indexForeignKey中的参数，默认情况下为True。  
Django自动为所有 创建索引 `models.ForeignKey`列 。  
在上自动创建数据库索引 `ForeignKey`。 可以通过设置禁用此功能 `db_index`为 `False`。 如果要创建外键以保持一致性而不是联接，或者要创建替代索引（例如部分或多列索引），则可能要避免索引的开销。

  


