# Markdown 图片

Markdown 图片语法格式：

![alt 属性文本](图片地址)
![alt 属性文本](图片地址 "可选标题")

- 开头一个感叹号 !
- 接着一个方括号，里面放上图片的替代文字
- 接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上选择性的 'title' 属性的文字

例子：
![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png)
![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png "RUNOOB")

也可以像网址那样对图片网址使用变量

这个链接用 1 作为网址变量[RUNOOB][1].
然后再文档的结尾为变量赋值（网址）

[1]: http://static.runoob.com/images/runoob-logo.png

Markdown还没有办法制定图片的高度和宽度，可以使用HTML的<img>标签
<img src="http://static.runoob.com/images/runoob-logo.png" width="50%">
