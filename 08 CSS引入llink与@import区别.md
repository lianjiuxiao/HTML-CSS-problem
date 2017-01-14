#  CSS引入方式的异同

## CSS引入方式
    * 行内式
    * 内联式
    * 外嵌式(1.link 2.@import)

## 外联式两种方法的区别：
    1.link是属于XHTML范畴的，除了可以加载CSS之外，还可以定义RSS(就是一段规范的XML数据，一般以rss，xml或者rdf作为后缀)，而@import只能加载CSS
    2.link在引用CSS的时候，在页面加载的同时加载CSS文件，而@import是在页面加载完成之后，才加载的。
    3.link不是XML标签，没有兼容性，@import是CSS2.1之后推出来的，低版本浏览器不支持。
    4.link支持js控制DOM去改变样式，而@import不支持

##　@import的几种写法
    @import 'style.css' //Windows IE4/ NS4, Mac OS X IE5, Macintosh IE4/IE5/NS4不识别
    @import "style.css" //Windows IE4/ NS4, Macintosh IE4/NS4不识别
    @import url(style.css) //Windows NS4, Macintosh NS4不识别
    @import url('style.css') //Windows NS4, Mac OS X IE5, Macintosh IE4/IE5/NS4不识别
    @import url("style.css") //Windows NS4, Macintosh NS4不识别　