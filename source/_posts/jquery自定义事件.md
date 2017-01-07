---
title: jQuery自定义事件
date: 2016-12-27 16:19:26
tags:
	- 自定义事件
categories:
	- jQuery
---

> jquery 自定义事件
	
示例：
```
html:
<button class="clickMeBtn">click me</button>
js:
		var clickMeBtn;
		$(document).ready(function(){
			clickMeBtn = $('clickMeBtn');
			clickMeBtn.click(function(){
				var e = jQuery.Event("myEvent");
				clickMeBtn.trigger(e);
			});
			clickMeBtn.on("myEvent", function(event){
				console.log(event);
			});
		});
```


