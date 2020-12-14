---
description: 向一个表中插入1000行数据
---

# MySQL向某张表中循环添加数据

## 首先设置delimiter

delimiter的作用：告诉解释器，这段命令是否已经结束了，mysql是否可以执行了 默认情况下，delimiter是‘；’但是当我们编写procedure时，如果是默认设置，那么一遇到‘；’，mysql就要执行，这是我们不希望看到的



```text
delimiter //
create procedure per2() 
begin 
declare num int; 
set num=1; 
while num < 1000 do 
insert into per2(你的表名) values(concat("fan", num)); 
set num=num+1;
end while;
end
 //
```



