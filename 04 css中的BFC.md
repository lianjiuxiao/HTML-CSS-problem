# BFC 

* 定义:BFC是Block Formatting Context （块级格式化上下文）的缩写，它是W3C CSS 2.1      规范中的一个概念，是一个独立的渲染区域，只有Block-level box参与， 它规定了内部的Block-level Box如何布局，并且与这个区域外部毫不相干。

* 什么情况下会触发BFC?
  1.浮动元素（float: left | right）；

  2.绝对定位元素（position: absolute | fixed）；

  3.行内块元素（display: inline-block）；

  4.表格的单元格（display: table-cells，TD、TH）；

  5.表格的标题（display: table-captions，CAPTION）；

  6.'overflow' 特性不为visible 的元素（除非该值已经传播到viewport?）；

  7.表格元素创建的"匿名框" ;
* BFC布局规则
    1.内部的Box会在垂直方向，一个接一个地放置。
    2.Box垂直方向的距离由margin决定。属于同一个BFC的两个相邻Box的margin会发生重叠
    3.每个元素的margin box的左边， 与包含块border box的左边相接触(对于从左往右的格式化，否则相反)。即使存在浮动也是如此。
    4.BFC的区域不会与float box重叠。
    5.BFC就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素。反之也如此。
    6.计算BFC的高度时，浮动元素也参与计算



  ```
  <!DOCTYPE html>
  <html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Test</title>
    <style>
      .box{
        width: 300px;
        height: 300px;
        position: relative;
        border: 1px solid #000;
      }
      .son1{
        width: 100px;
        height: 150px;
        float: left;
        background-color: pink;
      }
      .son2{
        height: 200px;
        background-color: red;
        /* 如果这里加上overflow的话，就会出现BFC情形 */
        /* 看效果请去掉这句代码 */
        overflow: hidden;
      }
    </style>
  </head>
  <body>
    <div class="box">
      <div class="son1"></div>
      <div class="son2"></div>
    </div>
  </body>
  </html>
  ```
