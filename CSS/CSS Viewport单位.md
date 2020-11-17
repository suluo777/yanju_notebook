# CSS Viewport

```javascript
为开发者提供了一种不需要使用JS就能以动态的方式调整大小的方法
```

```javascript
视口百分比单位相对于初始包含块的大小，它是Web页面的根元素
视口单位为vw、vh、vmin、vmin
vw单位表示根元素宽度的百分比，1vw等于视口宽度的1%，vh表示高度，同理
vmin表示视口的宽度和高度的较小值，也就是vw和vh中较小的那一个，vw>vh-->vmin=vh
vmax表示视口的宽度和高度的较大值，vw>vh=vmax=vw
视口单位基于页面的根元素、百分比则基于它们所在的容器

calc()函数用于动态计算长度值 width: calc(20px + 2vw)
```

```javascript
全屏
section来获取100%的视口高度 height:100vh

粘性布局
footer没有粘在底部
给内容(content)一个高度 content= 视口高度-(header + footer)
(1)header和width高度确定 height: calc(100vh - header - height)
(2)flexbox和视口单位
min-height: 100vh;display:flex;flex-column
flex-grow: 1
```

```javascript
通过使用CSS网格和视口单位，可以做到移动端和PC端完全动态的响应式
视口单位也可以用于grid-(网格)属性 也用于border、border-radius属性

用视口单位来表示元素之间的间距，可以与margin、top、bottom、grid-gap等值一起使用，使用时，间距将基于宽度或高度，用于布局动态性
```



