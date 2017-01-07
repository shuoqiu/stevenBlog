---
title: css 学习笔记（四）
date: 2016-12-13 14:39:27
tags:
	- css
categories:
	- css
---

# css3 学习笔记（四）

> css 的常用操作

1. 对齐操作
	* 使用margin属性进行水平对齐；*eg: margin:0px auto;居中*
	* 使用position属性进行左右对齐；*eg:position:absolute; right:0px;右对齐*<!--more-->
	* 使用float属性进行左右对齐；*eg: float:right; 右对齐*
2. 尺寸操作(常用属性)
	* height： 设置元素高度；
	* line-height： 设置行高；
	* max-height： 设置元素最大高度；
	* max-width： 设置元素最大宽度；
	* width： 设置元素宽度；
	* min-height： 设置元素最小高度；
	* min-width： 设置元素最小宽度；
3. 分类操作（常用属性）
	* clear： 设置一个元素的侧面是否允许其他的浮动元素；
	* cursor： 规定当光标指向某一元素之上时显示的指针类型；*eg：cursor:pointer;小手效果*
	* display： 设置是否显示以及如何显示元素；*eg：display:inline；给li标签这个属性，将li横向展示，通常作为导航栏来用；*
	* float： 定义元素在哪个方向浮动；
	* position： 把元素放置到一个静态的、相对的、绝对的、固定的位置；
	* visibility： 设置元素是否可见或者不可见； 
4. 导航栏
	* 垂直导航栏
		`a:link,a:visited {
		text-decoration: none;/*去掉导航栏的样式，顶端的点去掉*/
}`
`ul {
		list-style-type: none;/*去掉导航栏的样式，顶端的点去掉*/
}`
`a:active,a:hover {
		color: red;/*设置鼠标悬浮上方导航栏的效果*/
}`

	* 水平导航栏

		`li{display: inline;/*将li标签横向水平依次排列*/}`
5. 图片操作


