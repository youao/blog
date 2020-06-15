# css-flex-master
网页布局（layout）是 CSS 的一个重点应用。
布局的传统解决方案，基于盒状模型，依赖 display 属性 + position属性 + float属性。它对于那些特殊布局非常不方便，比如，垂直居中就不容易实现。

2009年，W3C 提出了一种新的方案----Flex 布局，可以简便、完整、响应式地实现各种页面布局。目前，它已经得到了所有浏览器的支持，这意味着，现在就能很安全地使用这项功能。
Flex 布局将成为未来布局的首选方案。本文介绍它的语法，下一篇文章给出常见布局的 Flex 写法。网友 JailBreak 为本文的所有示例制作了 Demo，也可以参考。
以下内容主要参考了下面两篇文章：A Complete Guide to Flexbox 和 A Visual Guide to CSS3 Flexbox Properties。

Flex 是 Flexible Box 的缩写，意为"弹性布局"，用来为盒状模型提供最大的灵活性。
任何一个容器都可以指定为 Flex 布局。
注意，设为 Flex 布局以后，子元素的float、clear和vertical-align属性将失效。

采用 Flex 布局的元素，称为 Flex 容器（flex container），简称"容器"。它的所有子元素自动成为容器成员，称为 Flex 项目（flex item），简称"项目"。
容器默认存在两根轴：水平的主轴（main axis）和垂直的交叉轴（cross axis）。主轴的开始位置（与边框的交叉点）叫做main start，结束位置叫做main end；交叉轴的开始位置叫做cross start，结束位置叫做cross end。
项目默认沿主轴排列。单个项目占据的主轴空间叫做main size，占据的交叉轴空间叫做cross size。

以下6个属性设置在容器上。
flex-direction
flex-wrap
flex-flow
justify-content
align-items
align-content

flex-direction属性决定主轴的方向（即项目的排列方向）。
``` css
.box {
  flex-direction: row | row-reverse | column | column-reverse;
}
```
...
献上阮一峰大神教程
http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html

[盒模型](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)
