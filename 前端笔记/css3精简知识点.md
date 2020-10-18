## css3基础

#### 声明样式

![image-20201016231557744](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201016231557744.png)

来源：https://www.w3school.com.cn/cssref/css_selectors.ASP

| 选择器                                                       | 例子                  | 例子描述                                            | CSS  |
| :----------------------------------------------------------- | :-------------------- | :-------------------------------------------------- | :--- |
| [.*class*](https://www.w3school.com.cn/cssref/selector_class.asp) | .intro                | 选择 class="intro" 的所有元素。                     | 1    |
| [#*id*](https://www.w3school.com.cn/cssref/selector_id.asp)  | #firstname            | 选择 id="firstname" 的所有元素。                    | 1    |
| [*](https://www.w3school.com.cn/cssref/selector_all.asp)     | *                     | 选择所有元素。                                      | 2    |
| [*element*](https://www.w3school.com.cn/cssref/selector_element.asp) | p                     | 选择所有 <p> 元素。                                 | 1    |
| [*element*,*element*](https://www.w3school.com.cn/cssref/selector_element_comma.asp) | div,p                 | 选择所有 <div> 元素和所有 <p> 元素。                | 1    |
| [*element* *element*](https://www.w3school.com.cn/cssref/selector_element_element.asp) | div p                 | 选择 <div> 元素内部的所有 <p> 元素。                | 1    |
| [*element*>*element*](https://www.w3school.com.cn/cssref/selector_element_gt.asp) | div>p                 | 选择父元素为 <div> 元素的所有 <p> 元素。            | 2    |
| [*element*+*element*](https://www.w3school.com.cn/cssref/selector_element_plus.asp) | div+p                 | 选择紧接在 <div> 元素之后的所有 <p> 元素。          | 2    |
| [[*attribute*\]](https://www.w3school.com.cn/cssref/selector_attribute.asp) | [target]              | 选择带有 target 属性所有元素。                      | 2    |
| [[*attribute*=*value*\]](https://www.w3school.com.cn/cssref/selector_attribute_value.asp) | [target=_blank]       | 选择 target="_blank" 的所有元素。                   | 2    |
| [[*attribute*~=*value*\]](https://www.w3school.com.cn/cssref/selector_attribute_value_contain.asp) | [title~=flower]       | 选择 title 属性包含单词 "flower" 的所有元素。       | 2    |
| [[*attribute*\|=*value*\]](https://www.w3school.com.cn/cssref/selector_attribute_value_start.asp) | [lang\|=en]           | 选择 lang 属性值以 "en" 开头的所有元素。            | 2    |
| [:link](https://www.w3school.com.cn/cssref/selector_link.asp) | a:link                | 选择所有未被访问的链接。                            | 1    |
| [:visited](https://www.w3school.com.cn/cssref/selector_visited.asp) | a:visited             | 选择所有已被访问的链接。                            | 1    |
| [:active](https://www.w3school.com.cn/cssref/selector_active.asp) | a:active              | 选择活动链接。                                      | 1    |
| [:hover](https://www.w3school.com.cn/cssref/selector_hover.asp) | a:hover               | 选择鼠标指针位于其上的链接。                        | 1    |
| [:focus](https://www.w3school.com.cn/cssref/selector_focus.asp) | input:focus           | 选择获得焦点的 input 元素。                         | 2    |
| [:first-letter](https://www.w3school.com.cn/cssref/selector_first-letter.asp) | p:first-letter        | 选择每个 <p> 元素的首字母。                         | 1    |
| [:first-line](https://www.w3school.com.cn/cssref/selector_first-line.asp) | p:first-line          | 选择每个 <p> 元素的首行。                           | 1    |
| [:first-child](https://www.w3school.com.cn/cssref/selector_first-child.asp) | p:first-child         | 选择属于父元素的第一个子元素的每个 <p> 元素。       | 2    |
| [:before](https://www.w3school.com.cn/cssref/selector_before.asp) | p:before              | 在每个 <p> 元素的内容之前插入内容。                 | 2    |
| [:after](https://www.w3school.com.cn/cssref/selector_after.asp) | p:after               | 在每个 <p> 元素的内容之后插入内容。                 | 2    |
| [:lang(*language*)](https://www.w3school.com.cn/cssref/selector_lang.asp) | p:lang(it)            | 选择带有以 "it" 开头的 lang 属性值的每个 <p> 元素。 | 2    |
| [*element1*~*element2*](https://www.w3school.com.cn/cssref/selector_gen_sibling.asp) | p~ul                  | 选择前面有 <p> 元素的每个 <ul> 元素。               | 3    |
| [[*attribute*^=*value*\]](https://www.w3school.com.cn/cssref/selector_attr_begin.asp) | a[src^="https"]       | 选择其 src 属性值以 "https" 开头的每个 <a> 元素。   | 3    |
| [[*attribute*$=*value*\]](https://www.w3school.com.cn/cssref/selector_attr_end.asp) | a[src$=".pdf"]        | 选择其 src 属性以 ".pdf" 结尾的所有 <a> 元素。      | 3    |
| [[*attribute**=*value*\]](https://www.w3school.com.cn/cssref/selector_attr_contain.asp) | a[src*="abc"]         | 选择其 src 属性中包含 "abc" 子串的每个 <a> 元素。   | 3    |
| [:first-of-type](https://www.w3school.com.cn/cssref/selector_first-of-type.asp) | p:first-of-type       | 选择属于其父元素的首个 <p> 元素的每个 <p> 元素。    | 3    |
| [:last-of-type](https://www.w3school.com.cn/cssref/selector_last-of-type.asp) | p:last-of-type        | 选择属于其父元素的最后 <p> 元素的每个 <p> 元素。    | 3    |
| [:only-of-type](https://www.w3school.com.cn/cssref/selector_only-of-type.asp) | p:only-of-type        | 选择属于其父元素唯一的 <p> 元素的每个 <p> 元素。    | 3    |
| [:only-child](https://www.w3school.com.cn/cssref/selector_only-child.asp) | p:only-child          | 选择属于其父元素的唯一子元素的每个 <p> 元素。       | 3    |
| [:nth-child(*n*)](https://www.w3school.com.cn/cssref/selector_nth-child.asp) | p:nth-child(2)        | 选择属于其父元素的第二个子元素的每个 <p> 元素。     | 3    |
| [:nth-last-child(*n*)](https://www.w3school.com.cn/cssref/selector_nth-last-child.asp) | p:nth-last-child(2)   | 同上，从最后一个子元素开始计数。                    | 3    |
| [:nth-of-type(*n*)](https://www.w3school.com.cn/cssref/selector_nth-of-type.asp) | p:nth-of-type(2)      | 选择属于其父元素第二个 <p> 元素的每个 <p> 元素。    | 3    |
| [:nth-last-of-type(*n*)](https://www.w3school.com.cn/cssref/selector_nth-last-of-type.asp) | p:nth-last-of-type(2) | 同上，但是从最后一个子元素开始计数。                | 3    |
| [:last-child](https://www.w3school.com.cn/cssref/selector_last-child.asp) | p:last-child          | 选择属于其父元素最后一个子元素每个 <p> 元素。       | 3    |
| [:root](https://www.w3school.com.cn/cssref/selector_root.asp) | :root                 | 选择文档的根元素。                                  | 3    |
| [:empty](https://www.w3school.com.cn/cssref/selector_empty.asp) | p:empty               | 选择没有子元素的每个 <p> 元素（包括文本节点）。     | 3    |
| [:target](https://www.w3school.com.cn/cssref/selector_target.asp) | #news:target          | 选择当前活动的 #news 元素。                         | 3    |
| [:enabled](https://www.w3school.com.cn/cssref/selector_enabled.asp) | input:enabled         | 选择每个启用的 <input> 元素。                       | 3    |
| [:disabled](https://www.w3school.com.cn/cssref/selector_disabled.asp) | input:disabled        | 选择每个禁用的 <input> 元素                         | 3    |
| [:checked](https://www.w3school.com.cn/cssref/selector_checked.asp) | input:checked         | 选择每个被选中的 <input> 元素。                     | 3    |
| [:not(*selector*)](https://www.w3school.com.cn/cssref/selector_not.asp) | :not(p)               | 选择非 <p> 元素的每个元素。                         | 3    |
| [::selection](https://www.w3school.com.cn/cssref/selector_selection.asp) | ::selection           | 选择被用户选取的元素部分。                          | 3    |

##### css选择器的作用

场景：就是选择标签时使用的。

##### 基础选择器----标签选择器

例如p标签，div标签，缺点就是整体选择。

```
.p{xxx}
```

##### 基础选择器----类选择器

举个例子

```
<style>
.xxx{
color:颜色;
}
</style>
<ul>
<li class="xxx">1</li>
<li>2</li>
<li>3</li>
</ul>
```

##### css3命名规则

来源：https://www.cnblogs.com/jiuxin/p/10116405.html

| 名字                     | 表达       | 名字     | 表达              |
| ------------------------ | ---------- | -------- | ----------------- |
| 头                       | header     | 内容     | content/container |
| 尾                       | footer     | 导航     | nav               |
| 侧栏                     | sidebar    | 栏目     | column            |
| 页面外围控制整体布局宽度 | wrapper    | 左右中   | left/right/center |
| 登录条                   | loginbar   | 标志     | logo              |
| 广告                     | banner     | 页面主体 | main              |
| 热点                     | hot        | 新闻     | news              |
| 下载                     | download   | 子导航   | subnav            |
| 菜单                     | menu       | 子菜单   | submenu           |
| 搜索                     | search     | 友情链接 | friendlink        |
| 页脚                     | footer     | 版权     | copyright         |
| 滚动                     | scroll     | 内容     | content           |
| 标签页                   | tab        | 文章列表 | list              |
| 提示信息                 | msg        | 小技巧   | tips              |
| 栏目标题                 | title      | 加入     | joinus            |
| 指南                     | guild      | 服务     | service           |
| 注册                     | register   | 状态     | status            |
| 投票                     | vote       | 合作伙伴 | partner           |
| 摘要                     | summary    | 按钮     | btn               |
| 主要的                   | master.css | 模块     | module.css        |
| 基本公用                 | base.css   | 布局     | layout.css        |
| 主题                     | themes.css | 专栏     | columns.css       |
| 文字                     | font.css   | 表单     | froms.css         |
| 补丁                     | mend.css   | 打印     | print.css         |

### 类选择器----多类名

格式：两个类名中间使用空格隔开。

多类名选择器很好使用。

举个实际使用的例子。

```
<style>
</style>
.类1{
属性:xxx;
}
.类2{
属性:xxx;
}
<body>
<div class="类1 类2">内容</div>
</body>
```

总结： 第二次看html发现以前写的代码太过于冗余，这个多类名可以解决很多的问题，要是类1属性和类2属性合在一起，可能会多写很多的代码，是模块化编程的思想。

场景：需要有某些共同点。

```
<style>
</style>\
.类x{
抽离出公共的部分;
}
.类1{
属性:xxx;
}
.类2{
属性:xxx;
}
<body>
<div class="类x 类2">内容</div>
</body>
```

##### 基础选择器----id选择器（#表示）

特点：只能调用一次，具有唯一性，常常好javascript搭配使用。

##### 基础选择器----通配符选择器

*号定义，表示选择页面中所有元素。

### css字体属性

font-family:'中文/英文都可以';定义字体样式属性系列。

font-size:'字体大小/像素';定义字体大小。

font-weight:'字体的粗细/像素'；定义字体的粗细。

font-style:'normal/italic';斜体和粗体；

![image-20201017203415392](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201017203415392.png)

![image-20201017203722433](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201017203722433.png)

##### css文本属性

text-algin:元素内容文本对齐方式。

left：左对齐；right：右对齐；center：居中对齐；

##### 装饰文本

text-decoration：

![image-20201017205033902](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201017205033902.png)

##### 行间距

line-height：xxxpx；用于设置行的距离，行高，可以控制文字行与行之间的距离。

文字本身的高度+ 上间距+下间距。

![image-20201017210333309](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201017210333309.png)

##### 首行缩进

text-indent：1em；首行缩进1em。

##### 内部样式表

```
<head>
    <style></style>
</head>
```

##### 行内样式表

```
<p style=""></p>
```

##### 外部样式表

```
<link rel="stylesheet" href="文件存放的路径">
```



