AngularJS学习笔记
==

AngularJs的四大核心特性
--

1. MVC
2. 模块化和以来注入
3. 双向数据绑定
4. 指令



指令
--

###restrict:

1. E元素(相当于div,form这种)
2. A属性(相当于name)
3. M样式类(相当于样式)
4. C注释(相当于注解)

> 推荐使用元素和属性的方式使用指令
> 当需要创建带有自己的模版的指令时,使用元素名称的方式创建指令
> 当需要为已有的HTML标签增加功能时,使用属性的方式创建指令

###template:

	templateUrl
	templateCache

###replace:
将内容覆盖
	
###transclude:
不覆盖


###compile():
用来对模版自身进行转换

###link():
	
一般用来操作DOM,绑定事件监听器


###scope:
@把当前属性作为字符串传递
=与父scope中的属性进行双向绑定
&传递一个来自父scope的函数,稍后调用




