

1、方法参数验证、验证方法参数为空

```javas
const isRequired = () => {
  throw new Error('params is required')
}
const print = (num = isRequired()) => {
  console.log(`printing ${num}`)
}
print(2) // printing 2
print()  // error
print(null) // printing null
```

2、格式化JSON代码

```javascript
JSON.stringify
stringify方法有3个参数 value replacer space
后两个为可选参数，要缩进JSON,必须使用space参数
console.log(JSON.stringify({name:"John",Age:23},null,'\t'));
```

3、从数组中获取唯一的值(filter set)

```javascript
let uniqueArray = [
  ...new Set([
    1,
    2,
    3,
    3,
    3,
    "school",
    "school",
    "ball",
    false,
    false,
    true,
    true
  ])
];
```

4、数组中删除虚值

js中的虚值：undefined、null、NaN、0、``空字符、false

filter(boolen)

5、合并多个对象

```javascript
const summary = {...user, ...college, ...skills}
```

6、等待Promises

```javascript
在某些情况下，需要等待多个Promise结束，使用Promise.all,关于Promise.all需要注意的一件事是，当一个Promise拒绝时，该方法将引发错误。 这意味着我们的代码将不会等到所有的Promise都完成。如果想要等到所有Promise都完成后，无论它们被拒绝还是成功，可以使用Promise.allSettled.




```





