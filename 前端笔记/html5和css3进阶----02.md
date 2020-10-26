

## html5和css3进阶----02wei

##### 小米布局案例1：产品模块布局分析

![image-20201021180443372](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201021180443372.png)

类似于这样的产品模块，使用css+html布局来完成。

![](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201021191941705.png)

而且加了伪类选择器，使得鼠标滑动的时候出现变大的效果。

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MI</title>
<style>
    *{
        margin: 0;
        padding: 0;
    }
    body{
       background-color: #f5f5f5;
    }
    .box{
        width:1100px;
        height:400px;
        margin: 200px auto;
      
       
    }
    .box1{
        width:200px;
        height:350px;
        background-color: white;
       margin: 10px 10px 10px 20px;
       display:inline-block;
       padding: 10px;
       overflow: hidden;
       transition: all 1s;
    }
    .box1:hover{
			 transform: scale(1.07);
			}
    .box1 img{
        width: 100%;
    }
    .box1 h5{
        text-indent: 25px;
    }
    .box1 p{
        font-family: 宋体;
        font-size: 10px;
        color: #9e9494;
        margin-top: 20px;
    }
    .box1 h4{
        font-family: 微软雅黑;
        color:red;
        margin-top: 20px;
        text-indent: 2em;
        float: left;
    }
    #lgprice{
        margin-top: 20px;
        color: #9e9494;
    }
</style>
</head>
<body>
    <div class="box">
        <div class="box1">
            <img src="image/picture.jpg"/>
            <h5>Redmi 红米电视 70英寸</h5>
             <p>70英寸震撼巨屏，4K画质，细腻如真</p>
             <p><h4>3429元</h4></p> 
           <h4 id="lgprice"> <del>3117元</del></h4>
            
        </div>
        <div class="box1">
            <img src="image/picture.jpg"/>
            <h5>Redmi 红米电视 70英寸</h5>
             <p>70英寸震撼巨屏，4K画质，细腻如真</p>
             <p><h4>3429元</h4></p> 
           <h4 id="lgprice"> <del>3117元</del></h4>
            
        </div>
        <div class="box1">
            <img src="image/picture.jpg"/>
            <h5>Redmi 红米电视 70英寸</h5>
             <p>70英寸震撼巨屏，4K画质，细腻如真</p>
             <p><h4>3429元</h4></p> 
           <h4 id="lgprice"> <del>3117元</del></h4>
            
        </div>
        <div class="box1">
            <img src="image/picture.jpg"/>
            <h5>Redmi 红米电视 70英寸</h5>
             <p>70英寸震撼巨屏，4K画质，细腻如真</p>
             <p><h4>3429元</h4></p> 
           <h4 id="lgprice"> <del>3117元</del></h4>
            
        </div>
      
    </div>
</body>
</html>
```

#### 圆角边框

border-radius：length；//数值越大，越圆。可以跟四个值，顺时针方向。

border-top-left-radius：xxpx；//设置左上角。

#### 盒子阴影

box-shadow：h-shadow v-shadow blur spread color inset；//严格按照顺序来写

| 值       | 描述                                                         |
| -------- | ------------------------------------------------------------ |
| h-shadow | 必须，水平阴影的部分，可以是负值。                           |
| v-shadow | 必须，垂直阴影的部分，可以是负值。                           |
| blur     | 可选，模糊距离。                                             |
| spread   | 可选，阴影尺寸的位置。                                       |
| color    | 可选，阴影的颜色。                                           |
| inset    | 可选，可将外部阴影改为内部阴影，但是默认outset但是没必要写 。 |

##### 小米布局案例2：增加阴影效果

```
  box-shadow: 10px 10px 10px rgba(0,0,0,0.3);
```

很明显阴影的效果会出来。

![](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201022143732294.png)

#### 浮动

为什么需要浮动？

使用行内块会出现空隙。

网页布局的第一准则：多个块级元素纵向排列找标准流，多个块级元素横向排列找浮动。

什么是浮动？

float属性用于创建浮动窗，将其移到一边，直到左边缘或右边缘触及包含块或另一个浮动框的边缘。

##### 浮动特性：

+ 脱标，脱离标准普通流移动到指定的位置。
+ 浮动的盒子不再保留原先的位置。

叠起来的感觉。

<img src="C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201022152328178.png" alt="浮动前" style="zoom:80%;" /><img src="C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201022152857104.png" alt="浮动后" style="zoom: 50%;" />                

注意：

+ 如果多个盒子都设置了浮动，则它们会按照属性值一行内显示并且顶端对齐。

+ 浮动的元素是互相贴在一起的（没有缝隙）。如果父级宽度装不下这些浮动的盒子，多出的盒子会启另一行对齐。

##### 浮动元素会具有行内块元素的特性

任何元素都可以浮动，不管原先是什么模式的元素，添加浮动之后具有行内块元素的特性。

##### 浮动元素经常和标准流父级搭配使用

##### 小米布局案例3：浮动布局

![image-20201022155619136](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201022155619136.png)

这个是小米官网的极简布局形式，可以使用浮动来实现。

##### 案例：小米布局实例4：

![image-20201022165016738](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201022165016738.png)

这里主要实现它的布局模式。

![image-20201022164335466](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201022164335466.png)

+ 有一个点要说到，那就是权重问题。

```
.box li{
    width: 296px;
    height: 285px;
    background-color: white;
    list-style: none;
    margin-right: 14px;
    float: left;
   
}
.box .last{
    margin-right: 0;
}
```

+ 我们这里的last的权重没有li高，所以使用

```
 .last{
    margin-right: 0;
}
```

+ 是不可以解决问题的，或者给li绑定一个id属性，可以解决这个问题，加上.box也是可以的。

+ 这个主要是父类的盒子装不下子类的容器，使用css层叠性去掉最后一个盒子不需要的属性。

##### 小米布局案例5：浮动的综合学习。

![image-20201022165111412](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201022165111412.png)

![](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201022170908731.png)

##### 浮动要注意的点

+ 一个浮动，理论上所有的兄弟元素都要浮动。
+ 浮动只会压住后面的标准流，不会压住前面的标准流。
+ 先使用标准父元素排列上下位置，之后内部子元素采取浮动排列左右位置。

#### 所有的父盒子都必须要有高度吗？

当子元素很多时候，不方便计算。

理想中的就是让子元素撑开父元素。

但是不可以，父盒子的兄弟盒子会跑上去。但可以使用清除浮动。

##### 为什么要清除浮动

+ 父级没高度。
+ 子盒子浮动了。
+ 影响下面布局了，我们就要清除浮动。

##### 清除浮动

+ 本质：清除浮动元素造成的影响。

+ 如果父盒子本身有高度，则不需要清除浮动。
+ 清楚浮动之后，父级就会根据浮动的子盒子自动检测高度，父级有了高度，就不会影响下面的标准流了。

语法：

```
选择器{clear:属性值；}
```

| 属性值 | 描述                 |
| ------ | -------------------- |
| left   | 清除左侧浮动的影响   |
| right  | 清除右侧浮动的影响。 |
| both   | 两侧都清除           |

下面这个案例就是没有给父类设置高度，虽然独占一行可以，但是变为一行的时候，下面的元素还是会挤上来。

![image-20201022175006634](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201022175006634.png)

如何去解决这个问题呢？

一般使用clear：both；

清除浮动的策略：

+ 方法一：闭合浮动，使用<div></div>。
+ 方法二：父级添加overflow

可以给父级添加overflow属性，将其属性设置为hidden、auto或scroll。

缺点：溢出隐藏

+ ：after伪元素清除浮动。
+ 双伪元素清除浮动。

```
.clearfix:before,.clearfix:after{
content:"";
display:table;
}
.clearfix:after{
clear:both;
}
.clearfix{
*zoom:1;
}

<div class="box clearfix">
子元素
</div>
```

使用before和after关住盒子。

缺点：I6和I7不支持

```
.clear{
            clear:both;
        }
 <div class="clear"></div>//加在所浮动盒子的下面
```

这个方法叫做额外标签法，同时被称为“隔墙法”。但是

注意：这个元素必须是块级元素，不能是行级元素。

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .left{
            float: left;
            width: 100px;
            height: 100px;
            background-color: blueviolet;
        }
        .right{ 
               float: left;
            width: 100px;
            height: 100px;
            background-color: rgb(53, 47, 58);
        }
        .box2{
          
            width: 500px;
            height: 200px;
            background-color: brown;
        }
        .clear{
            clear:both;
        }
    </style>
</head>
<body>
    <div class="box1">
    <div class="left"></div>
    <div class="right"></div>
    <div class="clear"></div>
    </div>
    <div class="box2"></div>
</body>
</html>
```

![image-20201022175618437](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201022175618437.png)

##### ps切图

jpg：jpeg（jpg）对色彩的信息保留好，高清，颜色较多，产品类一般使用。

gif：gif最多存储256色，通常显示简单图形及其字体，可保留透明背景和动画效果，多用于图片小动画。

png：png图像结合了jpg和jpeg的优点，保留透明背景。

psd：是photoshop的专用格式，里面可以放图层，通道，遮罩等多种设计稿，可以复制文字，获得图片，甚至测距离和大小，比较方便。

