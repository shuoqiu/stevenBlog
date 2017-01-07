---
title: css 学习笔记（六）
date: 2016-12-18 19:27:55
tags:
	- css
categories:
	- css
---

> css3 学习笔记（六）


### 一、2D、3D的转换

1. 2D的转换方法包括：
	* translate(x轴移动到的位置坐标，y轴移动到的位置坐标)  移动  
	`eg: transform:translate(100px, 100px) `
	* rotate(旋转的度数)  旋转   
	`eg: transform:rotate(180deg)  从原来的位置旋转180度`
	* scale(宽度缩放倍数， 高度缩放倍数)   缩放  <!--more-->
	`eg: transform:scale(1, 2) 宽度缩放为1倍，高度缩放为2倍；`
	* skew(围绕x轴旋转角度， 围绕y轴旋转的角度)  倾斜
	`eg: transform:skew(30deg, 50deg) 围绕x轴旋转30度，围绕y轴旋转50度`
	* matrix()  矩阵
	 
	[参考一篇讲解css矩阵的文章](http://www.zhangxinxu.com/wordpress/2012/06/css3-transform-matrix-%E7%9F%A9%E9%98%B5/)
	
2. 3D的转换方法包括：
	* rotateX()
	* rotateY()
	
```
	ps： 各个浏览器的适配
	-webkit-transform:translate(x, y);  /*safari chrome*/
	-ms-transform:translate(x, y);  /*IE*/
	-o-transform:translate(x, y);  /*opera*/
	-moz-transform:translate(x, y);  /*Firefox*/
```
	
### 二、css 的过渡

css3 的过渡是元素从一种样式改变为另一种样式：
	
* 动画效果的css
* 动画执行的时间

![过渡](http://oalppxaqn.bkt.clouddn.com/%E8%BF%87%E6%B8%A1.jpeg)

transition属性    设置四个过渡属性
transition-property属性  过渡的名称
transition-duration属性  过渡效果花费的时间
transition-timing-function属性   过渡效果的时间曲线
transition-delay属性		过渡效果延时开始的时间
```
div{
	width: 100px;
	height: 100px;
	background-color: green;
	transition: width 2s, height 2s, transform 2s;
	-webkit-transition: width 2s, height 2s, transform 2s;
	transition-delay: 2s;
}

div:hover{
	width: 200px;
	height: 200px;
	transform: rotate(360deg);
	-webkit-transform: rotate(360deg);
}
```

###  三、css3 的动画

css3可以用来创建动画，css3动画需要遵循@keyframes规则，此规则包括：

* 规定动画的时常
* 规定动画的名称

```
div{
	width: 100px;
	height: 100px;
	background-color: red;
	position: relative;
	animation: anim 2s infinite alternate;/*动画效果持续2s，反复执行*/
	-webkit-animation: anim 2s;
}
@keyframes anim{
	0%{
		background-color: red;
		left: 0px;
		top: 0px;
	}
	25%{
		background-color: green;
		left: 200px;
		top: 0px;
	}
	50%{
		background-color: blue;
		left: 200px;
		top: 200px;
	}
	75%{
		background-color: yellow;
		left: 0px;
		top: 200px;
	}
	100%{
		background-color: gray;
		left: 0px;
		top: 0px;
	}
}
@-webkit-keyframes anim{
	0%{
		background-color: red;
		left: 0px;
		top: 0px;
	}
	25%{
		background-color: green;
		left: 200px;
		top: 0px;
	}
	50%{
		background-color: blue;
		left: 200px;
		top: 200px;
	}
	75%{
		background-color: yellow;
		left: 0px;
		top: 200px;
	}
	100%{
		background-color: gray;
		left: 0px;
		top: 0px;
	}	
}
```

### 四、css3 的分列

在css3中可以通过创建多列来对**文本或者区域**进行布局，多列的属性包括：

   * column-count  分列的数量
   * column-gap	  每一列之间间隔的距离
   * column-rule	  每一列之间间隔的线以及线的颜色

```
html:
<div>包含好多好多内容，超级多内容</div>
css:
div{
	column-count: 4;/*分为4列*/
	-webkit-column-count: 4;
	column-gap: 30px;/*每列之间间隔30px*/
	-webkit-column-gap: 30px;
	column-rule: 5px outset red;/*每列间隔间由5像素红色隔开*/
	-webkit-column-rule: 5px outset red;
}
```

### 五、css3 实现瀑布流效果

```
html:
<div class="container">
		<div><img src="images/1.png"></div>
		<div><img src="images/2.png"></div>
		<div><img src="images/3.png"></div>
		<div><img src="images/4.png"></div>
		<div><img src="images/5.png"></div>
		<div><img src="images/6.png"></div>
		<div><img src="images/7.png"></div>	
		<div><img src="images/1.png"></div>
		<div><img src="images/2.png"></div>
		<div><img src="images/3.png"></div>
		<div><img src="images/4.png"></div>
		<div><img src="images/5.png"></div>
		<div><img src="images/6.png"></div>
		<div><img src="images/7.png"></div>	
		<div><img src="images/1.png"></div>
		<div><img src="images/2.png"></div>
		<div><img src="images/3.png"></div>
		<div><img src="images/4.png"></div>
		<div><img src="images/5.png"></div>
		<div><img src="images/6.png"></div>
		<div><img src="images/7.png"></div>	
		<div><img src="images/1.png"></div>
		<div><img src="images/2.png"></div>
		<div><img src="images/3.png"></div>
		<div><img src="images/4.png"></div>
		<div><img src="images/5.png"></div>
		<div><img src="images/6.png"></div>
		<div><img src="images/7.png"></div>		
	</div>
	
css:	
.container{
column-width: 250px;
-webkit-column-width: 250px;
column-gap: 10px;
-webkit-column-gap: 10px;
}
.container div{
width: 250px;
margin: 5px;
}
```


	
	

		
 

