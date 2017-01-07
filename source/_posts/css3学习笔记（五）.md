---
title: css 学习笔记（五）
date: 2016-12-13 20:56:08
tags:
	- css
categories:
	- css
---

> css3 学习笔记（五）
	
1. 元素选择器
	`最常见的选择器，是基本选择器；*eg： span{}或者body{}等等`
2. 选择器分组
	`span,p{} 等等这种形式的写法； *{}，这是一个通配符的写法；`<!--more-->
3. 类选择器
	`写法为： .className{}，以点开头。`
	* 类选择器可以结合元素选择器来使用
		`写法为： span.className{}`
	* 可以写成多类选择器
		```html:
		<div class="class1 class2">this is a word.</div>
		css:
		.class1.class2{
			color: red;
		}```
4. ID选择器
	`写法为： #idName{}`
	* 类选择器和ID选择器区别：
		1. ID只可以在文档中使用一次，而类选择器可以使用多次；
		2. ID选择器不可以结合使用，而类选择器可以；
		3. 当使用js的时候，需要用到ID；
5. 属性选择器
	```
	html: <span title="">hello world.</span>
	css: [title]{color: red;}
	```
	* 根据具体属性值选择
		`eg：css: a[href="www.baidu.com"]{}`
	* 属性和属性值必须完全匹配
	* 根据部分属性值选择
		```eg:
		html:
		<div title="tile">hello world</div>
		<div title="title">hello world</div>
		<div title="tle">hello world</div>
		<div title="tit">hello world</div>
		<div title="title name">hello world</div>
		css:
		[title~="title"]{color: red;}
		```
6. 后代选择器
	`eg: html: <div>this <strong>is <i>a</i></strong> word.</div>; css: div strong i{color: red;}`
7. 子元素选择器
	`eg: html:<p>this <strong>is a</strong> word.</p>; css: p>strong{color:red;}`
8. 相邻兄弟选择器
	* 可选择紧接在另一个元素后的元素，且二者有相同父元素；
		```
		eg: html:
		<div>
		<ul>
			<li>item</li>
			<li>item1</li>
			<li>item2</li>
		</ul>
		</div>
		css:
		li+li {color: red;}
		仅仅item1和item2会有字体变红效果；
		```


