# 第二次作业  
- 周敬


老师，您好，我是美术跨专业学生周敬，作业请教了刘一达和何蕊同学，
教我在IDEA上上传文档，以及学习代码部分。
刚学习C#，接收能力有点差，感觉真的很难，很多方面还是理解不了。还在努力学习中，争取跟上部队！
- 作业要求：

使用Open XML SDK方法解析Word文件，提取出Word文件中的所有文字。文字按段落分组。使用WordprocessingDocument类作为实验项目的主要类。
把方法封装到自定义类中。

知识点

使用VS2017中的NuGet安装项目的外部引用。
熟悉Word文件的XML格式。
熟悉XML格式及OpenXmlElement处理，熟悉XML中对象的遍历。


第一步：了解XML是什么？

XML是指可扩展标记语言（EXtensible Markup Language），XML是传输数据的一项工具。
XML标签没有被预定义，需要自行定义标签。 XML 是 W3C 的推荐标准。

第二步：提取文档

先把文档下载到桌面，再打开VS，在VS中通过管理NuGet程序包添加DocumentFormat.OpenXml，使用OpenXml可以对Word文件进行处理， 可以将Word中的所有文字解析并显示出来。 
再使用OpenXml插件中的WordprocessingDocument类来进行word文档中的文字提取。

开始标签<<w:body>> 表示文章的开头；

结束标签</<w:body>> 表示文章的结束；

<<w:rPr>>与 </<w:rPr>>是一对标签；
<<w:t>>：表示字符串，文字内容;

<<w:rpr>>：表示是<<w:r>>标签内的标签，对文本属性进行修饰;

<<w:p>>:表示段落;

<w:b w:val=”on”>>表示该格式串种的文本为粗体，而<<w:p>>一般是<<w:r>>的外层;

<w:b w:val=”on”> 表示该格式串种的文本为粗体;

<w:sz  w:val="80"/> 设置字号;

<w:rFonts   w:ascii="Arial" w:eastAsia="Arial" w:hAnsi="Arial" />设置字体;

……

<w:docPr> 
     <w:view w:val="print"/> 按页面显示;g

     <w:zoom w:percent="100"/> 显示比例100%


 
 
 
 
 

 


 
 
 
 