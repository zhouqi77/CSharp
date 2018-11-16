# 第四次作业  

#  实验目的和要求

- 本实验在上一个实验（实验3）的基础上进行。要求对每个考生的答卷（docx文档）进行自动阅卷并评分，最后把评分写入一个二进制文件中。
- 样例文件在老师的test4目录中。本实验的输入是：原题.docx，标准答案.docx，以及考生答案目录(students_answer)，在考生答案目录中存放的是考生的作答文件，每个考生文件的命名方式是考号_姓名.docx。程序必需能够自动对考生答案目录中的每个文件进行评分。
- 本实验的输出是一个二进制成绩结果文件。比如result.dat，这个文件的中存放了每个考生的个人信息和成绩。
- 本实验必须能够写result.dat文件，并且把文件内容再正确的读出来。

# 知识点

- LCS
- 泛型
- 运算符重载
- 二维数组
- 递归调用
- 使用VS2017中的NuGet安装项目的外部引用。
- 熟悉Word文件的XML格式。
- 熟悉XML格式及OpenXmlElement处理，熟悉XML中对象的遍历。

# 实验步骤：

- 创建一个Windows的窗体应用程序，找到工具箱，首先拖动splitContainer进主体中，然后将Orientation 的值设置为Horizontal，使得容器呈上下排布，接着拖动按钮，文本框，标签等。

- 通过双击对应的部件可以进入设置事件之类的.cs文件中，在这里进行逻辑响应事件等的设置。

- 我们设置了一个链接标签进行路径的选择，然后将路径显示在文本框中。

- 利用前面已经写好的LCS对比，创建这些类。这里会新建三个类文件。

- 写文件，主要用FileStream流的方法，先创建一个.dat文件用于存放二进制文件，然后获取学生的分数， 接着将版本号信息，考试要求，学生数量等转化为字节流数组存储，之后是通过Write()将这些信息写入文件中， 最后是学生信息，因为有多个学生，按每个学生信息存储，所以使用for循环，一个一个的将信息转化为字节流数组再写入文件。

- 读文件，主要是将每个部分分开读然后将我们需要的主要的数据ID，姓名，分数等存储到一个独立的LIst链表中传递到Form中进行显示。

- 在Form中，得到需要的路径，然后通过for循环，一组一组的将数据显示到数据列表中。

# 运行结果


![ImageText](http://m.qpic.cn/psb?/V10AubBI1movr3/NAubiZKbwyb4MQjf6mVTzkwSfuS0ubeOYfgvUw82EvA!/b/dDUBAAAAAAAA&bo=CwOhAAAAAAADB4s!&rf=viewer_4 )

![ImageText](http://m.qpic.cn/psb?/V10AubBI1movr3/H4a9dpmI5gGgv7tzIZVAiJX5aX0Qdne*aiT55Jw8XlA!/b/dAgBAAAAAAAA&bo=ogKgAQAAAAADFzM!&rf=viewer_4 )

![ImageText](http://m.qpic.cn/psb?/V10AubBI1movr3/4xvL9qKVryafoK6oz9XTpN1gaY78Sx53zVoSBDMctb4!/b/dFYBAAAAAAAA&bo=gwKIAQAAAAADFzo!&rf=viewer_4 )
