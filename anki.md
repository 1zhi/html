# 该文档存放已经置于anki的知识点

## 图示解释盒子模型（The Box Model）
涉及到的几个关键术语为：
margin
background-color
background-image
border
padding
content

图片示意如下（图片来自网络）
![](./_image/2020-09-07/2020-09-07-15-03-53.png)

## Css的中英文全称是什么？
Cascading Style Sheets
层叠样式表

## Html 的中英文全称是什么？
HyperText Marked Language
超文本标记语言


## html文件的基本结构包含哪些内容？

包含 DOCTYPE, html, head, body 标签对等，内容如下：
```
<!DOCTYPE html>
<html lang="zh">
    <head>
        <meta charset="UTF-8">
        <title>1zhi</title>
        <link href="/style.css",type="text/css",rel="stylesheet"/>
    </head>

    <body>

    </body>

</html>
```

## 在html中引入css外部样式表的语法格式？

```
<link href="/sytle.css", type="text/css", rel="stylesheet"/>
```

## 在html中有哪三种引入css样式表的方法，如果多种引入样式表的方式同时使用时会有什么效果？

* 方法一外部样式表：通过在head中引入link的方式
```
<link href="/style.css", type="text/css", rel="stylesheet" />
```
* 方法二内部样式表：在head中定义内部样式表
```
<style type="text/css">
    hr {color: sienna;}
</style>
```
* 方法三内联样式：在相关的html标签内使用
```
<p style="color: sienna; margin-left: 20px">
This is a paragraph
</p>
```

如果多种引入样式表的方法同时使用，如果某些属性在不同的样式表中被同样的选择器定义，属性值将从更具体的样式表中被继承。

## html 和 css的注释语法是？
```
<! --html 的注释内容-->
```

```
/* css的注释内容 */
```

## css 中的基本概念有哪些，并用实际的代码举例说明？

规则、选择器、声明（包含属性和值）

**CSS 规则**由两个主要的部分构成：选择器，以及一条或多条声明。

**选择器**通常是您需要改变样式的 HTML 元素。

每条**声明**由一个属性和一个值组成。

属性（property）是您希望设置的样式属性（style attribute），每个属性有一个值。属性和值被冒号分开。

```
selector {property: value}
```

以下代码举例
```
h1 {color:red; font-size:14px;}
```
![](./_image/2020-09-07/2020-09-07-16-15-53.jpg)


## css 中的伪元素是什么，常用的伪元素有哪些？

英文为：Pseudo-elements

CSS 伪元素用于向某些选择器设置特殊效果。

常用的伪元素有：
:first-line
:first-letter
:before
:after


## margin 和 padding的属性值有哪些，这两个元素的使用有什么注意事项？

margin 的值可以是1个到4个值，可以是长度、百分比、自动，语法格式如下：
`[ <length> | <percentage> | auto ]{1,4}`

其中长度包括和绝对长度和相对长度，比例是百分比。
如果是1个值是对四边有效，两个值是上下和左右，三个值是上、下、左右，四个值对应上右下左顺时针方向

另外要注意：margin对内联元素的上下会失效，padding不会

其他的知识点如果需要更新，参考如下的链接
https://developer.mozilla.org/zh-CN/docs/Web/CSS/margin
https://developer.mozilla.org/zh-CN/docs/Web/CSS/length
https://developer.mozilla.org/zh-CN/docs/Web/CSS/percentage
https://developer.mozilla.org/zh-CN/docs/Web/CSS/padding


## html 中 css 没出现效果的原因是什么，如何排查？

* 有可能是使用了代理，导致本地环境无法在浏览器中更新效果，解决办法：关闭代理。
* html中调用css的文件名写错了，link中格式错误（有逗号、属性写错等等）。解决办法：检查文件名、引用的语法等。
* 有可能是正常的效果就是没有效果的，自己搞错了。解决办法：要确认css生效了，可以加入如下的代码段，核心是让css的方式回写html文字的方式直接的看到效果。

```html
<span class='ref'>Something<span>
```

```css
.ref:before{
    content: "Reference";
    color: navy;
    font-weight: bold;
}
```

## 如何利用border画圆形？
设置border包含内容 的长和宽、border的线宽、border的圆角，
可以画实心圆、空心圆等各种，举例如下：
```
#round03{
    width: 50px;
    height: 50px;
    background-color: transparent;
    border-radius: 50px;
    border: 25px solid red;
}
```

## css的选择器中 中.cover.links 和 .cover .links 一个有空格一个没空格，主要区别是什么？

有空格的指的是.cover元素下的.links后代元素。这里的空格是后代元素选择的语法
没有空格是匹配多个class，html的class属性可以同时存在多个值，中间用空格隔开即可

## css中的box-sizing属性可以有哪些值，对应的区别是什么？

box-sizing可以为 content-box 或者 border-box，默认为content-box。
主要区别在于对元素的width和height的值的计算逻辑不同，基于框盒模型，content-box 以content area的长宽计算，padding和border的部分不计算在内。
和border-box以content和padding和border的长宽总和计算width和height。

参考链接：https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-sizing


## 说明

卡片的内容大部分来自自己的理解，图片一般来自互联网的搜索，一些概念和定义来自[w3school](https://www.w3school.com.cn/css/css_syntax.asp)，均为非商业引用。