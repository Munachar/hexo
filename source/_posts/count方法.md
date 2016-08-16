---
title: 面试题
date: 2016-06-23 14:11:29
categories: Testing
tags:
	- 算法
	- JS
---

### count方法
封装一个count方法，能实现如此调用：count(a)(b)(c)(d)(e)… 并且返回的值为参数连乘的结果，即abcde*…。如count(1)(3)(7) 得到21

	function count(x){
		var fn = function(y){
			return count(x*y);
		}
		fn.toString = function(){
			return x;
		};
		return fn;
	};