# javascript

运行于浏览器上的语言。 咱们看到的 十年前的网站，总会有 页面上，小雪花飘啊飘，或者小红旗， 用的就是这个语言做的。

其实它还可以做很多事情。

js 还可以做计算， 可以操作页面的 div 等 结构（我们叫DOM）， 还可以做表单验证， 文件上传等等功能。

## 一个例子

```
a = 1 + 1
alert('1 + 1 = ' + a)
```

## 定义变量

```

var a = 1;
var b = 2;

var c = a + b;

```

加上var， 就是局域变量 ( 只在当前的scope中生效)
不加var， 就是全局变量 ( 在浏览器的整个window中生效）

## 定义方法

```
function sum(a, b ) {
  return a  + b;
}
```

## 定义数组

```
var my_array = [1,2,3]
```

## hash

```
var jim = {
  name: "jim",
  age: 26
}
```
js中， 所有提到的“对象”， 都是hash.  包括： window, document

## 基本语法

循环：


```
/*
 1. 先声明变量 i = 0
 2. 再判断 i <= 这个数组的长度， 如果true的话，执行循环语句
 3. 执行完当前循环之后， 让i 增加1. 再继续执行 第二步。
*/
var my_array = [1,2,3]
for( var i = 0 ; i<= my_array.length; i++ ) {
  console.info(my_array[i])
}

```

if-else: 几乎所有的编程语言都长这样：

```
var result = true;

if(result) {
  // .. .
}else{
  // .. .
}

```

判断是否会运行正常：  try catch:

```
try{
  100 / 0

}catch(e) {
  console.error(e)
}

```

## 语法要求：

每一行最后都要有  ';'   但是我一般不写。 （前提是不会压缩它）

未压缩：

```
a = 1;
b = 2;
c = 3;
function(e){
  alert(e);
}

```
压缩（多行变一行，为了让浏览器更快的加载）：

```
a = 1; b = 2; c = 3; function(e){ alert(e); }
```
所以， 如果你的js 代码要被压缩的话， 务必，每一行都要严格的写上 `;`

## javascript中， 跟浏览器相关的变量和方法。

以下的变量和方法， 在纯粹的js 环境下（例如 nodejs）是不能使用的。 但是在浏览器中， 可以不经过声明， 直接调用。

- window

表示当前的 窗口

```
window
> Window {speechSynthesis: SpeechSynthesis, caches: CacheStorage, localStorage: Storage, sessionStorage: Storage, webkitStorageInfo: DeprecatedStorageInfo…}
```

我们定义的 所有 不带 `var`的变量，其实都是window中的对象。

```
a = 1
window.a = 1
```
是一样的。

- document

表示当前的窗口的 document, 是重要的文档对象。

```
document.getElementById()
```
这个方法就可以能根据id 来找到某个 <div> 元素。 这个方法，也被jQuery取代了。

```
document.write()
```
用来向当前页面上， 增加一段文字。 （极其罕见这个用法）目前，几乎所有的操作，都通过jQuery中使用

- alert()方法

该方法会显示一个窗口。

- confirm()方法

显示一个窗口，让用户选择 OK , cancel

## js 中的内置对象和函数。

- console 控制台

有若干方法可以调用

```
console.debug('我是debug')
console.info('我是info')
console.warn('我是warn')
console.error('我是error')
```

- setTimeout

在若干毫秒之后，执行某个函数

```
setTimeout(function(){
  console.info('你会在1.5秒后看到我')
} , 1500)
```

- setInterval


每隔若干毫秒，就执行一个方法

```
setInterval(function(){
  console.info(new Date().getTime()
)}, 1000)
```
