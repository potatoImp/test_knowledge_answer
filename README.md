# test_knowledge_answer
测试面试问题汇总

## 数据库

### 基础
1.关键字执行顺序（group by 和where哪个先执行）

2.mysql inner join 和 letf join 的区别

结果集内容差异：
INNER JOIN：只返回两个表中连接条件相匹配的行。如果连接的列在任一表中没有匹配的行，那么这些行将不会出现在结果集中。
LEFT JOIN（或LEFT OUTER JOIN）：返回左表（即LEFT JOIN之后的第一个表）的所有行，即使右表（第二个表）中没有匹配的行。
如果右表中没有匹配的行，结果集中相应的列将包含NULL值。

性能上，LEFT JOIN可能比INNER JOIN稍微慢一些，因为它需要扫描左表的所有行，即使某些行在右表中没有匹配的行。
然而，性能差异通常很小，并且取决于具体的查询和数据库的执行计划。



## 编程语言

### python

1.python list 取出第二到第五个值
第一种切片：sub_list = my_list[1:5]  # 取出索引1到4的元素
第二种循环：通过range()函数与循环配合遍历取出值
第三种删除：通过del删除第一个与第五个之后的del my_list[1:5] 





## 性能相关
### 性能测试手段
1.性能测试如何发起压力（施加压力）
首先通过性能测试工具jmeter或者自开发工具，编写对应的场景任务来模拟用户的行为
（python可以通过request、socket，golang可以通过net库实现）
其次设置合理的并发用户数、持续时间、请求频率等参数，实现线性增加，阶梯增加和波峰波谷等模式，在一台或多台服务器上发起压力
