# ES1 to ES6

### 历史 :tada:

> * ES1：JavaScript 第一版，发布于 1997 年。
> * ES2：JavaScript 第二版，发布于 1998 年，包含了一些修改和错误修复。
> * ES3：JavaScript 第三版，发布于 1999 年，引入了正则表达式、try-catch、对象属性的 getter 和 setter 等特性。
> * ES4：因为在标准制定过程中，ES4 的提案与实际需求不符而被废除。
> * ES5：JavaScript 第五版，发布于 2009 年，增加了严格模式、数组方法（如 forEach、map、reduce 等）和 JSON 对象等特性。
> * ES6（也称 ECMAScript 2015）：JavaScript 第六版，发布于 2015 年，包含了箭头函数、let 和 const 变量声明、解构赋值、默认参数、展开操作符、模板字符串、类和模块等特性。
>
> 除此之外，还有 ES7、ES8、ES9、ES10、ES11 等版本，不过它们相对于 ES6 来说变化较小，引入的新特性也比较局限。

{% tabs %}
{% tab title="ES1" %}
```
// 使用 var 声明变量
var x = 5;
var y = 10;

// 使用 function 声明函数
function add(a, b) {
  return a + b;
}

// 使用 new 声明对象
var obj = new Object();
obj.name = "John";
obj.age = 30;

// 使用 for 循环迭代数组
var arr = [1, 2, 3];
for (var i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}

```
{% endtab %}

{% tab title="ES2" %}
```javascript
// 使用 let 和 const 声明变量
let x = 5;
const y = 10;

// 使用 try-catch 语句处理异常
try {
  // some code
} catch (err) {
  console.log(err);
}

// 使用正则表达式
var re = /hello/g;
var str = "hello world";
console.log(re.test(str));

```
{% endtab %}

{% tab title="ES3" %}
{% code title="Javascript" overflow="wrap" lineNumbers="true" %}
```javascript
// 使用 new Date() 获取当前日期
var date = new Date();
console.log(date.toLocaleDateString());

// 使用 eval() 执行字符串代码
var x = 1;
var y = 2;
var z = eval("x + y");
console.log(z);

// 使用字符串的 replace() 方法替换字符串
var str = "hello world";
console.log(str.replace("world", "John"));

```
{% endcode %}
{% endtab %}

{% tab title="ES4" %}
```
ES4 是一个备受争议的版本，因为它引入了很多新的特性，包括类型推断、类型注释、函数重载等，这些特性使得 JavaScript 更加像是一种传统的面向对象语言。由于社区反对，ES4 最终没有发布。

ES5 (2009):

ES5 引入了很多新的特性，包括严格模式、Array 的一些方法、JSON 对象、Function.prototype.bind() 等。
```
{% endtab %}

{% tab title="ES5" %}
```javascript
// 使用 strict 模式
"use strict";
x = 3; // 报错，x 未定义

// 使用 Array 的 forEach() 方法迭代数组
var arr = [1, 2, 3];
arr.forEach(function(item) {
  console.log(item);
});

// 使用 JSON 对象进行数据解析
var jsonStr = '{"name":"John","age":30}';
var jsonObj = JSON.parse(jsonStr);
console.log(jsonObj.name);

// 使用 Function.prototype.bind() 绑定函数的 this 值
var obj = {
  name: "John",
  sayHello: function() {
    console.log("Hello, " + this.name);
  }
};
var func = obj.sayHello.bind(obj);
func();
```
{% endtab %}

{% tab title="ES6" %}
ES6（ECMAScript 2015）是 JavaScript 的一个版本，引入了很多新特性和语法糖。下面是一些 ES6 的新特性和相应的例子：

1. let 和 const 关键字

```javascript
// let 定义变量，作用域为块级
let a = 1;
if (true) {
  let a = 2;
}
console.log(a); // 1

// const 定义常量，一旦赋值不可更改
const b = 3;
b = 4; // TypeError: Assignment to constant variable.


```

2. 箭头函数

```javascript
// 箭头函数定义函数
const sum = (a, b) => a + b;
console.log(sum(1, 2)); // 3

// 箭头函数与 map 结合使用
const arr = [1, 2, 3];
const arr2 = arr.map(x => x * 2);
console.log(arr2); // [2, 4, 6]


```

3. 模板字符串

```javascript
// 模板字符串可以直接换行
const str = `Hello
             world`;
console.log(str); // Hello
                  // world

// 模板字符串插入变量
const name = 'Tom';
const str2 = `Hello, ${name}!`;
console.log(str2); // Hello, Tom!


```
{% endtab %}
{% endtabs %}









