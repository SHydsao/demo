null是JavaScript语言的关键字，它表示一个特殊值，常用来描述“空值”。对null执行typeof预算，结果返回字符串"object"，也就是说，可以将null认为是一个特殊的对象值，含义是“非对象”。但实际上，通常认为null是它自有类型的唯一一个成员，它可以表示数字、字符串和对象是“无值”的。大多数编程语言和JavaScript一样含有null：你可能对null或nil很眼熟。

```js
  var res = null;

  document.write(typeof (res));//object
```

JavaScript还有第二个值来表示值的空缺。用未定义的值表示更深层次的“空值”。它是变量的一种取值，表明变量没有初始化，

1. 如果要查询对象属性或数组元素的值时返回undefined则说明这个属性或元素不存在。
2. <font color="red">如果函数没有返回任何值，则返回undefined</font>。
3. 引用没有提供实参的函数形参的值也只会得到undefined。

undefined是预定义的全局变量（它和null不一样，它不是关键字），它的值就是“<font color="red">未定义</font>”。在ECMAScript 3中，undefined是可读/写的变量，可以给它赋任意值。这个错误在ECMAScript 5中做了修正，undefined在该版本中是只读的。如果使用typeof运算符得到undefined的类型，则返回"undefined"，表明这个值是这个类型的唯一成员。

<font color="red">尽管null和undefined是不同的，但它们都表示“值的空缺”，两者往往可以互换。判断相等运算符“==”认为两者是相等的（要使用严格相等运算符“===”来区分它们）</font>

```js
 var res = null;

  var res1;

  document.write(res == res1); //true

  document.write(res === res1); //false

  // document.write(typeof (res));//object
```

在希望值是布尔类型的地方它们的值都是假值，和false类似。<font color="red">null和undefined都不包含任何属性和方法</font>。实际上，使用“.”和“[]”来存取这两个值的成员或方法都会产生一个类型错误。你或许认为undefined是表示系统级的、出乎意料的或类似错误的值的空缺，而null是表示程序级的、正常的或在意料之中的值的空缺。<font color="red">如果你想将它们赋值给变量或者属性，或将它们作为参数传入函数，最佳选择是使用null</font>。