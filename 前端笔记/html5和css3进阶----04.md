##  html5和css3进阶----04

#### 定位

##### 为什么需要定位？

以上效果，标准流或浮动都无法快速实现，此时需要定位来实现。

##### 定位组成

定位=定位模式+边偏移（定位盒子移到的最终位置，由top，bottom，left，right组成）。

##### 定位模式

定位模式决定元素的定位方式，它通过css的position属性来设置，其值可以分为四个：

| 值       | 语义     |
| -------- | -------- |
| static   | 静态定位 |
| relative | 相对定位 |
| absolute | 绝对定位 |
| fixed    | 固定定位 |

##### 1.静态定位static

静态定位是元素的默认定位方式，无定位的意思。

语法：选择器{

position：static;

}

+ 静态定位在布局中很少用到，没有脱离标准流，它没有边偏移。
+ 静态定位在布局时很少用到。

##### 2.相对定位relative

相对定位是在元素移动位置的时候，是相对于它原来的位置来说的，而非浏览器。

语法：选择器{

position：relative;

}

特点：

1.它是相对原来的位置来移动的（移动的位置是参照自己原来的位置）。

2.原来在标准流的位置继续占有，后面的盒子仍然以标准流的方式对待它。（不脱标，继续保留原来的位置）。

##### 3.绝对定位absolute

绝对定位是在元素移动位置的时候，是相对于父级元素来说的。

语法：选择器{

position：absolute；

}

特点：

1.如果没有父级元素或者父级元素没有定位，则以浏览器为准定位（Document文档）。

2.如果父级元素有定位（相对、绝对、固定），则以最近一级的有定位元素作为参考点移动位置。

3.绝对定位不占有原先的位置。

![](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201119102017288.png)

这是由于父类没有使用相对定位，子类相对于浏览器进行定位。

![image-20201026141850393](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201026141850393.png)

就如同这个图，2是1的最近一级，但是如果2没有定位，那么1只能参考3的标准。

##### 子绝父相的由来

子级是绝对位置的话，父级要使用相对定位。

1.子级绝对定位，不会占有位置，可以放到父盒子里面的任意一个地方，不会影响其他的兄弟盒子。

2.父盒子需要加定位限制子盒子在父盒子内部显示。

![image-20201121214428304](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201121214428304.png)

使用子绝父相来定位hot标签。

```
.box-bd ul li > img{
  width: 100%;
}
.box-bd ul li em{
  position:absolute;
  top:0;
  right: -10px;
}
```

```
<div class="box-bd w" style="margin-top: 200px;margin-left: 600px;">
        <ul class="clearfix">
           <li>
               <em>
                   <img src="images/hot.png" alt="">
               </em>
               <img src="images/timg.jpg" alt="goods">
               <h4>java web Spring底层原理，大佬带你飞</h4>
               <div class="info">
                   <span>高级</span>● 10000人在学习
               </div>
```

##### 4.固定定位

固定定位是元素固定于浏览器可视区的位置，主要使用场景，可以在浏览器页面滚动时元素的位置不会改变。

语法：

选择器{

position：fixed；

}

注：不要直接控制图片，而是使用盒子控制图片。

特点：1.以浏览器的可视窗口参照点移动元素。

![image-20201121230602345](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201121230602345.png)

使用固定定位将右侧电话栏定位，好多时候官网的布局就如同这样。

```
  .w{
            height: 1400px;
            width: 800px;
            background-color: pink;
            margin:0 auto;
        }
        .fixed{
            position: fixed;
            left: 50%;
            /*版心的一半*/
            margin-top: 100px;
            margin-left: 400px;
            height: 150px;
            width: 50px;
            background-color: aqua;
        }
```

##### 5.粘性定位

粘性定位被认为是相对定位和固定定位的组合

语法：

选择器{

position：sticky；

top：10px；

}

特点：

1.以浏览器的可视窗口为参照点移动元素（固定定位的特点）。

2.粘性定位占有原先的位置（相对定位的特点）。

3.必须添加top，bottom，left，right四个边偏移的其中一个。

###### 总结：

| 定位模式         | 是否脱标         | 移动位置             | 是否常用     |
| ---------------- | ---------------- | -------------------- | ------------ |
| relative相对定位 | 否（占有位置）   | 相对于自身位置的移动 | 常用         |
| absolute绝对定位 | 是（不占有位置） | 带有定位的父级       | 常用         |
| fixed固定定位    | 是（不占有位置） | 浏览器可视区         | 常用         |
| static静态定位   | 否               | 不能使用边偏移       | 很少         |
| sticky粘性定位   | 否（占有位置）   | 浏览器可视区         | 当前阶段很少 |

##### 定位的叠放次序

可以使用z-index来控制盒子的前后次序（z轴）。

选择器{

z-index：1；

}

这个是有次序的，例如定义三个盒子，按照标准流的方式排放，但是给它加了固定定位以后，会有后来居上的作用。

<img src="C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201122155356805.png" alt="image-20201122155356805" style="zoom:50%;" /><img src="C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201122160537241.png" alt="image-20201122160537241" style="zoom:50%;" />

或者可以使用z-index来调整优先级，数值越大越靠上面。

##### 定位的特殊性

+ 绝对定位和相对定位也和浮动类似。

+ 行内元素添加绝对或者固定定位，可以直接设置高度和宽度。

+ 脱标的盒子不会触发外边距塌陷。

+ 绝对定位（固定定位）会压住下面标准流所有的盒子，但是不会压住其中的文字。（浮动最早是处理文字的环绕）。


