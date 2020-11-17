

#### 箭头函数：一种定义函数的方式

```javascript
1、 const aaa = function(){}
2、对象字面量中
const obj = { bbb(){}}
3、Es6中的箭头函数
const ccc = () =>{}
```

```javascript
参数问题
放入两个参数
const sum =(num1,num2) => {
    return num1 + num2
}
放入一个参数(小括号省略)
const power = num => {
    return num*num
}
函数代码块中只有一行代码
const mul = (num1,num2) => num1 * num2
```

```javascript
this使用
箭头函数中的this引用的是最近作用域中的this
this如何查找
向外层作用域中，一层层查找this，直到有this的定义
谁调用指向谁
```

#### 深拷贝与浅拷贝

```javascript
赋值 
基本数据类型(boolean number string undefind null) 赋值两个变量互不干扰
引用数据类型(object symbol ) 赋址仅改变引用的指针，指向同一个对象，所以相互之间有影响

根据拷贝的层次不同分为浅拷贝和深拷贝
浅拷贝:重新在堆中创建内存、拷贝后对象的基本数据类型互不影响、只拷贝一层、不能对对象中的子对象进行拷贝，改变其中一个对象，另一个对象也会发生改变
深拷贝:对对象中的子对象进行递归拷贝、拷贝前后的两个对象互不影响
```

##### 浅拷贝的实现方式

```javascript
1、Object.assign()
let clone_demo = Object.assign({},demo)
2、展开运算符(...)
let clone_demo = {...demo}
3、Array.prototype.slice()
slice方法返回一个新的数组对象 这一对象由begin和end决定的原数组的浅拷贝、原始数组不会改变
```

##### 深拷贝的实现方式

```javascript
深拷贝会拷贝所有的属性，并拷贝属性指向的动态内存的内存。
当对象和它引用的对象一起拷贝时即发生深拷贝，深拷贝相比于浅拷贝速度较慢并且花销较大，拷贝前后两个对象互不影响
JSON.parse(JSON.stringify(obj))
深拷贝会忽略undefined Symbol、不能序列化函数、不能解决循环引用的对象、不能正确处理new Date()、不能处理正则
jQuery.extend和lodash.cloneDeep也可以实现深拷贝

```

#### 路由vue-router及其映射关系

```javascript
路由器：路由和传送
路由决定了数据包从来源到目的地的路径
转送将输入端的数据转移到合适的输出端
IP地址必须是唯一的
```

```javascript
前端渲染和后端渲染
1、后端渲染 jsp（java server page）
2、前端渲染 浏览器中显示的网页中的大部分内容都是由前端写的js代码在浏览器中执行，最终渲染出来的网页
```

#### 前端性能优化

```javascript
站在用户视角的主观的可感知的性能
站在开发者视角的可客观度量的性能
```

```javascript
1、减少请求次数
2、减小资源大小
3、提高响应和加载速度
4、优化资源加载时机
5、优化加载方式
```

```javascript
构建优化（基于vue/cli）
1、gzip压缩
2、去除console.log
3、去除SourceMap
4、CDN减少打包体积
5、渲染方式：客户端渲染、服务端渲染、预渲染
预渲染：将浏览器解析JavaSCript动态渲染页面的这部分工作，在打包阶段就将它完成。换个说法，webpack通过使用prerender-spa-plugin插件生成静态结构的html。
预渲染模式下的路由模式必须为history，不设置的话每个index.html文件中的内容都会是一样的。
```

```javascript
网络资源优化
1、Service Worker（离线资源缓存）
运行在浏览器后台进程里的一段 JS，它可以做许多事情，比如拦截客户端的请求、向客户端发送消息、向服务器发起请求等等，其中最重要的作用之一就是离线资源缓存。
优点：拥有对缓存流程丰富灵活的控制能力，当页面请求到 ServiceWorker 时，ServiceWorker 同时请求缓存和网络，把缓存的内容直接给用户，而后覆盖缓存。
注：需要HTTPS才可以使用ServiceWorker
2、HTTP缓存
普通刷新会启用协商缓存，忽略强缓存。
只有在地址栏或收藏夹输入网址、通过链接引用资源等情况下，浏览器才会启用 强缓存。
（1）强缓存（本地缓存）（200）
最快速的一种缓存方式，只要资源还在缓存有效期内，浏览器就会直接在本地请求，不会请求服务端。
（2）协商缓存（304缓存）
经过浏览器与服务器之间协商过之后，在决定是否读取本地缓存，如果服务器通知浏览器可以读取本地缓存，会返回304状态码，并且协商过程很简单，只会发送头信息，不会发送响应体。
（3）缓存位置
缓存位置一般分为：Memory Cache（内存缓存）和 Disk Cache（硬盘缓存）
内存缓存：读取快、持续时间短、容量小。
硬盘缓存：读取慢、持续时间长、容量大。
（4）缓存优先级
Service Worker -> Memory Cache -> Disk Cache -> Push Cache（推送缓存）
3、HTTP2（前提必须是https）
（1）多路复用，无需多个TCP连接，因为其允许在单一的HTTP2连接上发起多重请求，因此可以不用依赖建立多个TCP连接。
（2）二进制分帧，将所有要传输的消息采用二进制编码，并且会将信息分割为更小的消息块。（3）头部压缩，用HPACK技术压缩头部，减小报文大小
（4）服务端推送，服务端可以在客户端发起请求前发送数据，换句话说，服务端可以对客户端的一个请求发送多个相应，并且资源可以正常缓存。
4、资源预加载：提前加载资源，当用户需要查看时可直接从本地缓存中渲染
（1）preload(对当前页面进行预加载)
在页面加载的过程中，在浏览器开始主体渲染之前加载
（2）prefetch（除当前页面之外的预加载）
页面加载完成后，利用空闲时间提前加载。
注：vue-cli默认开启prefetch，在vue.config.js中全局禁用prefetch，再针对指定模块开启。
（3）dns-prefetch:页面加载完成后，利用空闲时间提前加载。
5、异步无阻塞加载JS：异步加载js文件，并且不会阻塞页面的渲染
（1）普通的script标签解析过程
<script src="a.js"> script
停止解析document
请求a.js
执行a.js中的脚本
继续解析document
（2）defer
<script src="b.js" defer> script
<script src="c.js" defer> script
不阻止解析document，并行下载b.js,c.js
即使下载完b.js,c.js,仍继续解析document
按照页面中出现的顺序在其他同步脚本执行后，DOMContentLoaded事件前依次执行b.js,c.js
（3）async
<script src="d.js" async> script
<script src="e.js" async> script
不阻止解析document，并行下载d.js,e.js
当脚本下载完后执行（两者执行顺序不确定，执行阶段也不确定，可能在DOMContentLoaded事件前或者后）
6、webp
一种新的图片格式，它的体积只有JPEG 的2/3，将图片资源大量换成 webp 格式可以加快请求的速度。
注：webp格式在浏览器兼容上还有一定的问题，所以需要判断浏览器是否支持webp格式哦。
```

```javascript
感知性能优化
1、loading加载
2、骨架屏（ele中没有提供，antd中使用）
```

```javascript
jsp java serve page
java从数据库中读取数据，并且将它动态的放在页面中

后端路由阶段
前后端分离阶段 后端只负责提供数据，不负责其他内容 前端渲染
前端路由阶段 SPA 单页面富应用
```

![](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200623182317763.png)

￼<img src="C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200623182349573.png" style="zoom:200%;" />

![](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200623183913955.png)

```javascript
JSON.stringify()与JSON.parse()
1、 JSON.stringify(): 把JavaScript对象序列为JSON字符串
    JSON.parse(): 把JSON字符串解析为原生JavaScript对象
2、 JSON.stringify()
    语法：JSOn.stringify(value[,replace[,space]])
    value：将要序列化为JSON字符串的值
    replacer：可选|过滤器参数。（参数可能为数组，函数或null）数组：只有包含在这个数组中的属性名，才会显示；函数：传入的函数接收两个参数，属性名和属性值；没有提供/null：则不过滤，属性全部显示；
    space：可选|控制结果中的缩进和空白符。用于美化输出。（参数可能为数字、字符串、没有提供或为null）数字：上线为10，大于10则转换为10，小于1则没有空格；字符串：字符串长度最长不超过10个，大于10则取前10，替代空格显示；没有提供/null：没有空格；
3、 JSON.parse()
    语法：JSON.parse(text[,reviver])
    text：要被解析为JavaScript对象的字符串
    reviver：可选|函数，将在每个键值对上调用，用来修改解析生成的原始值，在parse返回之前调用。
    注：若传入的字符串不符合JSON规范，则会抛出SyntaxError异常；
       不允许对解析的原JavaScript对象出现以逗号结尾
4、 兼容性 caniuse.com
```

#### Chrome浏览器调试(devtools)

```javascript
1、元素面板 elements
自由的操作DOM和CSS来迭代布局和设计页面
检查和调整页面，编辑样式，编辑DOM
2、控制台面板 console
记录诊断信息，命令行交互
3、源代码面板 sources
断点调试
调试混淆的代码
使用开发者工具的Workspaces进行持久化保存
4、网络面板 NetWork
使用网络面板了解请求和下载的资源并优化网页加载性能
网络带宽基础
了解资源时间轴
网络带宽限制
5、性能面板 Performance
可以通过记录和查看网站生命周期内发生的各种事件来提高页面的运行性能
6、内存面板 memory
JavaScript CPU分析器
内存堆去分析器
7、应用面板 Application
使用资源面板检查加载的所有资源，包括IndexDB与Web SQL数据库，Local storage Session Storage cookie
应用程序缓存 图像 字体 样式表
8、 安全面板 Security
调试混合内容问题，证书问题
```

```javas
copying & saving
copy():通过全局copy() console里copy任何你能拿到的资源
Store as global(存储为一个全局变量)，对数据进行一些额外的操作而不用担心影响到他们原来的值
Stack trace(保存堆栈信息)
直接Copy HTML
```

```javascript
快捷键和通用技巧
1、切换DevTools窗口的展示布局
Ctrl+shift+D
2、切换DevTools的面板
Ctrl+[ :向左切换 Ctrl+] : 向右切换
按下 ctrl + 1 到 ``ctrl + 9可以直接转到编号1...9的面板
3、递增或递减
通过使用带有或者不带有修饰键的上 / 下箭头按键，你可以实现递增和递减 0.1 ，1或者10这样数值类型的值。
4、elements logs source & network中的查找
```

```javascript
Command
截图：节点截图 --？，Cpature full size screeshot
快速切换面板 ； 输入layout
快速切换主题 ： theme
代码块
Snippets:：它允许你存放 JavaScript 代码到 DevTools 中，方便你复用这些 JavaScript 代码块
```

```javascript
Console

1、$(jquery的选择器)
$0 对当前选中的html节点的引用 $1是对上一次我们选择的节点的引用 类推
$---->document.querySelector的别名
$$---->Array.from(document.querySelectAll)
$_---->对上次执行结果的引用
$i---->>在控制台安装npm包

2、异步的console
与浏览器相关的API都是基于Promise的，使用Promise的时候通常配套用.then(处理方法)或者将promise包裹在async方法中，再使用await来接收结果
console默认被async包裹，直接使用await方法
await navigator.storage.estimate():查看storage系统的占用数和空闲数
console.table(await navigator.getBattery()):查看设备的电池信息
console.table(await navigator.mediaCapablities.decodingInfo(query)):媒体能力
Cache storage keys一般对request和response进行缓存

3、Ninja console.log(忍者打印)
(1)条件断点:Conditional breakpoints
add conditional breakpoint 添加条件断点
edit breakpoint 编辑断点
输入条件

(2)The ninja 忍者 console.log
每一个条件都必须经过判断 - 当应用执行到这一行的时候进行判断
并且如果条件返回的是 falsy 的值(这里的 falsy并非是笔误，falsy 指的是被判定为 false 的值，例如 undefined )，它并不会暂停.

3、自定义格式转换器
常用console默认对object的转换
自定义:Custom Formatter---->header hasbody body
header:处理如何展示在console的日志中的主要部分
hasbody:如果显示一个用来展开对象的箭头，返回true
body:定义将会被显示在展开部分的内容中

4、对象&方法
(1)queryObjects(对象查询)方法
(2)monitor(镜像)方法
它能够让你 “潜入” 到任何 _function calls(方法的调用) 中：每当一个 被潜入 的方法运行的时候，console 控制台 会把它的实例打印出来，包含 函数名 以及 调用它的参数 。(监听函数)
(3)monitorEvents(镜像事件)方法
```

```javascript
自定义格式化应用
window.devtoolsFormatters = [{
    header: function(obj){
      if (!obj.__clown) {
        return null;
      }
      delete obj.__clown;
      const style = `
        color: red;
        border: dotted 2px gray;
        border-radius: 4px;
        padding: 5px;
      `
      const content = `🤡 ${JSON.stringify(obj, null, 2)}`;

      try {
        return ['div', {style}, content]
      } catch (err) { // for circular structures
        return null;  // use the default formatter
      }
    },
    hasBody: function(){
        return false;
    }
}]

console.clown = function (obj) {
  console.log({...obj, __clown: true});
}

console.log({message: 'hello!'});   // normal log
console.clown({message: 'hello!'}); // a silly log
```

```javascript
console一些操作
(1)console.assert
当我们传入的第一个参数为假时，console.assert打印跟在这个参数后面的值
摆脱if表达式，还可以获得堆栈信息
(2)console.table:将数据打印为表格形式
   console.table{}
(3)console.dir 查看这个节点所关联到的真实的JS对象以及相关属性
(4)console.time():开启一个计时器
   console.timeEnd():一结束计时并且将结果在console中打印出来
(5)给console.log加上CSS样式:加上%C
```

```javascript
Network
1、request initiator: 显示了调用堆栈信息，显示那个脚本的哪一行触发了请求，显示了在调用堆栈中触发请求的最后一步
2、请求过滤:过滤输入框接受字符串或正则表达式，对应显示匹配的请求。显示所有可能的关键字，在空白的输入框按下Ctrl+space
3、自定义请求表
   重新发送XHR的请求 Replay XHR
   XHR/fetch断点 
```

```javascript
elements 元素面板 
'h'隐藏元素面板中选择的元素，去掉里面的敏感信息、
   拖动&放置信息
   Ctrl移动元素
```

