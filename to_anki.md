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

## css 中 position 的relative 和 absolute 还有 sticky 如何理解？

position 有 static relative absolute sticky fixed 等几种主要的值，并且还需要搭配其他的属性和值综合使用
[position - CSS（层叠样式表） | MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/position)
上述链接的例子有大概的理解，还未通透，可以拆分开一个一个属性值对应的了解

其中的几个关键信息为：
absolute 会将元素移出正常文档流，通过指定元素相对于最近的非 static 定位祖先元素的偏移，来确定元素位置
fixed 元素会被移出正常文档流，通过指定元素相对于屏幕视口（viewport）的位置来指定元素位置。元素的位置在屏幕滚动时不会改变。打印时，元素会出现在的每页的固定位置。fixed 属性会创建新的层叠上下文。当元素祖先的 transform, perspective 或 filter 属性非 none 时，容器由视口改为该祖先。

static 不会移出文档流，且top, right, bottom, left 和 z-index 属性无效
relative 不会移出文档流
sticky 元素根据正常文档流进行定位，然后相对它的最近滚动祖先（nearest scrolling ancestor）和 containing block (最近块级祖先 nearest block-level ancestor)，包括table-related元素，基于top, right, bottom, 和 left的值进行偏移



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

## display:inline、display:block、display:inline-block
https://blog.csdn.net/sinat_34719507/article/details/53512509
https://developer.mozilla.org/zh-CN/docs/Web/CSS/display

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