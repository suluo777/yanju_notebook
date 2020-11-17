# Vue Route

### 1、router-link

```javascript
<router-link>组件支持用户在具有路由功能的应用中(点击)导航，用来代替写死的<a>标签，通过to属性指定目标地址，默认渲染为带有正确链接的<a>标签，通过配置tag属性生成别的标签。
HTML5中的history和hash模式在router-link中表现行为一致。
在HTML5 history模式下，router-link 会守卫点击事件，让浏览器不再重新加载页面。
当你在HTML5 history模式下使用base选项之后，所有的to属性都不需要写(基路径)了。
```

### 2、v-slot

```javascript
router-link中的一个作用域插槽来暴露底层的定制能力
在使用v-slot API时，需要向router-link传入一个单独的子元素
v-slot="{ href, route, navigate, isActive, isExactActive }"
(1)href：解析后的 URL。将会作为一个 a 元素的 href attribute。
(2)route：解析后的规范化的地址。
(3)navigate：触发导航的函数。会在必要时自动阻止事件，和 router-link 同理。
(4)isActive：如果需要应用激活的 class 则为true。允许应用一个任意的 class。
(5)isExactActive：如果需要应用精确激活的 class 则为 true。允许应用一个任意的 class。
```

### 3、props

#### (1) to

```javascript
表示目标路由的链接 被点击后把to的值传给router.push()/string类型/required
```

#### (2) replace

```javascript
设置replace属性会调用router.replace()而不是router.push(),导航后不会留下history记录
<router-link :to="{ path: '/abc'}" replace></router-link>
boolean/false
```

#### (3) append

```javascript
设置 append 属性后，则在当前 (相对) 路径前添加基路径。例如，我们从 /a 导航到一个相对路径 b，如果没有配置 append，则路径为 /b，如果配了，则为 /a/b. boolean/false
```

#### (4) tag 

```javascript
类型: string
默认值: "a"
有时候想要 <router-link> 渲染成某种标签，例如 <li>。 于是我们使用 tag prop 类指定何种标签，同样它还是会监听点击，触发导航。
<router-link to="/foo" tag="li">foo</router-link>
<!-- 渲染结果 -->
<li>foo</li>
```

#### (5) active-class

```javascript
类型: string
默认值: "router-link-active"
设置链接激活时使用的 CSS 类名。默认值可以通过路由的构造选项 linkActiveClass 来全局配置。
```

### 4、element-ui

```javascript
v-loading:加载 isLoading

```

### 5、Vue-router

```javascript
Url的hash
(1)锚点，本质上是改变window.location的href属性
(2)直接赋值location.hash来改变href，但页面不发生刷新

HTML5的history模式
显示最新改编的
history.back 回退 replaceState pushState go(-1)
back=go(-1)=forwaed
```

```javascript
安装vue-router
导入路由对象，并调用Vue.use(VueRouter)
创建路由实例，并且传入路由映射配置
Vue实例中挂载创建的路由实力
使用vue-router
创建路由组件
配置路由映射：组件和路径映射关系
使用路由：通过<router-link>和<router-view>
    router-link:vue-router中已经内置的组件，相当于a标签
    mode:'hiatory'
    linkActiveClass:'active'
    redirect·
路由代码跳转
<button @click="handleHome">首页</button>
methods:{
  handleHome(){
      this.$router.push('/home')
  }
}
```

```javascript
动态路由跳转
route router（局部路由-->活跃 全局路由）
this.$route.params.abc

嵌套路由

打包
app:当前应用程序开发的所有代码(业务代码)
manifest:为了打包的代码做底层支撑
vendor:提供第三方供应
```

```javascript
懒加载（性能优化第一步）:当打包构建应用时，JavaScript包会变得非常大，影响页面加载，把不同路由对应的组件分割成不同的代码块，当路由访问的时候才加载对应组件。
ES6中，代码分割
component:() => import('../components/Home')
结合Vue的异步组件和Webpack的懒加载
const Home = resolve => {require.ensure(['../components/Home.vue'],()=>{resolve(require(['../components/About.vue'],resolve))})}
AMD写法
const About = resolve => require(['../components/About.vue'],resolve);
```

```javascript
传递参数的方式 params query
1、params
配置路由格式: /router/:id
传递方式: 在path后面跟上对应的值
传递后形成的路径:/router/123，/router/abc
2、query（数据多）
配置路由格式:/router 普通配置
传递方式: 对象中使用query的key作为传递方式
传递后的路径: /router?id=123
 
```

```javascript
手写async await
function asyncToGenerator(generatorFunc){
    // 返回的是一个新的函数
  return function(){
      // 先调用generator函数 生成迭代器
      // 对应 var gen = testG()
      const gen = generatorFunc.apply(this,arguments)
      // 返回一个promise 因为外部是用.then的方式 或者await的方式去使用这个函数的返回值
      // key 有 next和throw两种取值，分别对应了gen的next和throw方法
      // arg参数则是用来把promise resolve 出来的值交给下一个yield
      return new Promise((resolve,reject) => {
          function step(key,arg){
              let generatorResult 
              // 这个方法需要包裹在try catch中
              // 如果报错了 就把promise给reject掉 外部通过.catch可以获取到错误
              try{
                  generatorResult = gen[key](arg "key")
              }catch(error){
                  return reject(error)
              }
              // gen.next()得到的是一个{value,done}的结构
              const(value,done) = generatorResult
              if(done){
                  // 如果已经完成了 就直接resolve这个promise
                  // 这个done是在最后一次调用next后才会变为true
                  // 以文本的例子来说 此时的结果是{done:true,value:'success'}
                  // 这个value也就是generator函数最后的返回值
                  return resolve(value)
              }else{
                  // 除了最后结束的时候外，每次调用gen.next()
                  // 其实是返回{value:Promise,done:false}
                  // 这里要注意的是promise.resolve可以接受一个promise为参数
                  // 并且这个promise参数被resolve的时候，这个then才会被调用
                  return Promise.resolve(value
                                        
                                        ).then(val => step('next',val),err => step('throw',err))
              }
          }
          step("next")
      })
  }
}
```

```javascript
导航守卫 全局守卫
前置守卫 后置导航、

keep-alive:Vue内置的一个组件，可以使被包含的路由保持，避免重新渲染 activated deacivated
生命周期 
beforeCreate created 
beforeMount mounted
beforeUpdate updated
beforeDestroy destroyed
```

#### Promise

```javascript
promise是异步编程的一种解决方案,一般情况下有异步操作时，使用promise对异步操作进行封装
new -->构造函数(保存了一些状态信息，执行传入的函数)
执行传入的回调函数时，会传入两个参数，resolve(接受)、reject(拒绝)本身又是函数
网络请求 
// 参数--> 函数
new Promise((resolve, reject)=> {
    SetTimeout(() =>{
        resolve()
    console.log("hello world")
},1000)
}).then(()=> {    
}).catch(error){
}

promise的3种状态 async(异步)

```



