---
title: css3 学习笔记（一）
date: 2016-12-8 13:01:48
tags:
	- css
categories: 
	- css
---

# css3 学习笔记（一）

>  css3 的背景属性： 

css3 允许应用纯色作为背景，也允许使用背景图片创建相当复杂的效果<!--more-->
![css 背景属性](http://oalppxaqn.bkt.clouddn.com/css%E8%83%8C%E6%99%AF%E5%B1%9E%E6%80%A7.png)

* background-attachment属性: 控制背景图片是否固定或者随着页面滚动；
* background-color属性: 设置元素的背景颜色；
* background-image属性: 把图片设置为背景；
* background-position属性: 设置图片的起始位置；
	*eg：background-position：right top； 背景图片从图片顶部开始显示在屏幕右方；*
* background-repeat: 设置背景图片是否重复展示；
* background-size: 规定背景图片的尺寸；
* background-origin: 规定背景图片的定位区域；
* background-clip: 规定背景的绘制区域；

>  css3 的文本属性：

css3 文本属性可定义文本外观
![css 文本属性](http://oalppxaqn.bkt.clouddn.com/css%E6%96%87%E6%9C%AC%E5%B1%9E%E6%80%A7.png)

* color属性：定义文本的颜色；
* direction属性：文本方向；
* line-height属性：行高属性；
* letter-spacing属性： 字符间距；
* text-align属性： 字符间的文本对齐样式；
* text-decoration属性： 向文本添加修饰；
* text-indent属性： 缩进元素中文本的首行；
* text-transform属性： 对元素中的字母进行操作，eg：全大写、首字母大写等等；
* unicode-bidi属性： 设置文本方向；
* white-space属性： 元素中空白的处理方式；
* word-spacing属性： 字间距；
* text-shadow属性： 向文本添加阴影；
	*eg：有四个属性值，第一个距左距离、第二个距上距离、第三个清晰度、第四个背景颜色；*
* word-wrap属性： 规定文本的换行规则；

**常用属性：** color、text-align、text-indent、text-transform、line-height、direction等；

>  css3 的字体属性：

css字体属性定义文本的字体系列、大小、加粗、风格和变形；
```
@fontface {
	font-family: 自己定义的字体的名字;
	src: url(); //需要使用的字体的路径;
}

body {
	font-family: 自己定义的所需要使用的字体名字;
}
```
![css 字体属性](http://oalppxaqn.bkt.clouddn.com/css%20%E5%AD%97%E4%BD%93%E5%B1%9E%E6%80%A7.png)

* font-family属性： 设置字体系列；
* font-size属性： 设置字体的尺寸；
* font-style属性： 设置字体风格；
* font-variant属性： 以小型大写字体或者正常字体显示文本；
* font-weight属性： 设置字体的粗细；

> CSS3 的链接🔗属性：

1. css3 中链接的四种状态：

	* a:link	普通的、未被访问的链接；
	* a:visited	用户已访问的链接；
	* a:hover	鼠标指针位于链接上方；
	* a:active	链接被点击的时刻；

2. css3 中常见的链接样式:

	text-decoration 属性大多用于去掉链接下方的下划线，传值为none；

3. css3 中链接的背景颜色：

	background-color 属性设置链接的背景颜色；
	
> css3 的列表属性：

css3 允许放置、改变列表标志，或者将图像作为列表项标志；
![css 列表属性](http://oalppxaqn.bkt.clouddn.com/css%20%E5%88%97%E8%A1%A8%E5%B1%9E%E6%80%A7.png)

* list-style属性： 简写列表项；
* list-style-image属性： 列表项图像；
* list-style-position属性： 列表标志位置；
* list-style-type属性： 列表类型；

```
html:
<ul class="ul1">
	<li>苹果</li>
	<li>栗子</li>
	<li>香蕉</li>
	<li>水果</li>
</ul>
<ul class="ul2">
	<li>苹果</li>
	<li>栗子</li>
	<li>香蕉</li>
	<li>水果</li>
</ul>

css:
ul li {
	list-style-image: url(“pictureName.png”);
}

ul.ul1 {
	list-style-position: inside;
}
ul.ul2 {
	list-style-position: outside;
}
```

> css3 的表格属性：

*css 的表格属性可以设置表格的外观*
css 的表格属性包括：
	1. 表格边框
	2. 折叠边框
	3. 表格宽高
	4. 表格文本对齐
	5. 表格内边距
	6. 表格颜色
```
html:
<tabel id="tb">
<tr>
	<th>姓名</th>
	<th>年龄</th>
	<th>性别</th>
</tr>
<tr>
	<td>小红</td>
	<td>18</td>
	<td>女</td>
</tr>
<tr>
	<td class="alt">小红</td>
	<td>18</td>
	<td>女</td>
</tr>
<tr>
	<td>小红</td>
	<td>18</td>
	<td>女</td>
</tr>
<tr>
	<td class="alt">小红</td>
	<td>18</td>
	<td>女</td>
</tr>
</tabel>

css:
#tb {
	border-collapse: collapse;/*折叠边框效果*/
	width: 500px; ／*表格宽500px*／
}
#tb td, #tb th {
	border: 1px solid bisque;／*表格添加一个1px bisque色的外边框效果*／
	padding: 5px;
}
#tb th {
	text-align: right;/*表格文本右对齐*/
	background-color: aqua;
	color: #ffffff;
}
#tb tr.alt td {
	color: black;
	background-color: aquamarine;
}
```

> css3 的轮廓属性

*轮廓主要是用来突出元素的作用*

* outline 属性： 设置轮廓的属性；
* outline-color属性： 设置轮廓的颜色；
* outline-style属性： 设置轮廓的样式；
* outline-width属性： 设置轮廓的宽度； 




 











