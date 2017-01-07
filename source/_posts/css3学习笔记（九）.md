---
title: css 学习笔记（九）
date: 2016-12-21 16:50:23
tags:
	- css
categories:
	- css
---

> css3 学习笔记（九）
	
1. UI元素伪类选择器
	
	在css3的选择器中，除了结构性伪类选择器外，还有一种UI元素状态伪类选择器。这些选择器的共同特点是：制定的样式只有当元素处于某种状态时才起作用，在默认状态下不起作用。<!--more-->
	在css3中，共有17种UI元素状态伪类选择器，分别是E:hover、E:active、E:focus、E:disabled、E:read-only、E:checked、E:default、E:indeterminate、E::selection、E:invalid、E:valid、E:required、E:optional、E:in-range.

```
eg: 
html:
<input type="text" name="name">
<input type="text" age="age">

css:
input[type="text"]:hover{/*当鼠标悬停在输入框上方时执行*/
	background-color: red;
}
input[type="text"]:focus{/*当输入框获取到焦点时执行*/
	background-color: green;
}
input[type="text"]:active{/*当鼠标在输入框内按下不放之后执行*/
	background-color: blue;
}

eg:
html:
	 <input type="radio" id="radio1" name="radio" onchange="">可用
	 <input type="radio" id="radio2" name="radio" onchange="">不可用
	 <input type="text" id="text" disabled>
js:
	 <script type="text/javascript">
	 	function radio_change(){
	 		var radio1 = document.getElementById("radio1");
		 	var radio2 = document.getElementById("radio2");
		 	var text = document.getElementById("text");
		 	if (radio1.checked) {
		 		text.disabled="";
		 	}else{
		 		text.value="";
		 		text.disabled="disabled";
		 	}	
	 	}
	 </script>
css:
	input[type="text"]:enabled{
		background-color: red;
	}
	input[type="text"]:disable{
		background-color: blue;
	}
```

2. 通用兄弟元素选择器
	
	用来指定位于同一父元素之中的某个元素之后的所有其他某个种类的兄弟元素所使用的样式。
	
```
eg:
html:
	 <div>
		 	<div>
		 		<p>拉萨的加夫里什的肌肤来说</p>
		 		<p>sldfjlsdjfls发牢骚的加夫里什的</p>
		 	</div>
		 	<p>falsdjflsdjfsjkdflsdkf</p>
		 	<p>ljsdflksjf法律监督撒了福建省地方</p>
		 	<p>flasjdflsjadfldsjfl来得及发来的撒酒疯</p>
	 </div>
css:
	div ~ p{/*此处div为子集中的div*/
	background-color: red;}
```	

