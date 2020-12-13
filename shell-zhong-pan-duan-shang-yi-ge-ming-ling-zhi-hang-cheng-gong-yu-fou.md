---
description: shell脚本中判断上一个命令是否执行成功
---

# Shell中判断上一个命令执行成功与否

shell中使用符号“$?”来显示上一条命令执行的返回值，如果为0则代表执行成功，其他表示失败。

`if [ $? -ne 0 ]; then  
    echo "failed"  
eles  
    echo "succeed"  
fi`

或者

`if [ $? -eq 0 ]; then  
    echo "succeed"  
eles  
    echo "failed"  
fi`

| 参数 | 含义 |
| :---: | :---: |
| -eq | 等于 |
| -ne | 不等于 |
| -gt | 大于 |
| -lt | 小于 |
| ge | 大于等于 |
| le | 小于等于 |

  




