# 运算符

ECMA-262描述了一组用于操作数据值的操作符，包括算术操作符（如加号和减号）、位操作符、关系操作符和相等操作符。ECMAScript操作符的与众不同之处在于，它们能够适用于很多值，例如字符串、数字值、布尔值，甚至对象。不过，在应用于对象时，相应的操作符通常都会调用对象的valueOf()和（或）toString()方法，以便取得可以操作的值。

在平时的开发当中。JS操作符 是和 JS语句 经常会搭配使用。

## 操作符优先级

操作符 | 说明
-- | --
.、[ ] 、( ) | 字段访问、数组索引、函数调用和表达式分组
++ -- - + ~ ! delete、typeof、new、void | 一元运算符、返回数据类型、对象创建、未定义的值
\*、/、% | 相乘、相除、求余数
\+、-、+、| 相加、相减、字符串串联
<< >> >>> | 移位
<、<=、>、>=、instanceof | 小于、小于或等于、大于、大于或等于、是否为特定类的实例
==、!=、===、!== | 相等、不相等、全等，不全等
& | 按位“与”
^ | 按位“异或”
&#124; | 按位“或”
&& | 逻辑“与”
&#124;&#124; | 逻辑“或”
?: | 三目元算符（条件运算）
= OP= | 赋值、赋值运算（如 += 和 &=）
, | 多个计算

```javascript
var num = 10;

if(5 == num / 2 && (2 + 2 * num).toString() === "22") {
    document.write(true);
}
// 运算符按以下顺序计算：用于分组的 ( )、*、+（分组内）、函数中的 "."、函数中的 ( )、/、==、=== 和 &&。
```

> [详细可参考-MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_Precedence#Table)

## 运算符结合性

在遇到相同优先级的运算符，就存在了运算符的结合性。而结合性，分类两种，左结合和右结合。

常用右结合的运算符包含： 一元操作符、三目运算符、赋值运算符等，其余基本都为左结合。

```javascript
1 + 1 * 3;  // 左结合

var a = b = c = 15; // 右结合

var d = 1, e = d++ + ++d;   // 一元运算符后置/前置先执行，然后执行 + 加法，最后执行 = 赋值
```

> [结合性-MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_Precedence#Associativity)