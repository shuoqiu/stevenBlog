---
title: css 学习笔记（三）
date: 2016-12-11 14:08:35
tags:
	- css
categories:
	- css
---

# css3 学习笔记（三）

> 标准盒子模型

盒子模型的内容范围包括：margin,border,padding,content;<!--more-->
![css 盒子模型](http://oalppxaqn.bkt.clouddn.com/css%20%E7%9B%92%E5%AD%90%E6%A8%A1%E5%9E%8B.png)

1. 内边距： 内边距在content外，边框内 ——> 属性包括：
	* padding：	设置所有边距
	* padding-bottom： 设置底边距
	* padding-top： 设置顶部边距
	* padding-left： 设置左边距
	* padding-right： 设置右边距

2. 边框： 边框的样式 border-style ——> 定义了10个不同的非继承样式，包括none；
	* 边框的样式： border-style
	* 边框的单边样式：
		* border-top-style;
		* border-left-style;
		* border-right-style;
		* border-bottom-style;
	* 边框的宽度： border-width
	* 边框单边的宽度：
		* border-top-width
		* border-left-width
		* border-right-width
		* border-bottom-width
	* 边框的颜色：border-color
	* 边框单边的颜色：
		* border-top-color
		* border-left-color
		* border-right-color
		* border-bottom-color
	* css3 所提供的边框：
		* border-radius： 圆角边框 `eg： border-radius:10px;`
		* box-shadow： 边框阴影 `eg:box-shadow: 5px 5px 5px #fff;//参数1：向右偏移；参数2：向下偏移；参数3:透明度；参数4:阴影颜色`
		* border-image： 边框图片
	
	
3. 外边距: 围绕在内容边框的区域就是外边距，外边距默认为透明区域；
	**外边距接受任何长度单位，百分数值**
* 外边距常用属性：
	* margin： 设置所有边距
	* margin-top： 设置顶边距
	* margin-bottom： 设置底边距
	* margin-left： 设置左边距
	* margin-right： 设置右边距
	
4. 外边距合并
![css 外边距合并](http://oalppxaqn.bkt.clouddn.com/css%20%E5%A4%96%E8%BE%B9%E8%B7%9D%E5%90%88%E5%B9%B6.png)
有两个元素，第一个元素在上方，距离下方外边距50px，第二个元素在第一个元素下方，距离上方外边距100px，则外边距叠加之后得道的两个元素的外边距为100px；因为外边距的叠加遵循**<span style="color:red">少服从多</span>**的原则;
	
		

	
	



