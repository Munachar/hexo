---
title: Markdown语法学习
date: 2016-06-13 14:15:33
tags:
	- study
---
### 标题
	
	# 这是 H1 #

	## 这是 H2 ##

	### 这是 H3 ######

### 引用块 ###

	>This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
	consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
	>>Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
	> 
	> 1.   这是第一行列表项。
	> 2.   这是第二行列表项。
	> 
	> 给出一些例子代码：
	> 
	>     return shell_exec("echo $input | $markdown_script");

>This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
>>Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
> 
> 1.   这是第一行列表项。
> 2.   这是第二行列表项。
> 
> 给出一些例子代码：
> 
>     return shell_exec("echo $input | $markdown_script");

<!-- more -->

### 列表

	>> * Red
	* Green
	* Blue
	>> + Tom
	+ Jack 
	+ Jerry
	>> + 张三丰
	+ 张翠山
	+ 张无忌
	> 有序列表 1.
	>> 1.  Bird
	2.  McHale
	3.  Parish

	> 1.  This is a list item with two paragraphs. Lorem ipsum dolor
		sit amet, consectetuer adipiscing elit. Aliquam hendrerit
		mi posuere lectus.

	>   Vestibulum enim wisi, viverra nec, fringilla in, laoreet
		vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
		sit amet velit.

	> 2.  Suspendisse id sem consectetuer libero luctus adipiscing.
	1986\. What a great season.

> 无序列表 *,+,-
>> * Red
* Green
* Blue
>> + Tom
+ Jack 
+ Jerry
>> + 张三丰
+ 张翠山
+ 张无忌
> 有序列表 1.
>> 1.  Bird
2.  McHale
3.  Parish

> 1.  This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

>   Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

> 2.  Suspendisse id sem consectetuer libero luctus adipiscing.
1986\. What a great season.

### 代码区块
这是一个普通的段落：

	这是一个代码区块
	<div class="footer">
        &copy; 2004 Foo Corporation
    </div>

### 分割线
<p>你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：</p>

	* * *

	***
	
	*****

	- - -

	---------------------------------------
<hr/>

<h3>区段元素</h3>
> #### 链接
<p>Markdown 支持两种形式的链接语法： 行内式和参考式两种形式。
不管是哪一种，链接文字都是用 [方括号] 来标记。
要建立一个行内式的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可，例如：</p>
>
> 	This is [an example](http://example.com/ "Title") inline link.
> 
> 	[This link](http://example.net/) has no title attribute.
> 会产生
> This is [an example](https://munachar.github.io/404.html "Title") inline link.
> 
> [This link](http://www.baidu.com/) has no title attribute.
> 下面是一个参考式链接的范例：
>
> 	 I get 10 times more traffic from [Google] [1] than from[Yahoo] [2] or [MSN] [3].
>
>	  	[1]: http://google.com/        "Google"
>	  	[2]: http://search.yahoo.com/  "Yahoo Search"
>	  	[3]: http://search.msn.com/    "MSN Search" 
> 或者：
>
>	 I get 10 times more traffic from [Google][] than from[Yahoo][] or [MSN][].
>
>	  	[google]: http://google.com/        "Google"
>	  	[yahoo]:  http://search.yahoo.com/  "Yahoo Search"
>	  	[msn]:    http://search.msn.com/    "MSN Search"br
> #### 强调
<p>Markdown 使用星号（\*）和底线（\_）作为标记强调字词的符号，被 \* 或 \_ 包围的字词会被转成用 <\em\> 标签包围，用两个 \* 或 \_ 包起来的话，则会被转成 <strong>，例如：</p>
>
>	 *single asterisks*
>
>	 _single underscores_
>
>	 **double asterisks**
>
>	 __double underscores__
>效果如下：
> *single asterisks*
>
> _single underscores_
>
> **double asterisks**
>
> __double underscores__
> #### 代码
如果要标记一小段行内代码，你可以用反引号把它包起来（`），例如：
>
>	 Use the `printf()` function.
效果如下：
> Use the `printf()` function.
> A single backtick in a code span: `` ` ``
>
> A backtick-delimited string in a code span: `` `<foo>` ``
> #### 图片
Markdown 使用一种和链接很相似的语法来标记图片，同样也允许两种样式： 行内式和参考式。

>行内式的图片语法看起来像是：
>
>	 ![Alt text](/path/to/img.jpg)
>
>	 ![Alt text](/path/to/img.jpg "Optional title")
>详细叙述如下：
>* 一个惊叹号 !
>* 接着一个方括号，里面放上图片的替代文字
>* 接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上 选择性的 'title' 文字。

>参考式的图片语法则长得像这样：
>
<pre>![Alt text][id]</pre>
>
>「id」是图片参考的名称，图片参考的定义方式则和连结参考一样：
>
>	 [id]: url/to/image  "Optional title attribute"
>到目前为止， Markdown 还没有办法指定图片的宽高，如果你需要的话，你可以使用普通的 <img> 标签。

### 其他
> #### 自动链接
>
>Markdown 支持以比较简短的自动链接形式来处理网址和电子邮件信箱，只要是用方括号包起来， Markdown 就会自动把它转成链接。一般网址的链接文字就和链接地址一样，例如：
>
>	 <http://example.com/>
Markdown 会转为：
>
>	 <a href="http://example.com/">http://example.com/</a>
邮址的自动链接也很类似，只是 Markdown 会先做一个编码转换的过程，把文字字符转成 16 进位码的 HTML 实体，这样的格式可以糊弄一些不好的邮址收集机器人，例如：
>
>	 <address@example.com>
Markdown 会转成：
>
> 	 <a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;
	&#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;
	&#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;
	&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a>
在浏览器里面，这段字串（其实是 <a href="mailto:address@example.com">address@example.com</a>）会变成一个可以点击的「address@example.com」链接。

（这种作法虽然可以糊弄不少的机器人，但并不能全部挡下来，不过总比什么都不做好些。不管怎样，公开你的信箱终究会引来广告信件的。）

> #### 反斜杠
>
>Markdown 可以利用反斜杠来插入一些在语法中有其它意义的符号，例如：如果你想要用星号加在文字旁边的方式来做出强调效果（但不用 <em> 标签），你可以在星号的前面加上反斜杠：
>
>	 \*literal asterisks\*
>Markdown 支持以下这些符号前面加上反斜杠来帮助插入普通的符号：
>
>	 \   反斜线
	`   反引号
	*   星号
	_   底线
	{}  花括号
	[]  方括号
	()  括弧
	#   井字号
	+   加号
	-   减号
	.   英文句点
	!   惊叹号

