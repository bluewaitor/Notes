JavaScript权威指南读书笔记
==

第2章 词法结构
--
1. JavaScript是区分大小写的,而HTML则没有,所以onclick在HTML中可以写成onClick,而在JavaScript中则必须写成小写的onclick
2. JavaScript可以转移Unicode,格式为"\uxxxx",x是16进制
3. 行注释//,段注释/**/
4. 标识符必须以字母,下划线_,或者美元符$开始的,后面的字符可以是字母,数字,下划线或美元符(数字不准开头)
5. 保留字,就不说了.
6. 可选的分号,总之,不是刻意而为之的话,是不会出现错误的,除非标新立异,这就看代码风格了,分号都写上去就是了.


第3章 类型,值和变量
--
1. JavaScript的数据类型分为两类:原始类型(primitive type)和对象类型(object type).
		原始类型有:数字,字符串,布尔值,null(空),undefined(未定义) 后面两个比较特殊

		对象类型有:对象是属性的集合(每个属性都是名/值对,值可以是原始值,也可以是对象),全局对象(global object),特殊对象-数组(array),特殊对象-函数
2. 可变类型和不可变类型
3. 类型转换自由
4. 16进制0x或0X打头,8进制0打头,最好不用8进制
5. 小数语法表示:[digits][.digits][(E|e)[(+|-)]digits]
6. 转义\
7. 字符串是固定不变的,执行了某些字符串方法之后是返回新字符串
8. 布尔值true和false,`undefined,null,0,-0,NaN,""(空字符串)`都会被转换成false,其他的都是true,&&(and),||(or),!(not).
9. null表示一个特殊值,常用来描述"空值",对null进行typeof运算,返回字符串object,可以将null看成一个特殊的对象值,及"非对象". undefined表示更深层次的"空值",它是变量的一种取值,表明变量没有初始化,undefined是预定义的全局变量,它不是关键字,它的值就是"未定义".(要用===严格区分它们俩)
10. 存取字符串,数字或布尔值的属性时创建的临时对象乘坐包装对象.由于字符串,数字和布尔值的属性都是只读的,并且不能给它们定义新属性,因此你需要明白它们是有别于对象的.
11. 不可变的原始值,可变的对象引用
12. 类型转换,JavaScript会自行转换类型,转换为数字(如果转换结果无意义则返回NaN,Not a Number),null,undefined转换为对象会报TypeError.
13. toString(radix),可以将数字转换为对应进制的字符串
14. toFixed,toExponential,toPrecision将小数转换为格式化字符串.
15. parseInt,parseFloat,将字符串转换为数字,parseInt可以接收第二个参数,表示进制
16. 变量声明用var(严格模式),如果var声明没有赋初始值,则初始值为undefined,虽然不声明的话JavaScript会当成全局变量,但是这样做会造成很多bug,所以要养成用var声明的习惯.
17. 变量作用域(scope),局部变量的作用域高于同名的全局变量.
18. 函数作用域,变量在函数里面声明,在整个函数里面都可以访问.声明提前,所有的声明都会被提前,但是初始化不会.
19. 用var声明的全局变量不可删除,而没用var则可以删除(用delete).
20. `作用域链`,全局变量在程序中始终都是有定义的.局部变量在声明它的函数体内以及其所嵌套的函数内始终是有定义的.


第4章 表达式和运算符
--

1. 原始表达式
2. 对象和数组的初始化表达
3. 函数定义表达式,即var fn = function(x){return x*x};表达式的值就是这个函数
4. 属性访问表达式,即用点(.)或者([])来访问属性
5. 调用表达式,即调用函数或者方法
6. 对象创建表达式,即用new创建对象,如果不用参数,对象的()括号是可以去掉的
7. 对于p和q取任意值,这两个等式都永远成立,!(p&&q)===!p||!q,!(p||q)===!p&&!q
8. eval,全局用的比较多
9. 三元运算符,?:
10. typeof
11. delete,通过var声明的变量不能删除
12. 逗号运算符,(i=0,j=1,k=2;)返回2

第5章 语句
--
1. 表达式语句
2. 复合语句和空语句,复合语句可以用{}花括号括起来,空语句则是用;分号结尾,比如空循环,空if.
3. 声明语句,var和function都是声明语句.
    * var在函数体内,就是定义一个局部变量,在顶层代码使用,就是全局变量,var声明的变量无法通过delete删除,如果没有初始化,则值为undefined.
    * function可以将表达式赋值给一个变量,也可以是含有变量名的语句.语法:
    		function funcname([arg1 [,arg2 [...,argn]]]){
				statements
			}
4. 条件语句,if,switch
5. 循环,while,do/while,for,for/in
6. 跳转,添加标签,identifier:statement,break,continue,return,throw,try/catch/finally
7. 其他语句类型,with,debugger,use strict(严格模式)

第6章 对象
--
1. 创建对象
 	`可以通过对象直接量,关键字new和Object.create()函数来创建对象.`
	+ 对象直接量,对象直接量是由若干 名/值 对组成的映射表,名/值 对中间用冒号分隔,名/值 对之间用逗号分隔,整个映射表用花括号括起来,其实就是json.
			如果在一个重复调用的函数中的循环体内使用了对象直接量,它将创建很多新对象,并且每次创建的对象的属性值也有可能不同.
	+ new关键字.new运算符创建并初始化一个新对象,关键字new后面跟随一个函数调用,这里的函数称作构造函数.
	+ 原型,Object.prototype.
	+ Object.create(),传入所需的原型对象即可.

2. 属性的查询和设置
	1. 在表达式右边的时候用点或者[]方括号来访问值
	2. 在表达式左边的时候用点或者[]方括号来设置值
	3. 用[]来访问值的时候很方便,可以配合for/in.
	4. JavaScript具有"自有属性",也有一些属性是从原型对象继承而来的.
	5. 属性访问错误

3. 删除属性,delete知识断开属性和宿主对象的联系,而不会去操作属性中的属性.delete运算符只能删除自有属性,不能删除继承属性.
4. 检测属性,判断某个属性是否存在于某个对象当中,可以通过运算符,hasOwnProperty()和propertyIsEnumerable()方法来检测.还有一种更简便的方法,那就是使用"!=="判断一个属性是否是undefined.
5. 枚举属性,对象继承的内置方法是不可枚举的,但是在代码中给对象添加的属性都是可以枚举的.枚举属性可通过for/in来访问
6. 属性getter和setter.get或者set跟一个函数名,比如get r(){};
7. 属性的特性.Object.getOwnPropertyDescriptor(),Object.defineProperty(),Object.defineProperties()
8. 对象的三个属性
	1. 原型属性.可以通过p.isPrototypeOf(o)来检测p是否是o的原型.
	2. 类属性.
			function classof(o){
				if(o === null) return "Null";
				if(o === undefined) return "Undefined";
				return Object.prototype.toString.call(o).slice(8,-1);
			}
		可以通过上面这个函数检测对象的类.
	3. 可扩展性.检测是否有扩展性Object.isExtensible(o),Object.preventExtensions(o)转为不可扩展,只影响到对象本身.Object.seal(o),除了将对象设置为不可扩展,还可以将对象所有自有属性设置为不可配置.可以通过Object.isSealed(o)来检测是否封闭.Object.freeze(o),更为严格的锁定对象--"冻结",除了seal的作用,还将自有的所有数据属性设置为只读.可以通过Object.isFrozen(o)来检测是否被冻结.会返回传入的参数,所以可以嵌套使用.
9. 序列化对象.JSON.stringify(),JSON.parse()
10. 对象方法.
	1. toString()方法,没有参数,将会返回调用这个方法对象值的字符串.
	2. toLocaleString()方法,Date和Number类对toLocaleString方法做了定制.
	3. toJSON()方法
	4. valueOf()方法.当JavaScript需要将对象转换为某种原始值而非字符串的时候才会调用它,尤其是转换为数字的时候

第7章 数组
--

1. 创建数组.直接用[]创建或者new Array()
2. 数组元素的读和写.arr[索引或者属性名].
3. 稀疏数组.
4. 数组长度.length属性值.可以通过设置length的值来删除数组的元素.
5. 数组元素的添加和删除.
	1. push()方法向数组末尾增加一个或多个元素.unshift()在首部插入一个元素,并将数组下标往后移.
	2. delete删除数组某个元素.pop()删除一个元素并返回该元素.shift()方法和unshitf()方法相反,删除首部的值并将数组的下标往前移.	
6. 数组遍历.
	1. for.遍历的时候记得处理不存在的元素,特别是稀疏数组.
	2. for/in.
	3. arr.forEach(function(x){dosomething with x in arr}).
7. 多维数组
8. 数组方法.
	1. join().将数组中所有元素都转化为字符串并连接在一起,可以指定一个可选的字符串在生成的字符串中分隔数组的各个元素,如果不指定分隔符,默认使用逗号.Array.join()方法是String.split()的逆操作
	2. reverse().将数组的元素颠倒顺序.
	3. sort().将数组中的元素排序并返回排序后的数组.可以传入一个函数,函数返回复数,则该元素排在前面,返回0,则无关紧要,返回整数,排在后面.
	4. concat().创建并返回一个新数组,会加上传入的参数.
	5. slice().返回指定数组的一个片段或子数组.跟python中的切片差不多.
	6. splice().在数组中插入或删除元素的通用方法.splice()会修改调用的数组.第一个参数指定删除或者插入的位置,第二个参数为删除的个数,其后的为插入的元素.
	7. push()和pop().push返回数组的个数
	8. unshift()和shift().在头部插入或者删除元素
	9. toString()和toLocaleString().
9. ECMAScript5中的数组方法
	1. forEach().传递一个函数作为forEach()的第一个参数,函数可以有三个参数:数组元素,元素索引,数组本身.
	2. map().调用数组的每个元素传递给指定的函数,并返回一个数组,它包含函数的返回值.简而言之就是返回一个新数组,值是通过原来的数组算出来的.
	3. filter().返回的数组元素是数组的一个子集,传入的函数是一个过滤条件,返回true或false.filter()会跳过稀疏数组中缺少的元素.
	4. every()和some(),返回true或false.
	5. reduce()和reduceRight(),reduce从左到右,而reduceRight从右到左.
	6. indexOf()和lastIndexOf(),indexOf()从头至尾搜索,lastIndexOf()从尾至头搜索.查找一个元素(值)返回它的下标.
10. 数组类型.
	Array.isArray([])//true
	Array.isArray({})//false
11. 类数组对象.
12. 作为数组的字符串.可以通过下标的方式来访问字符串,var s = "test",s.charAt(0)相当于s[0].

## 第8章

1. 函数定义.function \[funcname\](\[parameter\]){}\[('立即调用')\]
2. 函数调用.
	1. 作为函数
	2. 作为方法
	3. 作为构造函数
	4. 通过它们的call()和apply()方法间接调用
3. 函数的实参和形参
	1. 可选形参. a = a || [];
	2. 可变长的实参列表.可以通过arguments[index]来获取传入的实参
4. 作为值的函数
5. 作为命名空间的函数.定义一个函数,将所有变量函数都放在里面,然后立即执行,jQuery就是这样的.
6. 闭包.就是将函数内定义的变量通过一个函数return回来.
7. 函数属性,方法和构造函数
	1. length属性,函数的length属性代表函数的实参数量.
	2. prototype属性.这个属性指向一个对象的引用,这个对象称做"原型对象",每个函数都包含不同的原型对象.
	3. call()方法和apply()方法.
			要想以对象o的方法来调用函数f(),可以这样使用call()和apply()
			f.call(o);
			f.apply(o);
			相当于下面的代码:
			o.m = f;
			o.m();
			delete o.m;
		call()第一个参数是对象,接下来是函数的参数列表.
		apply()第一个参数是对象,接下来是一个参数数组.
	4. bind()方法. f.bind(o);将函数f绑定到o对象上面.
	5. toString()方法.
	6. Function()构造函数.
	7. 可调用的对象.

8. 函数式编程.
	1. 使用函数处理数组
	2. 高阶函数
	3. 不完全函数
	4. 记忆.在函数内定义一个对象,用来缓存,使用闭包.

## 第9章

1. 类和原型
2. 类和构造函数
	1. 构造函数和类的标识.prototype.通过instanceof来检验是不是属于某个类,instanceof是检测Class.prototype
	2. constructor属性.
3. JavaScript中Java式的类继承.
4. 类的扩充.可以在原型上Object.prototype上扩充属性和方法.
5. 类和类型.
	1. instanceof运算符. o instanceof c. o是对象,c是类.
	2. constructor属性.
	3. 构造函数的名称.
	4. 鸭式辩型.
6. JavaScript中的面向对象技术.
7. 子类.
8. ECMAScript5中的类
9. 模块

## 第10章
