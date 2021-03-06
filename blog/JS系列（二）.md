> 学前端也快一年了，最近想试试大公司的面试，然后这里把所有的知识点都整理出来，然后慢慢消化。该片总字数：1770，速读三分半，普通6分钟。有兴趣的可以关注一下我的[blog](https://github.com/laihuamin/JS-total/issues)

### 总的知识点概览

语法、数据类型、运算、对象、function、继承、闭包、作用域、原型链、事件、RegExp、JSON、Ajax、DOM、BOM、内存泄漏、跨域、异步加载、模板引擎、前端MVC、前端MVVM、路由、模块化、Http、Canvas、jQuery、EMCAScript、ES6、NodeJS、Vue、React

### 运算符

运算符分类：赋值运算符、比较运算符、算数运算符、位运算符、逻辑运算符、字符串运算符、条件运算符、逗号运算符、一元运算符、关系运算符

### 赋值运算符

- 简单赋值运算符只有一个`=`。
- 复合赋值运算符：

|名字|简单操作符|
|:---:|:---:|
|加法赋值|x += y|
|减法赋值|x -= y|
|乘法赋值|x *= y|
|除法赋值|x /= y|
|求余赋值|x %= y|
|求幂赋值|x **= y|
|左位移赋值|x <<= y|
|右位移赋值|x >>= y|
|无符号右移位赋值|x >>>= y|
|按位与赋值|x &= y|
|按位异或赋值|x ^= y|
|按位或赋值|x |= y|

- 解构：这是es6中出现的一种更加复杂的赋值运算。

```js
var foo = ["one", "two", "three"];
// 不使用解构
var one   = foo[0];
var two   = foo[1];
var three = foo[2];
// 使用解构
var [one, two, three] = foo;
```

### 比较运算符

|运算符|描述|
|:---:|:---:|
|等于(==)|操作数两边相等返回true|
|不等于(!=)|操作数两边不想等返回true|
|全等(===)|操作睡两边相等且数据类型相同返回true|
|不全等(!==)|于上述相反|
|大于(>)|左边操作数大于右边操作数返回true|
|大于等于(>=)|左边操作数大于等于右边操作数返回true|
|小于(<)|左边操作数小于右边操作数返回true|
|小于等于(<=)|左边操作数小于等于右边操作数返回true|


### 算术运算符
算术运算符除了普通的加减乘除(+-*/)
|运算符|例子|
|:----:|:--:|
|求余(%)|12 % 5 = 2|
|自增(++)|var a = 3;a++;console.log(a);//4|
|自减(--)|var a =3;a--;console.log(a);//2|
|一元负值符(-)|var a = 3; console.log(-a);//-3|
|一元正值符(+)|var a = '3'; console.log(+a);//3|
|指数运算符(**)|2 ** 3 = 8|

### 位运算符

|符号|使用|描述|
|:--:|:--:|:--:|
|与|`a & b`|在a和b的二进制表示中，每位都是1的时候才返回1|
|或|`a | b`|在a和b的二进制表示中，只要有一位为1就可以返回1|
|异或|`a ^ b`|在a和b的二进制表示中，只要a和b的相同位不同就返回1|
|非|`~a`|对a的二进制表示，求反|
|左移|`a << b`|把a的二进制串向左移b位，右边移入0|
|右移|`a >> b`|把a的二进制串向右移b位，左边移入0|
|无符号右移|`a >>> b`|把a的二进制表示向右移动b位，丢弃被移出的所有位，并把左边空出的位都填充为0|


### 逻辑运算符

我们先介绍一下有三个逻辑运算符，然后讲几个运用技巧

|运算符|范例|描述|
|:--:|:--:|:----:|
|与|`a && b`|a和b全为true的时候返回true|
|或|`a || b`|a和b有一个为true，就返回true|
|非|`!a`|如果a为true。那么返回false|

- 短路操作

`false` && anything  //返回false
`true` || anything //返回true
`true` && anything //anything
`false` || anything //anything`

### 条件运算符

> 条件 ？ 值1 : 值2

例如：

`var status = (age >= 18) ? "adult" : "minor";`

这样会比if-else简便的多。