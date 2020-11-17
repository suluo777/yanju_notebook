​          TypeScript是一种由微软开发的自由和开源的编程语言，是JavaScript的一个超集，而且本质上向这个语言添加了可选的静态类型和基于类的面向对象编程。

![image-20200915112510146](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200915112510146.png)

![image-20200915112549186](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200915112549186.png)

工作流程 ts--编译-->js--打包-->main.js--部署-->main.js

# 一、TS类型

1、Boolean、Number、String、Symbol、Array

2、Enum 类型（枚举类型）

使用枚举可以定义一些带名字得常量，清晰地表达意图或创建一组有区别的用例，ts支持数字的和基于字符串的枚举

数字枚举

字符串枚举

常量枚举

异构枚举

3、Any类型 unKnown 类型

ts中任何类型都可以被归为any类型，这让any类型成为了类型系统的顶级类型，本质上市类型系统的一个逃逸舱，允许对any类型的值执行任何操作，而无需事先执行任何形式的检查

unknown是ts类型系统的另一种顶级类型，只能被赋值给any类型和unknown类型本身

4、Tuple类型

