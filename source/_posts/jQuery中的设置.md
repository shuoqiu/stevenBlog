---
title: jQuery中的设置
date: 2016-12-27 17:07:17
tags:
	- 设置
categories:
	- jQuery
---

> jQuery中的设置

1. 修改标签中的内容

	```
	eg:
	html: 
	<p id="pid">hello world!</p>
	$("#pid").text("this is a p tag.");
	```
	将p标签中原本的"hello world!"字符换成了："this is a p tag."字符。
<!--more-->
2. 修改整个标签

	```
	eg:
	html:
	<p id="pid">hello world!</p>
	$("#pid").html("<a href="www.baidu.com">百度一下</a>");
	```
	将整个p标签和里面的内容换成了带超链接的：“百度一下”。
3. 修改标签属性
	
	```
	eg:
	html:
	<p><a id="aid" href="www.baidu.com">这是一个超链接</a></p>
	$("#aid").attr({
		"href": "cn.bing.com",
		"title":"超链接"	
	});/*同时修改多个a标签中的属性值。*/
	```
4. 标签中内容的回调

	```
	eg:
	html:
	<p id="pid">hello world！</p>
	$("#pid").text(function(i, ot){
		return "old:"+ot+" new:这是新添加的内容"+(i);
	});
	/*其中参数i为当前元素的下标，ot为即将需要修改的内容。参数i默认为0*/
	```
5. 添加内容、元素
	* append	`在被选中元素的末尾位置添加内容，紧跟元素原本内容之后，不还行`
	* prepend `在被选中元素的开头位置添加内容，后面紧跟元素原本内容，不还行`
	* before `在被选中元素的开头位置添加内容，会换行`
	* after `在被选中元素的末尾位置添加内容，会换行`

	```
	html:
	<p id="pid">这是一个p标签</p>
	$("#pid").append("hello");
	$("#pid").prepend("p标签");
	$("#pid").before("hi~");
	$("#pid").after("world!");
	
	用html、jQuery、DOM来添加元素或内容：
	html：
	var text1="<p>hello</p>"; 
	jQuery:
	var text2=$("<p></p>").text("world"); 
	DOM:
	var text3=document.getElment("p");
	text3.innerHTML="I love u";
	
	$("boday").append(text1, text2, text3);/*将增加的三个内容放到body中来*/
	```


