---
title: css 学习笔记（七）
date: 2016-12-19 10:21:28
tags:
	- css
categories:
	- css
---

> css3 学习笔记（七）

### css3 选择器详解（一）
1. 属性选择器
	css3 中新增加了三个属性选择器，分别为：[att*=val]、[att^=val]和[att$=val]，正因为这三个	属性的存在才使得属性选择器拥有了通配符的概念。<!--more-->

	* [att*=val]   [属性名*=属性值或属性值中的一部分]   
		`eg: [id*=div] 意思是对属性id中包含div的所有id都进行操作`
	* [att^=val]	[属性名^=属性值或者属性值中的一部分]
		`eg: [id^=div] 意思是对属性id中首字母是div开始的所有id进行操作`
	* [att$=val]	[属性名$=属性值或者属性值中的一部分]
		`eg： [id$=div] 意思是对属性id中末尾字母是div的所有id进行操作`

2. 伪类选择器
	结构性伪类选择器
	* 伪类选择器
	* 伪元素选择器
		* first-line	
		
			`eg: p:first-line{color:red;} 让p元素中第一行内容字体变为红色`
		* first-letter
		
			`eg: p:first-letter{color:green;} 让p元素中第一行第一个字符的字体变为绿色`
		* before
		
			`eg: li:before{content:"--";} 在每一个li元素的内容起始位置添加--标识`
		* after
		
			`eg: li:after{content:"这是列表项中的一个元素"} 在每一个li元素的内容结尾位置添加“”里的文字`
	
3. 选择器之root、not、empty和target
	css3中结构性伪类选择器的共同特征是允许开发者根据文档中的结构来指定元素的样式；
	
	* root  将样式绑定在页面的根元素上面
	```
	eg： :root{background-color:blue;} 将页面中根元素的背景色改为蓝色;
	body{background-color: red;} 若body和root同时出现，则body属性仅仅是将内容区域改变背景色
	```
	* not	  仅对某个元素使用样式同时排除对它的子元素使用此样式
	```	
		eg: 
			html:
			<div>
				<p>这是一个p标签</p>
				<h1>这是一个h1标签</h1>
				<h2>这是一个h2标签</h2>
			</div>
			css:
			div *:not(h1){
				color: red;
			}
		将div元素中除过h1元素外的其它元素文字颜色改为红色，h1元素颜色不改变。
	```
	* empty	当前元素中内容为空时所使用的样式
	```
	html:
	<table border="1">
		<tr>
			<td>我是第一个内容</td>
			<td>我是第二个内容</td>
		</tr>
		<tr>
			<td>我是第一个内容</td>
			<td></td>
		</tr>
		<tr>
			<td>我是第一个内容</td>
			<td></td>
		</tr>
	</table>
	css:
	:empty{
	background-color: red;
	}
	```
	* target	 对页面中某个target元素指定样式，该样式只在用户点击页面中的超链接，并跳转到target元素后来起作用。
	```
	eg：
	html：
	<a href="#">菜单一</a>|
	<a href="#">菜单二</a>|
	<a href="#">菜单三</a>|
	<a href="#">菜单四</a>
	<div id="div1">
		<h1>菜单一</h1>
		<p>内容</p>
	</div>
	<div id="div1">
		<h1>菜单二</h1>
		<p>内容</p>
	</div>
	<div id="div1">
		<h1>菜单三</h1>
		<p>内容</p>
	</div>
	<div id="div1">
		<h1>菜单四</h1>
		<p>内容</p>
	</div>
	css：
	:target{
	background-color: red;
}
	```





