# 一、Es6

作用域链、继承以及原型链

深拷贝 浅拷贝

















自建Gitlab，分支版本管理，打包发布Jenkins、

埋点系统：记录每个页面的访问量（PV page view UV unique vistor）、捕捉每个功能的使用量、捕捉报错情况、图表化显示、方便给其他部门展示。

安全管理：XSS注入、https  、CSRF

eslint:降低低级bug出现的概率、增加代码的可维护性、硬性统一代码风格

# 二、大前端体系

HTML5：语义化标签、音视频处理（audio、video）、canvas/webGl、history/API、requestAnimationFrame、地理位置（百度、高德）、web socket（实时直播、实时通信）

CSS3：常规、动画、盒子模型、响应式布局

JavaScript:ES 3/5/6/7/8/9、DOM、BOM、设计模式、底层原理-->堆栈内存、闭包作用域 AO/VO/GO/EC/ECSTACK、面向对象OOP、this、eventloop、浏览器渲染原理、回流重绘

网络通信层（前后端分离）：AJAX/Fetch/axios、HTTP1.0/2.0、TCP、跨域处理方案、性能优化

Hybird/APP/小程序：Hybird/uni-app/RN/Fluter/小程序 MPVUE/Weex/PWA

工程化方面：webpack/git/linux nginx\

全栈方面：node/express/koa2/mongodb/nuxt.js next.js

框架方面：                                                                                                                                                                     Angular、                                                                                                                                                                      Vue：基础知识、核心原理、vue-router、vue-cli、vuex、element-ui、vant、cube、SSR、优化               React：基础知识、核心原理、react-router-dom、redux、react-redux、dva、umi、mobix、antd、antd pro、SSR、优化

# 三、CSS

标签语义化：合适的标签做合适的事

行级标签 块级标签 行内块标签  

1、盒子水平垂直居中：

定位（三种）---->margin:auto、transform:translate,margin-left\margin-top

display：flex ---->jusitify-content:center

JavaScript:winW、winH、boxW、boxH

display：table-cell        

2、CSS盒子模型

标准盒子模型 ：box-sizing:content-box

怪异盒子模型---->ie  box-sizing：border-box

flex盒模型    ： main cross flex-item

多列布局：column                                                

3、几大经典布局

圣杯布局

双飞翼布局

左右固定，中间自适应（上下固定）

calc

flex

4、响应式布局：media rem flex vh/vw(百分比)

5、z-index 文档流

# 四、大前端

1、堆栈内存及闭包作用域

JS中的8中数据类型及区别

number/string/undefind/null/boolean/object/function/symbol 

闭包的两大作用：保存/保护

JS编译机制：VO/AO/GO

JS堆栈内存的运行机制

变量提升机制

作用域和作用域链

JS高阶编程技巧：惰性函数/柯理化函数/高阶函数

2、面向对象（OOP）和this处理

单例设计模式

类和实例

原型和原型链

new运算符的实现机制

call/apply/bind

constructor构造函数模式

JS中this五种情况的综合梳理

JS中的四大数据类型检测方案

JS中的四大继承方案（含深浅拷贝）

3、DOM/BOM及事件处理机制

DOM/BOM的核心机制

DOM 2级事件的核心运行机制

事件对象

拖拽及拖拽插件封装

发布订阅设计模式

移动端Touch/Gestrue事件封装处理

浏览器底层渲染机制和DOM的回流重绘

深度剖析JQ源码

事件传播机制和事件代理

Dialog模态框组件的封装

4、ES6/ES7

let/const和var的区别

箭头函数ArrowFunction

解构赋值和扩展运算符

Set/Map数据结构

Promise设计模式

async/await及实现原理

Promise A+规范（手写Promise源码）

JS底层运行机制：单线程和同步异步编程

JS底层运行机制：微任务宏任务和事件循环机制

Generator生成器函数 

Interator迭代器和for of循环

5、AJAX/HTTP前后端数据交互

AJAX核心四步操作

前端开发中的9种跨域方案

GET/POST核心机制与区别

HTTP状态码和实战中的处理方案

TCP三次握手和四次挥手

前端性能优化汇总（强缓存和弱缓存）

axios库和源码剖析

fetch基础和实战应用

6、OA

登录注册的前后端处理方案

存储方案：cookie、webStorage、session

加密策略：encodeURI-component 和MD5等

用户权限和登录态的校验处理

JQ/BootStrap

7、HTML5

响应式布局开发方案 @media/rem/flex

H5音视频处理方案

新表单元素和表单校验

CSS预编译语言：less/sass

8、Canvas Echarts

canvas的基础用法

echarts基础API

canvas动画 小游戏开发

canvas图像处理

多元化/个性化数据图标练习

异步数据的处理和更新、

echarts的事件和行为

9、Hybird

Hybird混合APP开发

swiper/zepto移动端类库

JSBridge通信机制和底层原理

微信JS SDK 

基于Hbuilder实现APP打包

移动端联调处理方案

# 五、JS

堆：存储引用类型值的空间

栈：存储基本类型值和指定代码的环境

symbol：创建唯一值



# 六、电脑相关

B站、百度、知乎、Chiphellws

CPU  

显卡

内存

硬盘

主板



# 七、相关网络理论

### 1、浏览器请求一个网页的流程

```javascript
Client 客户端-->DNS解析-->IP地址-->TCP/IP三次握手、建立TCP连接、发起HTTP请求-->Server服务端
Server服务端: HTML+CSS+JS-->浏览器获得HTML代码-->Client客户端-->解析页面、请求下载HTML中的静态资源-->Server服务端
Client客户端<----四次挥手 中断连接请求 渲染页面---->Server服务端

客户端就是数据的接口
服务端就是存储网页、存储和处理数据的程序，是数据的接口
后台是对数据的管理
服务器就是电脑
```

### 2、URI URL URN

```javascript
(1)URI: Uniform Resource Identifier
统一资源标识符，原来唯一标识一个资源(只是资源标识)
(2)URL: Uniform Resource Locator
统一资源定位符，标识一个资源，用地址定义一个资源
具有定位资源的功能
指明了获取资源采用的协议

http://   linchen.qq.com：80/   index/index.html  ?fr=hmpage
协议名称    主机名称        端口号    路径/文件       查询所需字符

https:默认端口号443 http默认端口号80 服务器MySQL默认3306

(3)URN:Uniform Resource Name
统一资源命名，通过名字定位一个资源(没有协议名称)

URL肯定是一个URI,URI可能是一个URL,也可能是一个URN,URI的子集-->url/urn
```

### 3、客户端与服务端

```javascript
Client Server
(1)云服务器 Elastic Compuute Serve 弹性计算服务ECS
```

![](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200702092419145.png)



```javascript
无需提前购买硬件设备，而是根据业务需要，随即创建所需数量的云服务器ECS实例、扩容键盘、增加带宽(选择多)

地域和可用区: ECS实例所在的物理位置，用户访问网站的速度和服务器部署物理位置有关
实例:等同于一台虚拟机、包含CPU、内存、操作系统、网络、磁盘等最基础的计算组件
实例规格:即实例的配置、包括VCPU参数、内存、网络性能等，实例规格决定了ECS实例的计算和存储能力
镜像: 是指ECS实例运行环境的模板、一般包括操作系统和预装的软件。操作系统支持多种Linux发行版本和不同的windows版本
块存储: 包括基于分布式存储架构的云盘和共享快存储，以及基于本地物理机本地硬盘的本地存储。可以像使用物理硬盘一样格式化并建立文件系统来使用块存储，满足大部分通用业务场景下的数据存储需求
快照: 指某一个时间点上一块弹性块存储的数据备份
网络类型:
  专用网络:基于阿里云构建的一个隔离的网络环境，专有网络之间逻辑上彻底隔离
  经典网络:统一部署在阿里云公共基础内，规划和管理由阿里云负责
  安全组:由同一地域内具有相同保护需求并相互信任的实例组成，一种虚拟防火墙，用于设置实例的网络访问控制
  
(2)C/S架构 Client/Serve 需要硬件
  将应用程序安装在客户端电脑中，由服务器提供客户端所需要的数据
优点: 界面操作丰富、安全性高、响应速度快(数据存储在本地)
缺点: 通常用于局域网、需要安装特定应用程序或使用特定硬件、维护成本高(需要安装升级)

(3)B/S架构 Browser/Serve(网页)
利用web浏览器呈现客户端界面、由服务器提供客户端所需要的数据
优点:无需安装特定应用程序或使用特定硬件、多客户性访问、交互性强、无需升级客户端
缺点:跨浏览器兼容性差、功能性相对较弱、设计成本高、安全性弱、功能性弱
```

### 4、域名 Domain Name

```javascript
相当于访问互联网某一户人家的地址
域名与服务器绑定之后，域名和服务器对应的IP是映射关系
域名比IP更方便用户记忆
IP可以对应多个域名、所以不同的域名可以访问一个或多个Web网页

解析域名:将域名与服务器Ip对应的记录、由DNS服务器来完成
```

#### 域名分类

```javascript
(1)通用类
.com:工商金融等企业 ,com.cn公司
.gov:政府机构 .gov.cn
.net:提供互联网网络服务机构 
.org:各类组织机构 
.ac:科研机构 .ac.cn
.edu:教育机构 .edu.cn

国家地区类 cn ca jp kr uk hk tw us

(2)域名级别

一级域名(顶级域名):baidu.com
二级域名: www.baidu.com
三级域名:qianduan.study.tencent.com

根域名服务器:分配管理域名
```

#### DNS解析 Domain Name Server(域名服务器)

```javascript
作用:域名与对应的IP转换的服务器
特征:DNS中保存了一张域名与对影视网Ip地址的表，一个域名对应一个IP地址，一个IP地址可以对应多个域名。、
gTLD:generic Top-Level DNS Server 顶级域名服务器， 为所有.com、.net ……后缀做域名解析的服务器
```

![](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200702102925007.png)

### 5、IP Internet Protocol  Address

```javascript
作用: 分配给用户上网使用的互联网协议
分类: IPv4、IPv6
IPv6优势:IPv6地址空间更大（8组（128位），十六进制）
        路由表更小
        组播支持以及对流支持增强
        对自动配置的支持
        更高的安全性
IP端口号范围:0~65535
```

### 6、TCP UDP HTTP  HTTPS

#### TCP

```javascript
Transmission Control Protocol 传输控制协议
特点:面向连接
建立连接基础:三次握手
应用场景:数据必须准确无误的收发，比如HTTP请求、FTP文件传输、邮件收发
优点:稳定、重传机制、拥塞控制机制、断开连接
缺点:速度慢、效率低、占用资源、容易被攻击(三次握手-->DOS、DDOS攻击)
TCP/IP协议组:提供点对点的连接机制、制定了数据封装、定址、传输、路由、数据接收的标准
```

#### UDP

```javascript
User Data Protocol 用户数据报协议
特点：面向无连接（不可靠的协议，无状态传输机制）->无连接信息发送机制
应用场景：无需确保通讯质量且要求速度快、无需确保信息完整 ->消息收发、语音通话、直播（QQ）
优点：安全、快速、漏洞少（UDP flood攻击）
缺点：不可靠、不稳定、容易丢包
总结：只要目的源地址、端口号、地址、端口号确定，则可以直接发送信息报文，但不能保证一定能收到或收到完整的数据。
```

#### HTTP HTTPS

```javascript
HTTP: HyperText Transfer Protocol 超文本传输协议
定义: 客户端和服务端请求和应答的标准，用于从Web服务器传输超文本到本地浏览器的请求
HTTP请求:按照协议规则先向Web服务器发送的将超文本传输到本地浏览器的请求

HTTPS:Hyper Text Transfer Protocol Secure 超文本传输安全协议(HTTP的安全版)
安全的基础是SSL/TLS
SSL:Secure Sockets Layer 安全套接层
TLS:Transport Layer Security 传输层安全
为网络通信提供安全及数据完整性的一种安全协议 对网络安全进行加密

区别:
1、HTTP是不安全的（监听和中间人攻击等手段，获取网站账户信息和敏感信息）； HTTPS可防止被攻击
2、HTTP协议的传输内容都是明文，直接在TCP连接上运行，客户端和服务器都无法验证对方身份
3、HTTPS协议的传输内容都被SSL/TLS加密，且运行在SSL/TLS上，SSL/TLS运行在TCP连接上，所以数据传输是安全的。
```

#### 三次握手

```javascript
标志位: 数据包
SYN: Synchronize Sequence Numbers 同步序列编号(发送包)
ACK: Acknoeledgement 确认字符

状态
LISTEN:侦听TCP端口的连接请求(我等着你发送请求呢)
SYN-SENT:在发送连接请求后等待匹配的连接请求(我发送了连接请求，等待回复)
SYN-RECEIVED:在收到和发送一个连接请求后等待连接请求的确认(已经收到你的请求，等你回复我)
ESTABLISHED:代表一个打开的连接，数据可以传送给用户(建立建立了，通知)
```

![](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200702143645536.png)



#### HTTP报文

```javascript
HTTP请求是通过请求和响应之间进行数据传输，基于TCP/IP通信协议来传递数据，基于C/S架构模型，是一个无状态的请求/响应协议(没有记忆)
限制每次连接只处理一个请求(传统的TCP/IP)，服务器处理完客户的请求，并收到客户的应答后，断开连接。
只要客户端和服务器知道如何处理的数据内容，任何类型的数据都可以通过HTTP发送，由C/S指定使用合适的MIME-type内容类型 Multipurpose Internet Mail Extensions type 多用途互联网邮件扩展类型

HTTP报文定义：在客户端与服务器之间发送的数据块。这些数据块以一些文本的元信息（meta-information）开头，描述了报文的内容及含义，后面跟着可选的数据部分，这些报文在客户端、服务器和代理之间流动。所以HTTP报文的发送也叫报文流。
每条HTTP报文包含一个客户端请求和服务端响应（请求报文Request和响应报文Response）
```

#### 状态码

```javascript
1xx 信息，服务器收到请求
2xx 成功，操作被成功接收并处理
3xx 重定向，需要进一步的操作以完成请求
4xx 客户端错误，请求包含语法错误或无法完成请求
5xx 服务器错误，服务器在处理请求的过程中发生了错误
```

```javascript
1xx post先把请求头发送给服务器，服务器确认了post的请求头，返回100状态码，然后再发送数据
302 重定向 类似跳转页面，跳转一个页面，在这个页面不会做长时间停留，就会跳转到其他页面
304 重定向 拿资源的时候如果服务器的资源和缓存的资源是一样的，就会跳转到缓存出来的页面去
403 服务器拒绝请求forbidden
404 页面错误
500 服务器发生不可预测的错误
503  server Unavailable
```

#### Accept & Content-Type

```javas
Accept 代表客户端希望接收的数据类型，在请求头里面
q：相对品质因子，权重，它从0到1的范围指定优先顺序，没有指定，质量值默认为“q = 1
Accept: （请求头）
Accept-Language: zh-CN,en-US;q=0.8,en;q=0.6 浏览器支持的语言是简体中文、其次是美国英语、再其次是其他形式的英语
Accept-Encoding: gzip, deflate, br 浏览器可以接受的资源编码格式（压缩格式）现在的服务器返回来的资源一般都会经过压缩，然后再由浏览器解压
Content-Type（响应头）: text/html; charset=UTF-8 （Accept-Charset）返回的资源类型与编码
Content-Language：zh-CN 说明返回资源的语言类型
Content-Encoding: gzip 服务器返回资源的编码格式（压缩格式，优化传输内容的大小
```

#### 浏览器缓存

```javascript
把已请求并返回的Web资源(HTML页面 图片 JS文件 CSS文件 数据等)复制成一个副本存储在浏览器的缓存中
减少网络带宽的消耗、降低服务器压力、减少网络延迟

旧版本 Pragma:no-cache(响应头) :指示浏览器忽略资源缓存副本(不管有没有缓存都不要用，每次访问都需要到服务器中获取)

现版本 Cache-control 缓存控制(响应头)
no-cache：指示浏览器忽略资源缓存副本，强制到服务器获取资源（浏览器依然缓存）
no-store：强制缓存在任何情况下都不要保留任何副本
max-age=31536000：指示缓存副本的有效时长，从请求时间开始到过期时间之间的秒数
public：表明响应可以被任何对象（包括：发送请求的客户端，代理服务器，等等）缓存。
private: 表明响应只能被单个用户缓存，不能作为共享缓存（即代理服务器不能缓存它）。
```

![](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200702152716787.png)



#### Connection：keep-alive

```javascript
HTTP短连接:每次请求一个资源就建立连接，请求完成后连接立马关闭
HTTP长连接:只建立一次连接，多次资源请求都复用该连接，完成后关闭。

不同版本HTTP连接方式
1、早期HTTP1.0:请求都要创建一个TCP/IP连接 短连接
2、后期的HTTP/1.0:在请求头增加 Connection:keep-alive
3、HTTP/1.1:默认开启Connection:keep-alive，关闭Connection:close

conten-length 描述HTTP消息实体的传输长度
get请求:请求头没有content-length 响应头带content-length
post请求:请求头与响应头都带content-length request require
```

#### HTTP协议版本

```javascript
HTTP/0.9 Beta版本
仅支持GET请求方式
仅能请求访问HTML格式的资源（只有文字）

HTTP/1.0
增加POST和HEAD请求方式
支持多种数据格式的请求与访问
支持cache缓存功能
新增状态码、多字符集支持、内容编码等
早期HTTP/1.0不支持keep-alive长连接，只支持串行连接（短连接）
后期HTTP/1.0增加Connection:keep-alive字段（非标准字段），开始支持长连接

HTTP/1.1
增加持久连接（默认开启Connection: keep-alive）
增加管道机制（支持多个请求同时发送）
增加PUT/PATCH/OPTION/DELETE等请求方式
增加Host字段（主机域名）-> 案例: 搜索百度 查看network
增加100状态码（Continue）,支持只发送头信息（post）
增加身份认证机制
支持传送内容的一部分和文件断点续传
新增了24个错误状态码

HTTP/2.0
增加双工模式（客户端同时发送多个请求，服务端同时处理多个请求）
服务器推送（服务器会把客户端需要的资源一起推送到客户端，合适加载静态资源。服务器主动推送，把服务器认为客户端所需要的资源全部推送过去）
头信息压缩机制（每次请求都会带上所有信息发送给服务端【HTTP协议不带状态】，要经过压缩）
二进制协议（头信息与数据体使用二进制进行传输）
多工（先发送已处理好的部分，再响应其他请求，最后再解决没有处理好的部分）
```

#### 关闭TCP连接 四次挥手

![](C:\Users\25771\AppData\Roaming\Typora\typora-user-images\image-20200702160028460.png)

```javascript
FIN:finish 关闭连接
状态:FIN-WAIT-1 	等待远程TCP的连接中断请求，或先前的连接中断请求的确认
    FIN-WAIT-2   从远程TCP等待连接中断请求 
    上面这两个是客户端等服务端
    CLOSE-WAIT 等待从本地用户发来的连接中断请求
    LAST-ACK 等待原来发向远程TCP的连接中断请求的确认(最后一次确认)
    TIME-WAIT 等待足够的时间以确保远程TCP接收到连接中断请求的确认(客户端要等待一段时间)
    CLOSED 没有任何连接状态

```









