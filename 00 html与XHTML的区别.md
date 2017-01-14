
# 不同点
1.XHTML 元素必须被正确地嵌套。
错误：<p><span>this is example.</p></span>
正确：<p><span>this is example.</span></p>

2.XHTML 元素必须被关闭。
错误：<p>this is example.
正确：<p>this is example.</p>

3.标签名必须用小写字母。
错误：<P>this is example.<P>
正确：<p>this is example.</p>
3.1空标签也必须被关闭
错误：<br>
正确：<br/>

4.XHTML 文档必须拥有根元素。
所有的 XHTML 元素必须被嵌套于 <html> 根元素中。


<!-- other -->

xhtml比html更注重语义，更接近xml

html允许一些不规范的写法，如：
html下可以写：<br>，而xhtml有严格限制，每个标签都得关闭，要写成：<br />
html下<table width=100>，可以不写引号""，而xhtml必须正确的写成：<table width="100">

xhtml废除了一些html里面的标签，原因是制定这个规范的w3c的牛人们觉得有些旧东西该淘汰或不科学

在xhtml和html下，同样的css样式表解析出来会有很多细节上的小差异