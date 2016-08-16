---
title: AJAX的XMLHttpRequest对象使用
date: 2016-05-20 10:09:29
tags: 
	- AJAX
	- JS
---
>### 代码如下
>			
>		//1 创建XHR对象
		var xhr = null;
		if(window.XMLHttpRequest){  //新IE、其它浏览器
			xhr = new XMLHttpRequest();  
		}else { //老IE
			xhr = new ActiveXObject('Microsoft.XMLHTTP');
		}
	//2 监听XHR的状态改变
		xhr.onreadystatechange = function(){
		  if(xhr.readyState===4){ //DONE响应消息接收完成
			if(xhr.status===200){
			  console.log('响应接收完成且成功');
			  console.log('响应主体：'+xhr.responseText);
			  doResponse(xhr.responseText);//调用自定义的函数，处理响应数据
			}else {
			  console.log('响应接收完成但不成功');
			  console.log('响应状态码为：'+xhr.status);
			}
		  }
		}
<!-- more -->
	//3 打开连接
		xhr.open('GET','test.php?uname='+n, true);
	//4 发送请求消息
		xhr.send( null );

