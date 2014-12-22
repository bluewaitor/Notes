MarkDown学习笔记
==

MarkDown是什么?
--

[MarkDown](http://daringfireball.net/projects/markdown/)是网页上对文字进行赋予样式的方式,你可以控制文件的展示.格式文字为粗体或者斜体,添加图片,创建列表,这都只是MarkDown功能的一小部分.基本上,MarkDown只是正常的文字加上一些非字母的字符,比如`#`(井号)或者`*`(星号).

你可以在github许多地方上使用MarkDown:
* Gists  
* Comments in Issues and Pull Requests  
* Files with the .md or .markdown extension  

1.文本
--
	It's very easy to make some words **bold** and other words *italic* with Markdown. You can even [link to Google!](http://google.com)
It's very easy to make some words **bold** and other words *italic* with Markdown. You can even [link to Google!](http://google.com)

	语法:一个星号*(或者使用_下划线)是斜体,两个星号**(或者使用两个下划线__)是粗体,链接会自动识别,[]方括号是链接的名字,()括号是链接的地址

2.列表
--
	Sometimes you want numbered lists:

	1. One
	2. Two
	3. Three

	Sometimes you want bullet points:
	
	* Start a line with a star
	* Profit!

	Alternatively,
	
	- Dashes work just as well
	- And if you have sub points, put two spaces before the dash or star:
	  - Like this
	  - And this


Sometimes you want numbered lists:

1. One
2. Two
3. Three

Sometimes you want bullet points:

* Start a line with a star
* Profit!

Alternatively,

- Dashes work just as well
- And if you have sub points, put two spaces before the dash or star:
  - Like this
  - And this



	语法:有序列表只要数字后面加个空格,无序列表是*星号后面加一个空格,或者-英文横线加一个空格

3.图片
--
	If you want to embed images, this is how you do it:

	![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)

If you want to embed images, this is how you do it:

![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)

	语法:图片跟链接差不多,在前面加一个英文的!感叹号.

4.标头&引用
--

	# Structured documents

	Sometimes it's useful to have different levels of headings to structure your documents. Start lines with a `#` to create headings. Multiple `##` in a row denote smaller heading sizes.

	### This is a third-tier heading

	You can use  one `#` all the way up to `######` six for different heading sizes.

	If you'd like to quote someone, use the > character before the line:

	> Coffee. The finest organic suspension ever devised... I beat the Borg with it.
	> - Captain Janeway

# Structured documents

Sometimes it's useful to have different levels of headings to structure your documents. Start lines with a `#` to create headings. Multiple `##` in a row denote smaller heading sizes.

### This is a third-tier heading

You can use  one `#` all the way up to `######` six for different heading sizes.

If you'd like to quote someone, use the > character before the line:

> Coffee. The finest organic suspension ever devised... I beat the Borg with it.
> - Captain Janeway

	语法:可以用1~7个星号来代表html中的h1~h7,用`(Tab键上面的按键)来高亮文字,用大于号>来表示引用.

5.代码
--
	There are many different ways to style code with GitHub's markdown. If you have inline code blocks, wrap them in backticks: `var example = true`.  If you've got a longer block of code, you can indent with four spaces:
	
	    if (isAwesome){
	      return true
	    }
	
	GitHub also supports something called code fencing, which allows for multiple lines without indentation:
	
	```
	if (isAwesome){
	  return true
	}
	```
	
	And if you'd like to use syntax highlighting, include the language:
	
	```javascript
	if (isAwesome){
	  return true
	}
	```

There are many different ways to style code with GitHub's markdown. If you have inline code blocks, wrap them in backticks: `var example = true`.  If you've got a longer block of code, you can indent with four spaces:

    if (isAwesome){
      return true
    }

GitHub also supports something called code fencing, which allows for multiple lines without indentation:

```
if (isAwesome){
  return true
}
```

And if you'd like to use syntax highlighting, include the language:

```javascript
if (isAwesome){
  return true
}
```

	语法:在三个\`号后面加上语言,以三个\`号结尾,就可以代码高亮了.

6.另外
--
	GitHub supports many extras in Markdown that help you reference and link to people. If you ever want to direct a comment at someone, you can prefix their name with an @ symbol: Hey @kneath — love your sweater!
	
	But I have to admit, tasks lists are my favorite:
	
	- [x] This is a complete item
	- [ ] This is an incomplete item
	
	And, of course emoji! :sparkles: :camel: :boom:

GitHub supports many extras in Markdown that help you reference and link to people. If you ever want to direct a comment at someone, you can prefix their name with an @ symbol: Hey @kneath — love your sweater!

But I have to admit, tasks lists are my favorite:

- [x] This is a complete item
- [ ] This is an incomplete item

And, of course emoji! :sparkles: :camel: :boom:

	语法:在github上有更多的功能,可以使用@符号,@你想@的人,任务列表[x]表示打勾,还可以使用emoji.


语法指引
==
这是一些你可以在github.com上或者在你自己的文件里可以使用的语法的概览.

###标题
	# This is an <h1> tag
	## This is an <h2> tag
	###### This is an <h6> tag

###强调
	*This text will be italic*
	_This will also be italic_
	
	**This text will be bold**
	__This will also be bold__
	
	*You **can** combine them*

###列表
####无序列表
	* Item 1
	* Item 2
	  * Item 2a
	  * Item 2b
	  
####有序列表
	1. Item 1
	2. Item 2
	3. Item 3
	   * Item 3a
	   * Item 3b

###图片
	![GitHub Logo](/images/logo.png)
	Format: ![Alt Text](url)

###链接
	http://github.com - automatic!
	[GitHub](http://github.com)

###引用
	As Kanye West said:

	> We're living the future so
	> the present is our past.

###内联代码
	I think you should use an
	`<addr>` element here instead.


github风格的MarkDown
==

###语法高亮
 Here’s an example of how you can use syntax highlighting with GitHub Flavored Markdown: 
	```javascript
	function fancyAlert(arg) {
	  if(arg) {
	    $.facebox({div:'#foo'})
	  }
	}
	```
___
 	或者使用4个空格 

###任务列表

	- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
	- [x] list syntax required (any unordered or ordered list supported)
	- [x] this is a complete item
	- [ ] this is an incomplete item

- [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
	- [x] list syntax required (any unordered or ordered list supported)
	- [x] this is a complete item
	- [ ] this is an incomplete item
___
	支持del标签
###表格

You can create tables by assembling a list of words and dividing them with hyphens `-` (for the first row), and then separating each column with a pipe `|`:

	First Header | Second Header
	------------ | -------------
	Content from cell 1 | Content from cell 2
	Content in the first column | Content in the second column

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column


###SHA references
Any reference to a commit’s SHA-1 hash will be automatically converted into a link to that commit on GitHub.

	16c999e8c71134401a78d4d46435517b2271d6ac
	mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
	mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac

###Issue references within a repository
Any number that refers to an Issue or Pull Request will be automatically converted into a link.
	#1
	mojombo#1
	mojombo/github-flavored-markdown#1

###用户名提醒 @mentions
Typing an `@` symbol, followed by a username, will notify that person to come and view the comment. This is called an “@mention”, because you’re mentioning the individual. You can also @mention teams within an organization.

###Automatic linking for URLs
Any URL (like http://www.github.com/) will be automatically converted into a clickable link.

	自动识别链接

###Emoji
GitHub supports emoji! :sparkles: :camel: :boom:

To see a list of every image we support, check out the [Emoji Cheat Sheet](www.emoji-cheat-sheet.com).

	可以在链接的地方找到Emoji的代码

以上翻译自[这里](https://guides.github.com/features/mastering-markdown/ "戳我戳我"),蹩脚英语翻译的实在痛苦T^T

自己使用过程中学到的:
==

1.三个下划线会变成一条分割线
--
	___
___


2.在链接中可以加入鼠标移到链接就弹出提醒
--

	[百度](http://www.baidu.com/ "百度一下,你就知道")

[百度](http://www.baidu.com/ "百度一下,你就知道")

还可以使用下面的方式:
	
	[百度][baidu]
	[baidu]:http://www.baidu.com/ "百度一下,你就知道"

[百度][baidu]
[baidu]:http://www.baidu.com/ "百度一下,你就知道"

	语法:
	[name][id]
	[id]:url "XXX" //这行是不会显示出来的 

3.github可以使用两个~波浪号包裹文字,效果如下
--
	~~被劈了~~
~~被劈了~~



