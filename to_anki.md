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
https://blog.csdn.net/zhangchen124/article/details/79634842


## css 中 white-space 的处理？
https://developer.mozilla.org/zh-CN/docs/Web/CSS/white-space

## line-height 如何使用？
主要用于多行元素的空间量，例如多行文本的间距
https://developer.mozilla.org/zh-CN/docs/Web/CSS/line-height

## text-decoration 用来做什么?
文本的修饰线外观，比如超链接默认有下划线等等，可以去掉这些修饰
https://developer.mozilla.org/zh-CN/docs/Web/CSS/text-decoration

## html 中 图片的标签和属性？

<img src="xx.jpg" alt= "">

https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img

## html 中的属性值用单引号还是双引号？

## right 和 left 属性在什么情况下会生效？

## background相关属性和使用
如何能够在css中同时存在 background color 和 image

https://juejin.im/post/6844904097733148686
https://www.cnblogs.com/tianma3798/p/7905341.html

## margin 的具体应用
https://developer.mozilla.org/zh-CN/docs/Web/CSS/margin

## css  position 中 absolute 和 relative 的组合应用

## font-size 在什么情况下会不生效？
这一类关于文字的修饰的问题可以放到一起考虑了解一下

https://developer.mozilla.org/en-US/docs/Web/CSS/font-size
https://juejin.im/post/6844903615816007693
https://www.html.cn/qa/css3/16863.html
https://blog.windstone.cc/front-end/css/font/css-font-metrics-line-height-and-vertical-align.html#line-height
https://www.w3cplus.com/css/css-font-metrics-line-height-and-vertical-align.html

## 如何引入iconfont
* [html 中 引用 iconfont - Google 搜索](https://www.google.com/search?sxsrf=ALeKk03Jy6VMhyTNoyNy88kuDsfpihv70Q%3A1601283629339&ei=LaZxX9WMFIrpsAea8r2YDA&q=html+%E4%B8%AD+%E5%BC%95%E7%94%A8+iconfont&oq=html+%E4%B8%AD+%E5%BC%95%E7%94%A8+iconfont&gs_lcp=CgZwc3ktYWIQAzoECAAQRzoECCMQJzoECAAQQzoCCAA6BAgAEAw6BQgAEMsBUMgFWKYfYM0iaANwAXgBgAHWA4gByiKSAQcxLjMtOS4zmAEAoAEBoAECqgEHZ3dzLXdpesgBCMABAQ&sclient=psy-ab&ved=0ahUKEwiV16SvvovsAhWKNOwKHRp5D8MQ4dUDCA0&uact=5)
* [关于iconfont三种引用方法的详细介绍（新手必备） 董事长 - 知乎](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=%E5%85%B3%E4%BA%8Eiconfont%E4%B8%89%E7%A7%8D%E5%BC%95%E7%94%A8%E6%96%B9%E6%B3%95%E7%9A%84%E8%AF%A6%E7%BB%86%E4%BB%8B%E7%BB%8D%EF%BC%88%E6%96%B0%E6%89%8B%E5%BF%85%E5%A4%87%EF%BC%89%20%E8%91%A3%E4%BA%8B%E9%95%BF%20-%20%E7%9F%A5%E4%B9%8E&pos=572&uri=https://zhuanlan.zhihu.com/p/28249275)
* [Web端如何引用iconfont，iconfont所有的引用方式。_RunCoder-CSDN博客](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=Web%E7%AB%AF%E5%A6%82%E4%BD%95%E5%BC%95%E7%94%A8iconfont%EF%BC%8Ciconfont%E6%89%80%E6%9C%89%E7%9A%84%E5%BC%95%E7%94%A8%E6%96%B9%E5%BC%8F%E3%80%82_RunCoder-CSDN%E5%8D%9A%E5%AE%A2&pos=0&uri=https://blog.csdn.net/TheMisery_Hang/article/details/79825688)
* [iconfont - Google 搜索](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=iconfont%20-%20Google%20%E6%90%9C%E7%B4%A2&pos=1258&uri=https://www.google.com/search?q=iconfont&oq=iconfont&aqs=chrome..69i57j69i61l2.327j0j7&sourceid=chrome&ie=UTF-8)
* [Iconfont-阿里巴巴矢量图标库](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93&pos=0&uri=https://www.iconfont.cn/collections/index?spm=a313x.7781069.1998910419.5&type=1)
* [All Icons | IcoFont](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=All%20Icons%20%7C%20IcoFont&pos=0&uri=https://icofont.com/icons)
* [All Icons | IcoFont](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=All%20Icons%20%7C%20IcoFont&pos=0&uri=https://icofont.com/icons)
* [How to Use | IcoFont](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=How%20to%20Use%20%7C%20IcoFont&pos=354&uri=https://icofont.com/how-to-use)
* [一次性搞定 Iconfont](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=%E4%B8%80%E6%AC%A1%E6%80%A7%E6%90%9E%E5%AE%9A%20Iconfont&pos=0&uri=https://juejin.im/post/6844903715023880199)
* [Iconfont-阿里巴巴矢量图标库](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=Iconfont-%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4%E7%9F%A2%E9%87%8F%E5%9B%BE%E6%A0%87%E5%BA%93&pos=0&uri=https://www.iconfont.cn/)
* [Font Awesome](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=Font%20Awesome&pos=0&uri=https://fontawesome.com/?from=io)
* [JohnWong/IconFont: IconFont is a way to build lossless images of pure color with font file。IconFont是一种通过字体文件来构建纯色图的方案。](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=JohnWong%2FIconFont%3A%20IconFont%20is%20a%20way%20to%20build%20lossless%20images%20of%20pure%20color%20with%20font%20file%E3%80%82IconFont%E6%98%AF%E4%B8%80%E7%A7%8D%E9%80%9A%E8%BF%87%E5%AD%97%E4%BD%93%E6%96%87%E4%BB%B6%E6%9D%A5%E6%9E%84%E5%BB%BA%E7%BA%AF%E8%89%B2%E5%9B%BE%E7%9A%84%E6%96%B9%E6%A1%88%E3%80%82&pos=0&uri=https://github.com/JohnWong/IconFont)
* [aliceui/iconfont: alice iconfont](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=aliceui%2Ficonfont%3A%20alice%20iconfont&pos=0&uri=https://github.com/aliceui/iconfont)

## css中的@是什么意思？
* [css 中的@ 是什么意思 - Google 搜索](https://www.google.com/search?sxsrf=ALeKk00X-TTUIEmwvWrqFQkfyXFfZODOIA%3A1601284941487&ei=TatxX-f8HMXisAeKvbz4Cw&q=css+%E4%B8%AD%E7%9A%84%40+%E6%98%AF%E4%BB%80%E4%B9%88%E6%84%8F%E6%80%9D&oq=css+%E4%B8%AD%E7%9A%84%40+%E6%98%AF%E4%BB%80%E4%B9%88%E6%84%8F%E6%80%9D&gs_lcp=CgZwc3ktYWIQA1CaXVi7ZGDAZmgAcAB4AIAB3AKIAeMPkgEDMy02mAEAoAEBqgEHZ3dzLXdpesABAQ&sclient=psy-ab&ved=0ahUKEwin1_ugw4vsAhVFMewKHYoeD78Q4dUDCA0&uact=5)
* [这个css里的@是什么意思呢？ - SegmentFault 思否](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=%E8%BF%99%E4%B8%AAcss%E9%87%8C%E7%9A%84%40%E6%98%AF%E4%BB%80%E4%B9%88%E6%84%8F%E6%80%9D%E5%91%A2%EF%BC%9F%20-%20SegmentFault%20%E6%80%9D%E5%90%A6&pos=1698&uri=https://segmentfault.com/q/1010000010043557)
* [css 中的@import 是什么意思 - Google 搜索](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=css%20%E4%B8%AD%E7%9A%84%40import%20%E6%98%AF%E4%BB%80%E4%B9%88%E6%84%8F%E6%80%9D%20-%20Google%20%E6%90%9C%E7%B4%A2&pos=822&uri=https://www.google.com/search?q=css+%E4%B8%AD%E7%9A%84%40import+%E6%98%AF%E4%BB%80%E4%B9%88%E6%84%8F%E6%80%9D&oq=css+%E4%B8%AD%E7%9A%84%40import+%E6%98%AF%E4%BB%80%E4%B9%88%E6%84%8F%E6%80%9D&aqs=chrome..69i57.3756j0j9&sourceid=chrome&ie=UTF-8)
* [了解CSS中的@import_我的技术博客 - SegmentFault 思否](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=%E4%BA%86%E8%A7%A3CSS%E4%B8%AD%E7%9A%84%40import_%E6%88%91%E7%9A%84%E6%8A%80%E6%9C%AF%E5%8D%9A%E5%AE%A2%20-%20SegmentFault%20%E6%80%9D%E5%90%A6&pos=480&uri=https://segmentfault.com/a/1190000000369549)
* [css link和@import区别用法 - DIVCSS5](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=css%20link%E5%92%8C%40import%E5%8C%BA%E5%88%AB%E7%94%A8%E6%B3%95%20-%20DIVCSS5&pos=0&uri=http://www.divcss5.com/rumen/r431.shtml)
* [CSS培训_DIV+CSS培训-DIVCSS5在线培训课程](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=CSS%E5%9F%B9%E8%AE%AD_DIV%2BCSS%E5%9F%B9%E8%AE%AD-DIVCSS5%E5%9C%A8%E7%BA%BF%E5%9F%B9%E8%AE%AD%E8%AF%BE%E7%A8%8B&pos=0&uri=http://www.divcss5.com/peixun/#n6)
* [@import - CSS（层叠样式表） | MDN](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=%40import%20-%20CSS%EF%BC%88%E5%B1%82%E5%8F%A0%E6%A0%B7%E5%BC%8F%E8%A1%A8%EF%BC%89%20%7C%20MDN&pos=1837&uri=https://developer.mozilla.org/zh-CN/docs/Web/CSS/@import)
* [在线加密解密](https://tool.oschina.net/encrypt?type=3)
* [base 64 解密 - Google 搜索](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=base%2064%20%E8%A7%A3%E5%AF%86%20-%20Google%20%E6%90%9C%E7%B4%A2&pos=0&uri=https://www.google.com/search?q=base+64+%E8%A7%A3%E5%AF%86&oq=base+64+%E8%A7%A3%E5%AF%86&aqs=chrome..69i57.5075j0j7&sourceid=chrome&ie=UTF-8)
* [Base64加密、解密 - 站长工具](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=Base64%E5%8A%A0%E5%AF%86%E3%80%81%E8%A7%A3%E5%AF%86%20-%20%E7%AB%99%E9%95%BF%E5%B7%A5%E5%85%B7&pos=0&uri=https://tool.chinaz.com/tools/base64.aspx)
* [x-font-woff2 - Google 搜索](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=x-font-woff2%20-%20Google%20%E6%90%9C%E7%B4%A2&pos=631&uri=https://www.google.com/search?q=x-font-woff2&oq=x-font-woff2&aqs=chrome..69i57.817j0j7&sourceid=chrome&ie=UTF-8)
* [Proper MIME type for .woff2 fonts - Stack Overflow](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=Proper%20MIME%20type%20for%20.woff2%20fonts%20-%20Stack%20Overflow&pos=990&uri=https://stackoverflow.com/questions/28235550/proper-mime-type-for-woff2-fonts)
* [了解woff2字体及转换 « 张鑫旭-鑫空间-鑫生活](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=%E4%BA%86%E8%A7%A3woff2%E5%AD%97%E4%BD%93%E5%8F%8A%E8%BD%AC%E6%8D%A2%20%C2%AB%20%E5%BC%A0%E9%91%AB%E6%97%AD-%E9%91%AB%E7%A9%BA%E9%97%B4-%E9%91%AB%E7%94%9F%E6%B4%BB&pos=5854&uri=https://www.zhangxinxu.com/wordpress/2018/07/known-woff2-mime-convert/)
* [WOFF 2.0 – Learn more about the next generation Web Font Format and convert TTF to WOFF2](chrome-extension://klbibkeccnjlkjkiokjodocebajanakg/suspended.html#ttl=WOFF%202.0%20%E2%80%93%20Learn%20more%20about%20the%20next%20generation%20Web%20Font%20Format%20and%20convert%20TTF%20to%20WOFF2&pos=269&uri=https://gist.github.com/sergejmueller/cf6b4f2133bcb3e2f64a)
* [Covid 19 Icons | Font Awesome](https://fontawesome.com/icons?d=gallery&q=covid-19&m=free)
* [User Nurse Icon | Font Awesome](https://fontawesome.com/icons/user-nurse?style=solid)