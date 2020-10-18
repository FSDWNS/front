## Html5基础

#### 语义

+ 加粗：<strong></strong>或者<b></b>
+ 倾斜：<em></em>或者<i></i>
+ 删除线：<del></del>或者<s></s>
+ 下划线： <ins></ins>或者<u></u>

#### 图像

alt和title有什么区别？

+ alt是图片显示不出来的时候，显示的替换文本。
+ title是鼠标悬浮在图片上面时候显示的文本。

#### 链接

target：目标窗口的弹出方式。（_self为默认值，__blank为打开新的窗口）。

下载链接：如果href里面是一个文件地址或者压缩包，它会下载这个文件。

锚点链接：同属于html一个页面，点击一下跳转到本页面某个位置。

```
举个例子：
<a href="#xxx"></a>
1.aaa
2.bbb
3.xxx   //<h1 id="xxx"></h1>
这里肯定会跳转到xxx
```

#### 注释

<!---->

#### 特殊字符

空格：&nbsp ;

小于号：&lt；

大于号：&gt；

#### 表格

```
<table>     
    <tr>
          <th>1</th>  //表头，有加粗和居中的作用
          <th>2</th>
          <th>3</th>
          <th>4</th>
    </tr>
    <tr>
        <td  style="height:20px"></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
     <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
</table>
```

<table>     
    <tr>
          <th>1</th>
          <th>2</th>
          <th>3</th>
          <th>4</th>
    </tr>
    <tr>
        <td  style="height:20px"></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
     <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
</table>

属性：（要写到table里面）

+ align：表格相对周围元素的对齐方式。
+ border：表格是否有边框。
+ cellpadding：像素值，规定单元边沿与其内容之间的空白，默认1像素，就是里面字体距离边框的位置。
+ cellsapcing：像素值，规定单元格之间的空白，默认2像素，就是双边框线变成单条线。

#### 表结构

<thead></thead>

<tbody></tbody>

有更好地语义。

### 合并单元格

跨行合并：rowspan="合并单元格";

跨列合并：colspan="合并单元格";

1.决定跨行还是跨列合并。

2.找到目标单元格，写上合并方式。例如<td colsspan="2"></td>

3.删除多余单元格。(合并之后，会多余出来一个)

![image-20201015203422797](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201015203422797.png)

#### 无序列表

```
<ul>
<li></li>
</ul>
```

#### 有序列表

```
<ol>
<li></li>
</ol>
```

#### 自定义列表

```
<dl>
    <dt></dt>
    <dd></dd>
    <dd></dd>
</dl>
```

#### 表单域

表单域是一个包含表单的元素。

<from action="url地址" method="提交方式" name="表单域名称"></from>

#### input表单元素

![image-20201015222323671](C:\Users\18522\AppData\Roaming\Typora\typora-user-images\image-20201015222323671.png)

#### 文本域

```
<textarea></textarea>
rows="行数"
cols="列数"
```

<textarea></textarea>

查阅文档：

mdn网站：https://developer.mozilla.org/zh-CN/

##### 