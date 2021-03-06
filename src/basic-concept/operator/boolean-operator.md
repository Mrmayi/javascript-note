# 条件运算符

条件操作符应该算是ECMAScript中最灵活的一种操作符了，而且它遵循与Java中的条件操作符相同的语法形式，如下面的例子所示：

```javascript
variable = boolean_expression ？ true_value : false_value;
```

本质上，这行代码的含义就是基于对boolean_expression求值的结果，决定给变量variable赋什么值。如果求值结果为true，则给变量variable赋true_value值；如果求值结果为false，则给变量variable赋false_value值。再看一个例子：

```javascript
var max = num1 > num2 ? num1 : num2；
```

在这个例子中，max中将会保存一个最大的值。这个表达式的意思是：如果num1大于num2（关系表达式返回true），则将num1的值赋给max；如果num1小于或等于num2（关系表达式返回false），则将num2的值赋给max。

* 如果在比较中，存在数字，则会将另一个数据转化为数字类型
* 如果比较的两个数值，都是字符串类型，则逐个对字符串的每个字符的 Unicode 值，进行比较