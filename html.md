#### 概述

Html即Hyper Text Mark-up Language超文本标记语言。超文本即超链接，标记即标签

#### 基本结构

``` Html
<!DOCTYPE html> 
<!--
注释
-->
<html lang="en"|"zh-CN">
    <head>
        <meta charset="UTF-8">
        <title>标题</title>
    </head>
    <body>
        <h1>主体<h2>
    </body>
</html>
 <!--body标签	topmargin属性：定义表格与浏览器窗口顶部的间距-->
```

html标签名里的lang属性指定网页的语言：英文"en" 中文"zh-CN"

meta标签里的 charset设置编码格式，utf-8、gbk、ascii等

#### 文档类型

主要有两类：

* HTML5 输入! ，按下Tab
* xhtml 输入html:xt 按下Tab

区别：html5新增了一些标签和属性，其他不会有啥区别

#### 标签

##### 标题标签

```html
<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>
<h4>四级标题</h4>
<h5>五级标题</h5>
<h6>六级标题</h6>
<!--
1-6 字体大小从大到小
搜索引擎会使用标题将网页的结构和内容编制索引
-->
```

##### 段落标签与字符实体

```html
<p>段落标签</p>
<!--
p标签会自动换行，开头不识别空格，段落里面无论的多少个空格，都识别为一个空格
可使用字符实体表示空格
-->

&nbsp;
<!--
字符实体表示的空格不精确，可以使用样式
-->

&gt;
<!--字符实体，大于号">"-->
&lt;
<!--字符实体，小于号"<"-->
```

##### 换行标签

```html
<br />
<!--换行-->

<hr />
<!--划线-->
```

##### 块标签

```html
<div>块标签</div>
<!--
表示一块内容，没有具体的语义，会换行，当块与块紧挨着，样式会用到
与p标签相比，div不带样式， div可嵌套
-->

<span>行内标签</span>
<!--
表示一行内的一小段内容，没有具体的语义，样式会用到
-->
```

##### 含样式和语义标签

```html
<em>表示语气的强调词，加粗</em>

<i>表示专业词汇，倾斜</i>

<b>表示文档中的关键字或者产品名，加粗</b>

<strong>表示非常重要的内容，倾斜</strong>
```

##### 语义化标签

##### 图像标签

```html
<img />
<!--img是独立使用的标签-->
<img src="path" alt="图片说明" />
<!--
src属性，定义图片的引用地址
altt属性，定义图片加载失败时显示的文字，搜索引擎会使用这个文字收录图片、盲人读屏软件会读取这个文字让盲人识别图片
-->
<!--
引用外部资源时的引用地址分为：绝对路径和相对路径
        绝对路径：相对于磁盘位置去定位
        相对路径：相对引用文件本身去定位，./当前目录， ../上一级目录，兼容性比绝对路径好
-->
```

##### 链接标签

```html
<a>链接</a>
<!--在网页上定义一个链接地址-->

<a href="地址，网址图片等", title="提示符字框" target="窗口打开的位置"></a>
<!--
href属性：定义跳转的地址，缺省的地址href="#"
title属性：定义鼠标悬停时弹出的提示文字框
target属性：定义链接窗口打开的位置
	target="_self"缺省值：新页面替换原来的页面，在原来的位置打开
	target="_blank"：打开一个新的窗口显示新的页面
-->
```

##### 列表标签

```html
<ol>
    <li></li>
    <li></li>
</ol>
<!--有序列表
ol>li*3 简单写法，按Tab
-->

<ul>
	<li></li>
    <li></li>
</ul>
<!--无序列表
ul>li*3， 按Tab
ul>(li>a{链接地址})*3，按Tab
-->

<dl>
    <dt>定义术语的题目</dt>
    <dd>术语的解释</dd>
</dl>
<!--定义列表
dl>(dt+dl)*3，按Tab
-->
```

##### 表格标签

```html
<table>
    <tr>
        <td></td>
        <td></td>    
    </tr>
</table>

<!--
table标签属性：
	border属性：定义表格的边框，设置值是数值
	cellpadding属性：定义单元格内容与边框的距离，设置值是数值
	cellspacing属性：定义单元格与单元格之间的距离，设置值是数值
	align属性：设置整体表格相对于浏览器窗口的水平对齐方式，设置值有：left|center|right
	wdith属性：定义表格的宽度
	height属性：定义表格的高度

-->

<!--
	tr标签，定义表格的一行
-->

<!--
td和th标签：定义一行中的一个单元格，td代表普通单元格，th代表表头单元格
	align属性：定义单元格内内容的水平对齐方式，设置值有：left|center|right
	valign属性：定义单元格内内容的垂直对齐方式，设置值有：top|middle|bottom
	colspan属性：设置单元格水平合并，设置值是数值，合并的单元格数
	rowspan属性：设置单元格垂直合并，设置值是数值，合并的单元格数
	width属性：设置单元格宽度，可以是数值，也可以是width="15%"
	height属性：设置单元格高度
	bgcolor属性：设置背景颜色
-->

<!--
tr>(tr>td*3))*4，按Tab，4行3列
-->
```

##### 页面布局

布局也叫做排版，把文字和图片等元素按照我们的意愿有机地排列到页面上，布局的方式有两种：

​	table布局：通过table元素将页面空间划分成若干个单元格，将文字或图片等元素放入单元格中，隐藏表格的边框，从而实现布局。这种布局方式也叫做传统布局。目前主要使用在EDM（广告邮件中的页面）中，主流的布局方式不用这种。

​	HTML+CSS布局（DIV+CSS）：主要通过CSS样式设置来布局文字或图片等元素，需要用到CSS盒子模型、盒子类型、CSS浮动、CSS定位、CSS背景图定位等知识来布局，它比传统布局要复杂，目前是主流的布局方式。

ctrl键点击 多行位置添加

##### 表单

用于收集数据

```html
<form>
    <label>用户名:</label>
    <input type="" name="" />
</form>

<!--
input标签的属性有:
	type="", 值有
		text 
		password 
		radio(单选框, 以name属性区别,  需要指定value值,提交判断那个选项) 
		checkbox(多选框, 需要指定value值)
		file(上传文件)
		submit(提交, value设置按钮显示的值)
		reset(重置,value设置按钮显示值)
-->

<input type="text" name="" />
<!--
单行输入框,比如账户名, 提交时会以name=输入的内容提交上去
-->

<input type="password" name="" />
<!--
单行密码输入框,  隐藏输入值, 提交时以name=输入的内容提交
-->

<input type="radio" name="1" />value
<input type="radio" name="1" />value
<!--
单选输入框, 即需要几个input标签,name属性设置为一样, 然后用户只能点击选中一个选项, 提交时以name=用户选中的值提交,比如男女性别
-->

<input type="checkbox" name="name" value="value1" />
<input type="checkbox" name="name" value="value2" />
<input type="checkbox" name="name" value="value3" />
<!--
多选 设置几个框, 指定相同的name属性, 不同的value属性, 用户可以勾选多个选项, 提交时以name=value1 or value2提交
-->

<input type="file" name="" />
<!--
上传文件
-->

<input type="submit" value="" />
<input type="reset" value="" />
<!--
提交重置按钮
-->

<textarea name="">文本输入框</textarea>
<!--
一个文本框的输入,比如输入评论的框
-->

<select name="">
	<option value="">下拉选项1</option>
    <option value="">下拉选项2</option>
</select>
<!--
下拉框, 提交的时候name=对应的value
-->

<input type="image"  src="" />
<!--
图片作为提交按钮, 一般会导致提交两次,不建议使用,src属性指定图片
-->

<input type="hidden" name="" value="" />
<!--
隐藏表单的内容,不显示,等到提交的时候,就提交上去
-->

<!--
form标签的属性:
	action属性: 一个脚本处理,未指定则本地
	method属性:默认get, get|post  
-->

<label for="user">用户名: </label>
<input type="text" name="username" id="user" />
<!--
label标签的属性:
	for属性, 可以在用户点击标签时, 鼠标直接跳转到指定的id处, 比如在input里面设置id
-->
```



