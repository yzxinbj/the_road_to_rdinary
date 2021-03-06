# flex
```
使用flex布局脑子里先想好要怎样排列，是单行还是多行，是单列还是多列
然后即可设置好主轴方向，一般的布局使用容器的属性即可完成简单布局
如果满足不了再设置 item 上的属性即可
```
## 主轴
flex-direction 定义主轴的方向是水平还是垂直

## 交叉轴
垂直于主轴的轴

## 对齐方式
```
flex-start | flex-end | center | baseline | space-between | space-around | stretch;
相同的对齐方式在不同的排列下表达不同的含义
例如：水平排列（flex-direction: row）flex-start表示最左边；
而垂直（flex-direction: column）排列flex-start表示最上边；
垂直翻转（flex-direction: column-reverse）排列flex-start表示最下边

注：
   1、baseline是字符的底边
   2、其中stretch会改变未设置宽高项目（即容器内子元素）的宽或高（注意是未设置宽高的）
```

## 容器上的设置项
```
display: flex; // 设置当前元素为弹性盒子

flex-direction: row;
flex-wrap: nowrap;
flex-flow: row nowrap; //（简写上面两个，默认，水平，不换行）//column wrap 垂直换行
align-items: stretch; //（默认stretch）定义每个item在交叉轴上的对齐方式
justify-content: flex-start; //定义主轴的对齐方式
align-content: center; // 必须有两个轴，即必须出现换行操作，以行为单位定义对齐方式，即每一行的对齐方式；垂直排列就是定义每一列的对齐方式
```
## item项目上（容器内子元素上）
```
order:0; // 数值越小，排列越靠前，如果你想改变个别item的顺序
flex-grow: 0; //默认为0，即如果存在剩余空间，也不放大。
flex-shrink:1 ; //默认为1，即如果空间不足，该项目将缩小
flex-basis: atuo; //flex-basis属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小。
flex: 0 1 auto;// 简写以上三个属性
align-self: auto;//默认auto继承容器设置的align-items
```