---
title: css 学习笔记（二）
date: 2016-12-9 12:03:39
tags:
	- css
categories:
	- css
---

# css3 学习笔记（二）

> css 的定位

css的定位机制分为：普通流、浮动和绝对布局；
css的定位属性包括：

* position 属性： 把元素放在一个静态的、相对的、绝对的或固定的位置中；<!--more-->
	* static 	//静态布局
	* relative //相对布局
	* absolute //绝对布局
	* fixed	//固定布局
* top 属性： 元素向上的偏移量；
* left 属性： 元素向左的偏移量；
* right 属性： 元素向右的偏移量；
* bottom 属性： 元素向下的偏移量；
* overflow 属性： 设置元素溢出其区域发生的事情；
* clip 属性： 设置元素显示的形状；
* vertical-align 属性： 设置元素垂直对齐方式；
* z-index 属性： 设置元素的堆叠顺序；//数值越大，呈现的优先级越高； 

> css 的浮动

1. 浮动 ——> float属性可用的值：
	* left	元素向左浮动
	* right	元素向右浮动
	* none	元素不浮动
	* inherit	元素从父级继承浮动属性
2. clear 用来去掉浮动属性 ——> clear属性包括的值：
	* left	去掉元素向左浮动
	* right	去掉元素向右浮动
	* both	左右两侧均去掉浮动
	* inherit	从父级继承来clear的值

