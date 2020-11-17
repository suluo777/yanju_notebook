```javascript
Es6
let const 有块级作用域
class(类)
arrow function 箭头函数
函数参数默认值 function parameter defaults 定义初始值
模板字符串 template string 拼接字符串
解构赋值 destructuring assignment 将属性/值从对象/数组中取出，赋值给其他变量
模块化 module
扩展运算符 spread operator 将表达式展开
对象属性简写 object attribute shorthand
Promise 三种状态 pending(等待中)/resolved(完成了)/rejected(拒绝了)
        这个承诺一旦从等待状态变成其他状态就永远不能更改状态了
for...of 在可迭代对象(array map set string)上创建一个迭代循环，调用自定义迭代钩子，并为每个不同属性的值执行语句
symbol 基本数据类型 具有静态属性和静态方法

迭代器(Iterator)/生成器(Generator)
iterator是一种迭代的机制，为各种不同的数据结构提供统一的访问机制，任何数据结构只要内部有iterator接口，就可以完成依次迭代操作，一旦创建，迭代器对象可以通过重复调用next()显示的迭代，从而获取该对象每一级的值。
生成器函数允许你定义一个包含自有迭代算法的函数，同时它可以自动维护自己的状态，使用function语法编写，根据需要多次调用该函数，每次都返回一个新的generator，每个generator只能迭代一次

Set/WeakSet
set对象允许你存储任何类型的唯一值，无论是原始值或者是对象引用，set实现数组去重
WeakSet结构与Set类似，区别有以下两点

```



```javascript
1、ES6 
Map:数据结构，类似于对象，也是键值对的集合，
Object:对象只接受字符串作为键名
Object提供了"字符串--值"的对应，Map结构提供了"值-值"的对应，是一种更完善的Hash结构实现

2、ES7
比ES6增加了求幂运算符(**)、Array.prototype.includes()方法、函数作用域中严格模式的变更

3、ES8
async await异步解决方案
ES8提供了新的字符串填充方法，该方法可以使得字符串达到固定长度。它有两个参数，字符串目标长度和填充内容。

4、ES10
Array的flat()方法和flatMap()
(1)flat()方法会按照一个可指定的深度递归遍历数组，并将所有元素与遍历到的元素合并为一个新数组返回
flat最基本的作用就是数组降维
还可以利用flat()方法的特性来去除数组的空项
```

