# 原始类型

在JS中，原始类型总共有6种，分别是`string`、`number`、`boolean`、`null`、`undefined`、`symbol`(ES2015新增的类型)。

## String

String类型有3种表达方式，分别是使用成对的`(')`单引号、`(")`双引号和``(`)``反引号包裹字符串。

```javascript
var str = '';
var str = "";
var str = ``;
```

## Number

## Boolean

Boolean表示逻辑主题，就两个值，`true`和`false`。

```javascript
var x = true;
var y = false;
```

## Null

Null类型只有一个值：`null`。

## Undefined

定义了但未被赋值的变量的初始值`undefined`。

```javascript
function test(t) {
  if (t === undefined) {
     return 'Undefined value!';
  }
  return t;
}

var x;

console.log(test(x));
// 输出: "Undefined value!"

```

## Symbol
