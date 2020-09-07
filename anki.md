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