# 准备放入Anki的内容


## html 中的主要概念有哪些？

## html 中元素常用的分类方式（还有其他的么？）
块级元素（block elements）、行内元素（inline elements）

## css 的选择器中的属性有哪些筛选方法？


## css的float 和 clear属性如何理解和使用？
float
[CSS 浮动](https://www.w3school.com.cn/css/css_positioning_floating.asp)
[float - CSS | MDN](https://developer.mozilla.org/zh-CN/docs/CSS/float)
当一个元素浮动之后，它会被移出正常的文档流，然后向左或者向右平移，一直平移直到碰到了所处的容器的边框，或者碰到另外一个浮动的元素。

clear
[clear - CSS（层叠样式表） | MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/clear)

这两个属性暂时不放入anki，还需要再实践和理解一下

## css中的伪类是什么改变？
[CSS 伪类](https://www.w3school.com.cn/css/css_pseudo_classes.asp)

## 伪类和伪元素是什么关系？
伪元素英文：Pseudo-elements

伪类：Pseudo-classes，添加到选择器的关键字，指定要选择的元素的特殊状态。
https://developer.mozilla.org/zh-CN/docs/Web/CSS/Pseudo-classes


CSS3 引入 ::before  是为了将伪类和伪元素区别开来。浏览器也接受由CSS 2 引入的 :before 写法。
基于CSS2的语法，伪元素和伪类都可以用一个冒号，如果基于CSS3的规则，伪元素应该用两个冒号，伪类为一个冒号
https://developer.mozilla.org/zh-CN/docs/Web/CSS/::before
常用的在CSS2中的伪元素就四个 befor after first-line first-letter，剩下的伪元素都是CSS3中定义的，必须用两个冒号区分，不过我目前还没怎么用到，以后再说


## css 中的颜色的合法值有哪些？
[CSS 合法颜色值](https://www.w3school.com.cn/cssref/css_colors_legal.asp)

## css 中 webkit-font-smoothing 是什么意思？
[字体平滑 - CSS（层叠样式表） | MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font-smooth)

font-smooth CSS 属性用来控制字体渲染时的平滑效果。




## css 中的文档流指的是什么？

W3C规范中没有document flow这个概念，只有normal-flow, 文档流的叫法主要还是多数中文译者的翻译方式问题。
[Visual formatting model](https://www.w3.org/TR/CSS2/visuren.html#normal-flow)
所以可以叫文档流、布局流、普通流，都是一回事


## css 中文档流和定位的关系？

[CSS普通流（文档流） | 前端工程师手册](https://leohxj.gitbooks.io/front-end-database/content/html-and-css-basic/css-normal-flow.html)
[正常布局流 - 学习 Web 开发 | MDN](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout/Normal_Flow)
[定位 - 学习 Web 开发 | MDN](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout/%E5%AE%9A%E4%BD%8D)


## 文档流的默认顺序修改
[writing-mode - CSS: Cascading Style Sheets | MDN](https://wiki.developer.mozilla.org/en-US/docs/Web/CSS/writing-mode)





## vscode中如何快速给代码增加注释？

[Mac vscode快捷键 - 笔记 - SegmentFault 思否](https://segmentfault.com/a/1190000012811886)

需要区分系统、环境、可自定义

Mac下最快是 Cmd + `/` 可以增加行注释

## css 中 position 属性对应哪些值，应该如何理解？

position 有 static relative absolute sticky fixed 五种主要的值，并且还需要搭配其他的属性和值综合使用

static 默认值，在文档流中，且top, right, bottom, left 和 z-index 属性无效
relative 不会移出文档流，以static时位置的左上角为圆点，进行便宜

absolute 移出正常流，通过指定元素相对于最近的非 static 定位祖先元素的偏移，来确定元素位置
fixed 移出正常流，通过指定元素相对于屏幕视口（viewport）的位置来指定元素位置。元素的位置在屏幕滚动时不会改变。打印时，元素会出现在的每页的固定位置。fixed 属性会创建新的层叠上下文。当元素祖先的 transform, perspective 或 filter 属性非 none 时，容器由视口改为该祖先。

sticky 元素根据正常文档流进行定位，然后相对它的最近滚动祖先（nearest scrolling ancestor）和 containing block (最近块级祖先 nearest block-level ancestor)，包括table-related元素，基于top, right, bottom, 和 left的值进行偏移

[position - CSS（层叠样式表） | MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/position)
上述链接的例子有大概的理解，还未通透，可以拆分开一个一个属性值对应的了解

https://stackoverflow.com/questions/24323615/css-relative-positioning-without-setting-parent-to-relative

## 什么是祖先元素?

## 什么是屏幕视口（viewport）

## 什么是最近滚动祖先（nearest scrolling ancestor）和 containing block (最近块级祖先 nearest block-level ancestor)

## 什么是层叠上下文（stacking context）

## 什么是ICB（inital container block, 初始包含块）

## z-index 是什么含义？

## float 和 clear
float 是脱离文档流的

## css 1、2、3是什么？

## w3c是什么

## 如何利用css做三角形还有其他图形？
有相关的文字，还可以继续参考
https://segmentfault.com/a/1190000005715074


## css 增加 content，如何回写html内容？
https://developer.mozilla.org/en-US/docs/Learn/CSS/Howto/Generated_content





## html中怎么使用css在图片上添加文字？
https://m.html.cn/qa/css3/13117.html




## border属性的solid值的含义
https://www.runoob.com/css/css-border.html
https://developer.mozilla.org/zh-CN/docs/Web/CSS/border
solid: 实线边框
dashed：虚线边框
dotted：点线边框
double
none hidden

## html 中如何实现代码高亮？

## 如何实现多个div的内容在同一行显示？
float
display
https://blog.csdn.net/u010615629/article/details/53886774
https://blog.csdn.net/aitangyong/article/details/42775803
https://blog.csdn.net/hantiannan/article/details/7428566
https://www.html.cn/qa/css3/14035.html
position


## html 超链接 a
https://www.runoob.com/html/html-links.html
https://www.w3schools.com/cssref/sel_link.asp
https://www.w3school.com.cn/css/css_link.asp




## 外边距重叠的情况如何处理？
暂时还没时间精力研究，先放着
https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Box_Model/Mastering_margin_collapsing



## css 中常用的几种选择器是什么？（还需要进一步理解）

基本选择器

类选择器：在css中以.开头，后面的内容匹配html中`class=''`中的内容

id选择器：在css中以#开头，后面的内容匹配html中`id=''`中的内容

属性选择器：在css中被[]包裹的内容

元素选择器（又称为**类型选择器**）：

通用选择器：*



分组选择器（Grouping selectors）

选择器列表：中间用逗号分隔，是或的关系


组合器（Combinators）

后代组合器（Descendant combinator）：空格分隔


直接子代组合器（Child combinator）：> 分隔

一般兄弟组合器（General sibling combinator）

紧邻兄弟组合器（Adjacent sibling combinator）：+分隔

列组合器（Column combinator）


伪选择器（Pseudo）

伪类

伪元素

注意说明：css1、css2、css3中的内容是有区分的，了解后需要在一些特殊场景下区分使用

参考页面：
https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Selectors
http://www.ruanyifeng.com/blog/2009/03/css_selectors.html
https://www.runoob.com/cssref/css-selectors.html
https://www.w3school.com.cn/cssref/css_selectors.asp




## 如何利用css伪元素画线段，同时不用改变html？
在我输出的总结中有相关的内容

## vscode中如何增加代码片段

## css 中的box-sizing 属性如何理解？
https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-sizing
要和框盒模型结合起来理解


## 框盒模型的进一步介绍
涉及到 content-area padding-area border-area margin-area
https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model

## display 如何理解？
https://developer.mozilla.org/zh-CN/docs/Web/CSS/display

最常见的集中值 display:inline、display:block、display:inline-block
https://blog.csdn.net/sinat_34719507/article/details/53512509
https://developer.mozilla.org/zh-CN/docs/Web/CSS/display


display: table

https://developer.mozilla.org/zh-CN/docs/Web/CSS/display
https://juejin.im/entry/6844903504817946637
https://www.w3schools.com/cssref/playit.asp?filename=playcss_display&preval=table
https://www.w3schools.com/cssref/pr_class_display.asp


## html中的属性、元素指的是什么？

## html中title是属性还是元素？

## 如何理解left和right属性？
https://developer.mozilla.org/zh-CN/docs/Web/CSS/left
https://www.w3schools.com/cssref/pr_pos_left.asp

## position 和 display 如何配合使用？

## background vs background-color vs color
color 值得是文本的颜色
background-color 是背景颜色
background 可以组合多个background相关的属性放到一起，如下例：
```
background: #ffffff url("img_tree.png") no-repeat right top;
```

这里的right和top是什么意思？

https://stackoverflow.com/questions/39033070/css-color-vs-background-color-vs-background

https://stackoverflow.com/questions/10205464/what-is-the-difference-between-background-and-background-color

## css中增加链接的语法是什么？

background: url("smiley.gif") no-repeat fixed center;


## css中的line-height的作用是什么？

line-height简单理解是行高，实际的理解还需看下面的链接了解其中的细节

https://segmentfault.com/a/1190000003038583
https://developer.mozilla.org/zh-CN/docs/Web/CSS/line-height
https://www.w3schools.com/cssref/pr_dim_line-height.asp
https://www.w3schools.com/cssref/tryit.asp?filename=trycss_line-height

## 为什么「margin:auto」可以让块级元素水平居中？以及margin相关的理解

https://www.zhihu.com/question/21644198
https://developer.mozilla.org/zh-CN/docs/Web/CSS/margin
https://blog.csdn.net/dkmings/article/details/51661056



## 如何让元素居中
https://juejin.im/post/6844903693142196238
https://github.com/ljianshu/Blog/issues/29
https://juejin.im/post/6844903919144075278
https://segmentfault.com/a/1190000014116655
https://louiszhai.github.io/2016/03/12/css-center/

## 什么是响应式布局和自适应布局

https://juejin.im/post/6844903814332432397
https://baike.baidu.com/item/%E5%93%8D%E5%BA%94%E5%BC%8F%E5%B8%83%E5%B1%80
http://caibaojian.com/356.html
https://juejin.im/post/6844903779431612424


## div span p标签三者间的区别

<p></p>是段落标签，也就块元素。

<div></div>也是块元素.

<span>是内联元素。
块状元素：独占一行，width和height起作用
内联元素：width和heigh不起作用，不占一行

html标签分块元素和行内元素，div，p都是块元素，span是行内元素。
div和span是没有意义的标签，而p是代表一段话，一排文字的意思。
主要是这两方面。

p为段落标记，<p></p>包含文本内容 span是行内元素 就是在行内定义一块区域。

<p></p>段落标签

<span></span>为文字设置单独样式

假如要为某一个段落设置样式，我们使用嵌入式的时候，可以这样写<p style="color:blue">某一个段落</p>

假如要为几个字设置样式时，我们使用嵌入式的时候，可以写成<span style="color:blue">某几个字</span>

抛开css不说，就是现在不要设置文字的样式，只要你有段落就会用到<p></p>，如果不设置文字样式的话，用不到<span></span>

p标签是块级元素，span元素是行内元素。内元素可以写在块级元素里面  比如<p><span>内容</span></p>

