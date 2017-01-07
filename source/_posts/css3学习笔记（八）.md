---
title: css 学习笔记（八）
date: 2016-12-19 14:21:56
tags:
	- css
categories:
	- css
---

> css3 学习笔记（八）
	
### css3选择器详解（二）

* 选择器：first-child、last-child、nth-child和nth-last-child
	能够特别针对一个父元素中的第一个子元素、最后一个子元素、指定序号的子元素，甚至第偶数个或第奇数个子元素进行样式的指定。<!--more-->
	
	```
	eg：
	html：
	<h2>列表</h2>
	<ul>
		<li>列表1</li>
		<li>列表2</li>
		<li>列表3</li>
		<li>列表4</li>
		<li>列表5</li>
		<li>列表6</li>
	</ul>
	css:
	li:first-child{
	background-color: yellow;/*列表一整行背景色变为黄色*/
}
li:last-child{
	background-color: green;/*列表六一整行背景色变为绿色*/
}
li:nth-child(3){/*此处参数为需要改变的编号,正向编号*/
	background-color: red;/*列表三一整行背景色变为红色*/
}/*参数可以传递为：an+b的形式，即2n+1，2n+2等等*/
li:nth-last-child(3){/*此处参数为需要改变的编号，反向编号*/
	background-color: orange;/*列表四一整行背景色变为橙色*/
}/***参数可以给奇数odd或者偶数even***/
	```
	<span style="color:red">参数还可以给奇数odd或者偶数even</span>
	
* 选择器：nth-of-type和nth-last-of-type
	在css3中使用nth-of-type和nth-of-type选择器来避免某一类问题的发生。使用这两个选择器时，css3在计算子元素是第奇数个子元素还是第偶数个子元素时，就只针对同类型的子元素进行计算了。
	
	```
	eg:
	html:
	<h2>文章标题</h2>
	<p>文章正文</p>
	<h2>文章标题</h2>
	<p>文章正文</p>
	<h2>文章标题</h2>
	<p>文章正文</p>
	<h2>文章标题</h2>
	<p>文章正文</p>
	css:
	h2:nth-of-type(odd){
		background-color:red;
	}/*偶数行元素背景变为红色，正向编号*/
	h2:nth-last-of-type(even){
		background-color:blue;
	}/*奇数行元素背景变为蓝色，反向编号*/
	```
* only-child选择器
	当元素只有一个列表项的时候，可以代替使用nth-child和nth-last-child选择器的方法；
	
	```
	eg:
	html:
	<ul>
	 	<li>第一个</li>
	 </ul>
	 <ul>
	 	<li>第一个</li>
	 	<li>第二个</li>
	 	<li>第三个</li>
	 	<li>第四个</li>
	 </ul>
	 css:
	 li:nth-child(1){
	 	background-color:red;
	 }
	 当元素像第一个一样只有一个列表项可以使用，则能用
	 li:only-child{
	 	background-color:red;
	 }方法代替以上nth-child和nth-last-child方法；
	```

