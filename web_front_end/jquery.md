# 十年前， 存在鄙视链

程序员鄙视链。
后端(java)  >  js   >  html/css

## 原生 js的时代

当年的js, 是大家都不愿意去学习的。 为什么？ 特别不规范。

比如： java语言特别严禁。 我在windows, 和 linux上面，开发时，写的代码，一样。 调试时，表现一样。
js: 在IE5,6 上， 跟 firefox上，是完全不同的。

而且 , js 报错时，不会给出特别清晰的错误。

例如：  在当年的IE页面上，会提示：

```
当前页的脚本发生错误

行： 140
字符： 2012
错误： XX对象为空或不是对象。
代码： 0
```
然后我们兴冲冲的 打开这个页面的源代码， （这是个HTML页面）， 发现： 140行，根本没有JS代码。全都是HTML。
我们就蒙了。

所以，大家对于js 是又佩服又恨。

恨的是： 这个语言调试起来太可怕了。没法调试没法开发。 作后端的人，完全不想碰js.
佩服的是： 如果某个人，能给你一段JS代码，说：“把它复制上去，你的XX功能就能用了”，当年，我会觉得这个人英雄。

# 原生时期的js , 是一个怪兽。

怪兽有几个有名，但是可怕的点：

1. Ajax: 当年特别高级。 页面不用刷新，就能更新部分内容。 大家纷纷效仿。 06年有段时间一直想学ajax, 发现，
它跟茴香豆一样，有好几种写法。而且在不同的平台，需要写不同的代码。 所以我放弃了。
2. 动画效果。 高亮，渐变，漂雪花。当年的特别简陋，就这个，还需要好多好多代码。
3. 操作DOM。 （表单验证阿，修改HTML结构。。。）。 特别可怕。 只有寥寥几个方法可以用。getElementById()

而且，js语法的原生函数，名称不统一，对程序员不友好。

# Prototype, extJS 等年代。

extJS 2.0: 2007年。 当时实现了： 表格的分页，表格的排序，内容下载程excel. 实现的很利索。所以比较有名气。
但是： 1. 收费。 2. 不好定制化开发。(完全定制不了，因为它太复杂了）

prototype: 2005年被创建，但是，在国内，2008-09年左右才被人接受。渐渐使用。

```
document.getElementById("id_of_element")
在prototype下可以写成：

$("id_of_element")
```

另外prototype 还引入了很多比native js 方便很多的方法。例如，动画等操作。

但是，prototype 学习曲线特别高。

# jQuery

2006 年出现，国内10年以后才开始流行。

它的目的： 作者发现prototype 虽然比原生的js的各种方法名有了很大改进， 但是用起来，还是不人性化。

所以，作者对prototype进行了 “重构”， 到后来，就成了一个独立的项目，是prototype 的替代者。

目前，世界上  65%的网站使用了jQuery. 它有无数插件。

目前，流行的编程语言的风格，受到 ruby/jquery很大的影响。

给我一杯咖啡。

give('me').coffee(1)


对比：  给定一个table, 我希望对它的倒数第三行，左起第5列中的 第二个<a> 的样式，color改成red.

原生js:  写100代码。
prototype: 30 行。
jQuery: 2行。

jQuery 的写法大概就是：

jQuery('table tr').last(3).find('td')[4].find('a').second().css({color: 'red'})

jQuery的中的方法，完全根据大家的口语习惯来的。 如果你是欧美人，你会发现，几乎可以把你的文字需求，
直接转换成极其相似的jQuery代码。

## 记住一点

使用jQuery就对了。




## 安装

直接引入一个<script>

  <script src="https://code.jquery.com/jquery-1.12.4.js"></script>

然后就可以直接在页面中使用了。


<script>
jQuery('.tips')    //  跟css  selector 一样， 选择好所有的 class='tips' 这样的dom
jQuery('#footer')    //  跟css  selector 一样， 选择好所有的 id='footer' 这样的dom
jQuery('div')    //  跟css  selector 一样， 选择好所有的 div
jQuery 也写成： $
</script>

jQuery 几大块功能：

1. 选择，操作DOM

```
$('body').append(...)
```

append/prepend/html/text
wrap...
Manipulation
Class Attribute
Copying
DOM Insertion, Around
DOM Insertion, Inside
DOM Insertion, Outside
DOM Removal
DOM Replacement
General Attributes
Style Properties

以上API中的功能，大家都要知道。

2. Ajax 请求

$.get('http://www.baidu.com', function(data){
   console.info(data)
})


看 http://w3school.com.cn/jquery/index.asp

1. jQuery 遍历（就是上面的DOM操作）
2. AJAX
3. 动画效果。

