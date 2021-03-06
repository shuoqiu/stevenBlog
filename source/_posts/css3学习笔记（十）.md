---
title: css3 技巧总结
date: 2016-12-28 14:09:11
comments: false
tags:
	- css
categories:
	- css
---

### 左右结构，左侧固定右侧自适应
示例:
原理：`container`元素作为父元素，其中包括左侧的`slider`和右侧的`content`。`slider`固定宽度，而`content`元素使用相对定位，相对于`container`元素享有偏移一定的距离，这个距离与`slider`元素的宽度恰好相同，而且`content`元素的`right`为0，这样`content`元素的右边距与父元素`container`在一致的位置，好似“自适应”一般。
<!--more-->
### 响应式设计，根据宽度（变化的）设置高度
示例:
在响应式设计中，设备的宽度是不确定的，而有时需要根据宽度来设置高度，如上面的例子，想要一个与宽度相同的高度的div，即一个正方形。 
原理：`padding-top`使用百分比时，计算的是父元素的宽度。利用这一点，使用`padding-top:100%`设置子元素`std-rect`，然后给子元素的子元素`content`设置一个负数的`margin-top:-100%`，也使用百分比，这样，`content`元素里面的内容就会出现在正方形中。为了使得内容不会撑开div，将`content`相对于`std-rect`定位，并设置`std-rect`为`overflow:hidden`。在上面的例子中，还有一个`clearfix`的技巧值得记住。

另外，CSS3的`calc()`好像也能解决这种问题。

