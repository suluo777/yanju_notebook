一般情况vue推荐使用template模板、有时候需要更灵活的做一些功能，这时需要使用JSX

```javascript
JSX = JavaScript + XML 具备JavaScript的灵活性和HTML的语义化

应用场景
在消息框内添加HTMl
Message.alert({
    message:<div>确定要删除<span style="color:red">学习vue</span>笔记</div>,
    type:'warning'
})

函数式组件
export default{
    // 通过配置functional属性指定组件为函数式组件
    functional:true,
    render(h, context){
        const {props} = context
        if(props.avatar){
            return <img src={props.avatar}></img>
        }
        return <img src="default-avatar.png"></img>
    }
}

一个表单的需求
```

```javascript
createElement 增加一个元素
函数返回的值称之为虚拟节点 VNode
VNode扎堆组成的树就是虚拟dom

createElement{
    // {String| Object | Function}
    // 一个HTML签名 、组件选项对象、resolve了上述任何一种的一个async函数，必选
    'div',
    // {Object} 一个与模板中atrribute对应的数据对象、可选    
     {
        
    },
    [
        '先写一些文字',
        createElement('h1', '一则头条'),
        createElement(MyComponent,{
            props: {
                someProp: 'foobar'
            }
        })
    ]
}
```

```javascript
createElement用于实现组件太过于冗余复杂，使用JSX代替createElement简化整个代码的逻辑

methods: {
    $_handleInputUser(value){
        this.formInline.user = value
    },
    $_handleChangeRegion(value){
        this.formInline.region = value
    },
    $_handleSubmit(){}
},
    // 将h作为createElement的别名是Vue中一个通用惯例
    // const h = this.$createElement
render(h){
    return(
      <ElForm inline model={this.formInline} class="demo-form-inline">
         <ElFormItem label="审批人">
            <ElInput value={this.formInline.user} onInput={this.$_handleInputUser}
            placeholder="审批人"></ElInput>    
         </ElFormItem>  
         <ElFormItem label="活动区域">
             <ElSelect value={this.formInline.region}
                       onChange={this.$_handleChangeRegion} 
                       placeholder="活动区域"
              >
                    <ElOption label="区域一" value="shanghai"></ElOption>
                    <ElOption label="区域二" value="beijing"></ElOption>
             </ElSelect>    
         </ElFormItem>
         <ElFormItem >
            <ElButton type="primary" onClick={this.$_handleSubmit}>查询</ElButton>    
         </ElFormItem> 
      </ElForm>
    )
}
```

```java
JSX中指令的用法
    vue-cli4版本支持使用v-model <input v-model={this.value}> 安装插件babel-plugin-jsx-v-model
    v-for 使用for循环 array.map来代替 
    v-if  使用if语句，三元表达式来代替
    v-bind <input value={this.name}></input>
    v-html domPropsInnerHTML
    v-text domPropsInnerText
    
监听事件 on-->naiveOn
        
事件修饰符
     .stop-->event.stopPropagation() 阻止事件冒泡
     .prevent event.preventDefault() 阻止默认行为
     .self-->if(event.target != event.currentTarget){return} 只当事件是从侦听器绑定的元素触发时才触发回调
     .enter与keyCode 特定键触发时才触发回调 if(event.keyCode === 13){}
     .once .capture .passive .capture.once
```

```javascript
插槽就是子组件提供给父组件的一个占位符 默认插槽 具名插槽 作用域插槽
```

