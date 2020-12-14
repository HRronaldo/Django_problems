---
description: model 里的 generic object 会不会自动对 object_id 和 content_type 创建联合索引
---

# generic object 会不会自动对 object\_id 和 content\_type 创建联合索引

首先在项目的models.py 里面新建一个model用来验证django 会不会自动给object\_id 和content\_type 创建联合索引

![models.py](.gitbook/assets/tu-pian-%20%2817%29.png)



然后，运行`python manage.py makemigrations` 生成migrations 文件，运行`python manage.py migrate` ，完成后，进入MySQL查看效果。

在MySQL 中，使用`use twitter;` 命令将数据库切换成twitter，然后使用`show tables;` 查看所有表。

使用show index from accounts\_testmodel \G; 来查看你新建的model 所生成的索引：

> accounts\_testmodel 是你新建的model 在migrate 后生成的表名

![mysql](.gitbook/assets/tu-pian-%20%2814%29.png)

请注意：

![mysql](.gitbook/assets/tu-pian-%20%2816%29.png)

划线部分分别是两行的Column\_name，所以，得出结论：  
generic object**不会**自动对object\_id 和content\_type 创建联合索引。





