---
title: jQuery中的捕获
date: 2016-12-27 16:49:32
tags: 
	- 捕获
categories:
	- jQuery
---

> jQuery中的捕获

1. 获取标签中的值
	eg： 获取p标签中的内容<!--more-->
	
	```
	<p id="pid">this is a p tag.<a href="www.baidu.com">百度</a></p>
	1) $("#pid").text();   
	2) $("#pid").html();
	```
	
	区别：text()方法获取到的p元素中包含的所有值，不会有标签符号出现；
		  html()方法获取到的p元素中包含的所有值，还包括标签符号；
2. 获取输入框中的值
	eg:获取输入框中填写的内容  	
	```
	<p><input type="text" id="it" value="this is a input tags."></p>
	$("#it").val();  获取到input中的值，为 this is a input tags.
	```
3. 获取标签中的属性值
	eg： 获取a标签中的属性值
	```
	<p><a id="aid" href="www.baidu.com">百度一下</a></p>
	$("#aid").attr("href");  获取某个标签指定的某个属性。
	```	


