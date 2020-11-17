```
1、 $attrs   $listeners 二次包装组件
```

```javascript
2 监听组件的生命周期 hook event
（1）内部监听生命周期函数
export default{
    mounted(){
        this.chart = echarts.init(this.$el)
        // 监听窗口发生变化 resize组件
        window.removeEventListener('resize', this.$_handleResizeChart)
        // 通过hook监听组件销毁钩子函数 并取消监听事件
        this.$once('hook:beforeDestroy', () => {
            window.removeEventListener('resize', this.$_handleResizeChart)
        })
    },
    methods: {
        $_handleResizeChart(){
            
        }
    }
}
（2）外部监听生命周期函数
<template>
    <custom-select @hook:updated="$_handleSelectUpdated"/>
</template>
<script>
     import CustomSelect from "./"
     export default{
         components: {
             CustomSelect
         },
         methods: {
             $_handleSelectUpdated(){
                 console.log('custom-select组件的update钩子函数被触发')
             }
         }
     }
</script>
```

```javascript
3、如何实现防抖和节流
防抖 debounce: 防止抖动 单位时间内事件触发会被重置 以免把一次事件误认为多次 防抖重在清零 clearTimeout
节流 throttle: 控制时间发生的频率 单位时间内只能发生一次 节流重在开关锁 timer=timeout timer=null
```

```java
4、dispatch broadcast
(1) $dispatch: $dispatch会向上触发一个事件，同时传递要触发的祖先组件的名称与参数，当事件向上传递到对应的组件上会触发组件上的事件侦听器，同时传播会停止
(2)$broadcast: $bradcast会向所有的后代组件传播一个事件，同时传递要触发的后代组件的名称和参数，当事件传递到对应的后代组件时，会触发组件上的事件侦听器，同时传播会停止（因为向下传递是树形的，所以只会停止其中一个叶子分支的传递）
```

```javascript
5、函数式组件
函数式组件没有内部状态、没有生命周期函数、没有this(不需要实例化的组件)，用于开发一些纯展示性的业务组件、只需要将外部传入的数据进行展现
函数式组件不需要实例化、无状态、没有生命周期、所以渲染性能要好于普通组件、结构比较简单、代码结构更清晰

与普通组件的区别
函数式组件需要在声明组件时指定functional
函数式组件不需要实例化，所以没有this，this通过render函数的第二个参数来代替（props、slots都在上面挂着）
函数式组件，没有生命周期函数，不能使用computed、watch
函数式组件不能通过$emit对外暴露事件，调用事件通过context.listeners.click的方式调用外部传入的事件
函数式组件没有实例化的，外部通过ref去引用组件时，实际引用的是HTMLElement
函数式组件的props可以不用显示声明，所以没有在props里面声明的属性都会被自动隐式解析为props
```

```
Wat监听
组件创建的时候我们获取一次列表，同事监听input框，每当发生变化的时候重新获取一次筛选后的列表
created() {
  this.fetchPostList()
},
watch: {
  searchInputValue() {
  this.fetchPostList()
}
}
优化
在watchers中，可以直接使用函数的字面量名称，其次，声明immediate.true表示创建组件时立马执行一次
watch：{
  searchInputValue： {
  handler：'fetchPoslist',
  imaager'
}
```

```
组件注册

```



