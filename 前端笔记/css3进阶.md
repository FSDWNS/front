## html5和css3进阶----01

#### emmet语法

vscode内置emmet语法结构，点击！+Tab可以生成。想生成什么标签直接输入名字。

父子关系：使用>。

兄弟关系：使用+。

#### 自动化格式代码

![image-20201018161851597](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201018161851597.png)

#### 复合选择器

```
ol li{

xxx；

}
```

注意：中间隔开，ol为父类，li为子类。

#### 子元素选择器（子选择器）

```
<style>
nav a{
color:red;
}
</style>
<body>
<div class="nav">
<a href="#">子类1</a>  //变红
<a href="#">子类2</a>
</div>
</body>
```

#### 并集选择器

规范：使用，隔开

```
<style>
nav1,                //并集选择器适合竖着写。
a,
.nav2{
color:red;
}
</style>
<body>
<div class="nav1">大哥</div>
<a href="#">兄弟</a>
<div class="nav2">
<a href="#">子类1</a>  //变红
<a href="#">子类2</a>
</div>
</body>
```

#### 链接伪类选择器

使用：来表示。

+ 链接伪类选择器

+ 结构伪类

  | ----      | ----                       |
  | --------- | -------------------------- |
  | a:link    | 选择所有未被访问的链接     |
  | a:visited | 选择已被访问的链接         |
  | a:hover   | 选择鼠标指针位于其上的链接 |
  | a:active  | 选择活动链接               |

  顺序执行：LVHA。

  #### focus伪类选择器

   input：focus{

  background-color：yellow；

  }

input选取的表单元素。

![image-20201018185303781](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201018185303781.png)

#### 常见的块元素

```
<h1>~<h6>、<p>、<div>、<ul>、<ol>、<li>
```

块级元素的特点：

1.独占一行。

2.高度，宽度，外边距以及内边距都可以控制。

3.宽度是默认容器的100%。

4.是一个容器及盒子，里面可以放行内或者块级元素。

注意：文字类的元素内不能使用块级元素。

p、h标签主要用于存放文字，因此p里面不能放块级元素。

#### 常见的行内元素

```
<a>、<strong>、<b>、<em>、<i>、<del>、<s>、<ins>、<u>、<span>
```

行内元素的特点：

1.相邻行内元素在一行上，一行可以显示多个。

2.高、宽直接设置无效。

3.默认宽度就是它本身内容的宽度。

4.行内元素只能容纳文本或其他行内元素。

#### 行内块元素

```
<img />、<input />、<td>
```

它们同时具有块元素和行内元素的特点。

行内块元素的特点：

1.和相邻行内元素（行内块）在一行上，但是他们之间会有空白间隙，一行可以显示多个。

2.默认宽度就是他本身的内容宽度。

3.高度、行高，外边距以及内边距都难以控制（块级元素特点）。

#### 元素显示模式转换

+ 转换为块元素：display：block；
+ 转换为行内元素：display：inline；
+ 转换为行内块：display：inline-block；

#### 文字的垂直居中

当height：xxpx；和line-height：xxpx；相等时，可以在盒子中实现垂直居中的效果。

####  css背景

###### 背景颜色：

background-color：transparent|color（透明|颜色）。

###### 背景图片（装饰性小图片或者是超大的背景图片，便于控制位置）：

background-image：url(url)|none；

background-repeat|no-repeat|repeat-x|repeat-y

repeat:平铺|no-repeat:不平铺|repeat-x:向x轴平铺|repeat-y：向y轴平铺

###### 位置控制：

background-position：center top；//水平向上

background-position：right center；//向右水平垂直

注意：与方位名词顺序无关。

background-position：right；//此时，水平一定是靠右对齐，第二个参数省略y轴。

background-position：top；//此时，水平一定是向上对齐，第二个参数省略x轴。

###### 背景固定：

background-attachment：scroll（滚动）|fixed(固定)；

###### 背景复合写法：

background：black url（url） repeat-y fixed top；

###### 背景颜色半透明：

background：(0,0,0,0.5);//最后一个参数是alpha透明度，取值范围在0-1之间。

#### css三大特性

###### 层叠性：

```
div{
color：red；
font-size：;//不会覆盖掉
}

div{
color：yellow；
}
```

就近原则：下面的就会覆盖掉上面的，不会全部覆盖掉，不同的东西不会覆盖掉。

###### 继承性：

```
div{
color:red;
}

<div>
<p>aaa</p>
</div>

p标签的颜色会继承父类div的颜色。
```

作用：降低css样式的复杂性，简化代码。

行高的继承：

```
father{
color:red;
font:12px(文字大小)/24px(行高)或者1.5倍'Microsoft YaHei';
}
son{
font-size:14px;
1.5*14//当前的行高
}
p{
font-size:16px;
1.5*16//当前的行高
}
<div class="father">
<div class="son">
<p>aaa</p>
</div>
</div>

```

###### 优先级

+ 选择器相同，执行叠层性。
+ 选择器不同，根据权重执行。

| 选择器               | 选择器权重 |
| -------------------- | ---------- |
| 继承或者*            | 0,0,0,0    |
| 元素选择器           | 0,0,0,1    |
| 类选择器，伪类选择器 | 0,0,1,0    |
| ID选择器             | 0,1,0,0    |
| 行内样式，style=“”   | 1,0,0,0    |
| ！important 重要的   | 无穷大     |

继承权重为0。

#### css盒子模型

网页的布局过程：

最重要的一步就是利用盒子的浮动进行布局。

盒子里面的内容：

###### border：边框

```
border-width：xxpx；

border-style：solid（实线边框）|dotted（点线）|dashed（虚线）；

border-color：颜色；

边框的复合性写法：border：1px solid red；//没有顺序

边框可以分开来写。
```

举个例子

写一个盒子200*200，上边框为 红色，其余边框为蓝色。

```
方案一
div{
width：200px;
height：200px;
border-top:1px solid red;
border-left:1px solid blue;
border-bottom:1px solid blue;
border-right:1px solid blue;
}

<div></div>
```

```
方案二：
div{
width：200px;
height：200px;
border:1px solid blue;
border-top：1px solid red;
}

<div></div>
```

#### 注意：

1.很显然，第二种方式更加简单，因为利用了css样式的层叠性，red只是层叠了上边框。

2.border-top不能够放在border上面的，因为就近原则。

3.边框会影响盒子的实际大小。

border-collapse:collapse;会把相邻的边框合在一起。

###### content：内容

###### padding：内边距（设置边框与盒子内容之间的距离）。

+ 1个值，代表上下左右相同。
+ 2个值，代表上下是一个值，左右是一个值。
+ 3个值，代表上一个值，左右一个值，下一个值。
+ 4个值，代表上下左右分别代表不同的值。

##### 顺序：上--右--下--左 顺时针转圈。

案例：做导航栏的时候使用padding撑开盒子。

###### margin：外边距（控制盒子和盒子之间的距离）

##### 嵌套块元素垂直外边距的塌陷

![image-20201021171914973](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201021171914973.png)

很明显，我没有设置父类盒子的外边距，我只是设置了子类盒子的外边距，为什么会掉下来了？

这个问题我遇到过很多次，原因就是在有嵌套关系的时候，父元素有上外边距，此时父元素会塌陷较大的外边距值。

解决方案：

+ 为父元素定义一个上边框。
+ 可以为父元素定义内边距。
+ 可以为父元素添加overflow：hidden；

#### 清除内外边距

*{

margin：0；

padding：0；

}