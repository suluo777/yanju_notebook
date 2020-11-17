# display：grid

```javascript
grid布局与flex布局有一定的相似之处，是对flex布局的一个补充

将网页划分为一个个区域，并且可以对这个区域进行任意组合，以达到布局的效果

flex更像是一种线性的布局，根据横轴和纵轴的各种配置来达到布局的效果。
grid则是一种二维布局，利用row(行) column(列) 来分割出不同的二维区域，用过对这些二维区域的一切进行操作来实现不同的布局，grid更适用于一些多行多列、宽高不等的复杂布局
```

```javascript
容器(container) 所有项目(item)的直接父元素 class="container"
项目(item) container的直接子元素
线(line)
路径(track)
单元格(cell)
区域(area)
```

```javascript
container属性
display display:grid||inline-grid(把这个容器的元素变成一个内联元素)
grid-template-columns/gird-template-rows
grid-template-areas
grid-column-gap/grid-row-gap 间距

justify-items 行轴上设置item们在各自area中的对齐方式 
{start 左侧对齐 end 右侧对齐 center 水平居中对齐 stretch 填满单元格的宽度}
align-items 在列轴上设置items们在各自area中的对齐方式(与justify效果一样，水平变为垂直)

place-items:align-item和justify-items的合并写法 第一个值设置给align-items，第二个值给justify-items,只设置第一个值则这个值同时赋予align-items 和justify-items

justify-content align-content place-content(align和justify的合并写法)
{start：左侧对齐 end：右侧对齐 center：水平居中对齐 stretch：允许该网格填充满整个网格容器的宽度
space-around：左右两端放置一半的空间 space-between：左右两端没有空间 space-evenly：左右两端放置一个均匀的空间}

grid-auto-columns/grid-auto-rows 自动生成的track的高度/宽度
grid-auto-flow
```

```javascript
项目(item)属性
grid-column-start / grid-column-end / grid-row-start 
grid-row-end/grid-column / grid-row  
定线(lines) 来确定item在网格内的位置。

grid-area
justify-self/align-self/place-self
```

