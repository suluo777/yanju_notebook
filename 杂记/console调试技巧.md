`console.log`

`console.info `:和`console.log` 的作用是几乎完全一样的，也是在控制台中打印信息，只不过打印时的样式可能与 `console.log` 略有区别。

`console.error`:和`console.log`的作用几乎一样，会将打印的内容通过显示的红色标注出来并前面带一个×，便于快捷找到

`console.warn`:通过黄色感叹号来高亮打印信息

`console.time`和`console.timeEnd`结合一起使用，接收一个相同的参数，输出两句表达式中间的代码的执行时间

![image-20201106102212631](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20201106102212631.png)

`console.count`:打印当前的打印内容，并在后面跟上该内容的打印次数

`console.table`:将复合数据类型（对象、数组等）在控制台中以表格形式打印输出，并且你可以将对象数组嵌套乃至结合使用，他都能将其解析为表格形式

`console.group/console.groupCollapsed`和`console.groupEnd`:两者结合使用，他们用于将打印的信息分组，可以将信息折叠和展开

`console.trace`:追溯你的逻辑执行过程

`console.assert`:法接受两个参数，第一个参数是表达式，第二个参数是字符串。只有当第一个参数为false，才会输出第二个参数（并且以error提示的形式输出）。

`console.clear`:清空控制台所有打印内容，并将内容返回第一行

给console的内容设置style

`console.dix`()\ `console.dixml()`

