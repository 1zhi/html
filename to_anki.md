# 准备放入Anki的内容


## html 中的主要概念有哪些？

## html 中元素常用的分类方式（还有其他的么？）
块级元素（block elements）、行内元素（inline elements）

## css 的选择器中的属性有哪些筛选方法？

## css 中.cover.links 和 .cover .links 一个有空格一个没空格，主要区别是什么？



## css 中常用的几种选择器是什么？（还需要进一步理解）

[CSS 元素选择器](https://www.w3school.com.cn/css/css_selector_type.asp)又称为**类型选择器**

[CSS id 选择器](https://www.w3school.com.cn/css/css_syntax_id_selector.asp)

#开头

[CSS 类选择器](https://www.w3school.com.cn/css/css_syntax_class_selector.asp)

.开头

[CSS 属性选择器](https://www.w3school.com.cn/css/css_syntax_attribute_selector.asp)
[]包裹

[CSS 派生选择器](https://www.w3school.com.cn/css/css_syntax_descendant_selector.asp)
没太理解

## css的浮动框
float
[CSS 浮动](https://www.w3school.com.cn/css/css_positioning_floating.asp)


## css中的伪类是什么改变？
[CSS 伪类](https://www.w3school.com.cn/css/css_pseudo_classes.asp)

## 伪类和伪元素是什么关系？

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


## css 中的 position 属性的 relative 和 absolute 为何总是成对存在？

理解relative需要static作为比较，relative和static最大的区别在于static属于文档流中，relative 虽然在最终的位置上和文档流的绝对位置不同，但实际上还是在文档流中的，是相对于static 时的位置的偏移。（最后一点需要一点时间验证）

absolute 的注意点在于首先移除文档流，第二个在于相对位置的判定上，常见的使用方法是有一个relative的父元素作为对比，方便做位置的调整与确定。

更多的内容参见下方的链接：
https://blog.csdn.net/weixin_40026101/article/details/80525871
https://www.hotbak.net/key/absolute%E5%92%8Crelative%E7%9A%84%E5%BA%94%E7%94%A8.html
https://www.zhangxinxu.com/wordpress/2010/12/css-%E7%9B%B8%E5%AF%B9%E7%BB%9D%E5%AF%B9relativeabsolute%E5%AE%9A%E4%BD%8D%E7%B3%BB%E5%88%97%EF%BC%88%E4%BA%8C%EF%BC%89/
https://www.zhangxinxu.com/wordpress/2011/08/css%E7%9B%B8%E5%AF%B9%E5%AE%9A%E4%BD%8Drelative%E7%BB%9D%E5%AF%B9%E5%AE%9A%E4%BD%8Dabsolute%E7%B3%BB%E5%88%97%EF%BC%88%E5%9B%9B%EF%BC%89/

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

## css 中 text-overflow 属性的作用？
https://developer.mozilla.org/zh-CN/docs/Web/CSS/text-overflow

## 为什么有时候 text-overflow 不生效？
因为要配合使用


## css 中 white-space 的处理？
https://developer.mozilla.org/zh-CN/docs/Web/CSS/white-space