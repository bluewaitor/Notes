JQuery
==

插件模版:
--

```javascript
;(function($){
	$.fn.plugin=function(){
		var defaults = {
			//各种参数,各种属性
		}
		var options = $.extend({},defaults,options);
		this.each(function(){
			//实现的功能
		});

		return this;
	}
})(jQuery);


```