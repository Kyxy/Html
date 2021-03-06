## html与css的关系

1. html是网页内容的载体，内容指网页中的文本的标题、段落、图片、视频、链接等。
2. css是内容的样式、表现形式。例如文本中标题的颜色、字体或者为标题加入背景图片。css用来改变内容的外观，就像穿衣。
3. JavaScript是用来实现网页上的动态效果。例如鼠标滑过弹出下拉菜单、鼠标滑过表格的背景颜色改变、焦点新闻图片的轮换。用js来实现动画、交互等。

##### 认识标签

html标签用来标记网页中的内容，指明各部分分别是什么成分（标题、段落、图片、视频、连接等）。标记用来指明是什么。

标签由```<>```组成，html中标签成对出现，分为开始标签```<>```和结束标签```</>```，结束 标签比开始标签多了一个斜杠(slash)。html标签不区分大小写，但是**建议小写**。

##### html文件的基本结构

```html
<html>
	<head> ··· </head>
	<body> ··· </body>
</html>```
```

1. ```<html>···</html>```称为根标签，其他所有便签都嵌套在```<html>···</html>```内。

2. ```<head>···</head>```用于定义文档的头部，是所有头部元素的容器。头部元素包```<title>···</title>```、```<script>···</script>```、```<style>···<style>```、```<link>···</link>```、```<meta>```等等。
   ```<head>```标签描述了文档的头部属性和信息，包括文档的题目，会出现在浏览器的标题栏；其余大部分信息不会显示给用户。网页的```<title>```标签介绍网页的主要内容，方便用户或者搜索引擎判断。

3. ```<body>···</body>```标签间的内容是网页的主要内容，如标题标签```<h1>```~```<h6>```，段落标签```<p>```，图片标签```<img>```等

##### 标签的用途

**语义化**：将网页的内容以特定的标记来描述。使网页更容易被搜索引擎收录；浏览器更容易显示出网页的内容。

## 认识标签

##### span

**```<span>···<span>```标签：**为文字设置单独的样式。

   在```<head>```标签中嵌套```<style>```样式标签，在```<style>```中输入：

```html
      <style>
      	span{
      		color: red;
      		}
      </style>
```

  再选择```<body>```标签中要修改为指定样式的网页内容，以```<span>···</span>```包裹。 

##### q

**```<q>···</q>```标签：**短文本引用（quote）

##### blockquote

**```<blockquote>···</blockquote>```标签：**长文本引用。

##### p

**```<p>···</p>```标签：**标记段落文本。

##### h1

**```<h1>···</h1>```标签：**标记标题，总共有6级，标题字体均加粗，字号一次减小。

##### br

**```<br />```标签：**没有结束标签。语义：在html文档中实现换行功能。

##### 空格

**```&nbsp```标签：**实现空格功能，后面加一个分号。

##### 水平横线

**```<hr />```标签：**添加水平横线，没有结束标签。

##### 地址

**```<address>···</address>```标签：**为网页添加地址格式信息。

##### 单行代码

**```<code>···</code>```标签：**指明单行代码。

```python
print("hello world!")
```
##### 多行代码

**```<pre>···</pre>```标签：**在```<pre>```标签之间可以加入代码片段。```<pre>```标签间代码中的空格、换行符都将保留；还可以用在需要预格式化网页内容时。

```python
for i in range(10):
    print("hello world!")
```
##### 无序列表

**```<ul>···</ul>```标签：**网页中的无序列表信息。

```html
<ul>
  <li>信息</li>
  <li>信息</li>
  ···
</ul>
```
##### 有序列表

**```<ol>···</ol>```标签：**类似```<ul>```标签，只是每个信息前面有序序号，默认从1开始。

```html
<ol>
  <li>信心</li>
  <li>信息</li>
  ···
</ol>
```
##### div

**```<div>···<div>```标签：**在网页制作过程中可以将一些独立的逻辑部分划分出来，```<div>```标签作为逻辑部分的容器。

**逻辑部分：**指页面上一些相互关联的元素，如优酷的电视剧、电影、科技等分栏。为了使逻辑更加清晰，可以为一个独立的逻辑部分设置**唯一**的名称。

```html
<div id="名称">···</div>
```
##### 表格

**```<table>···</table>```标签：**用来创建网页中的表格。

创建表格的5个部分：以```<table>···</table>```开始、结束正个表格；```<tbody>···</tbody>```在```<table>```标签后（当表格内容很多时，表格会下载一点显示一点，加入```<tbody>```后，会下载完成再显示）；```<tr>···</tr>```表示表格的一行；```<td>···</td>```表示表格的一个单元格，有几个```<td>```表示表格有几行；```<th>···<th>```表示表格的表头单元格。

```<table>```在没有加入css样式前，浏览器默认不显示表格线；

使用```<table>```标签的summary属性可以为表格添加摘要，摘要内容不会出现在浏览器中，作用是增加表格的可读性；

```<caption>```表格标题```</caption>```可以为表格增加标题。

```html
<table summary="摘要">
  <tbody>
    <caption>表格标题</caption>
    <tr>
      <th>爱好</th>
      <th>姓名</th>
      <th>性别</th>
    </tr>
    <tr>
      <td>游泳</td>
      <td>lmd</td>
      <td>female</td>
    </tr>
    
    <tr>
    </tr>
    ···
  </tbody>
</table>
```
##### 链接

**```<a>···</a>```标签：**实现超链接，可以链接到另一个页面。

```title属性```：在鼠标滑过链接链接文本时显示的内容，可以用来介绍链接的网页;

```target属性```：当```target="_blank"时，在一个新创建的窗口中打开链接。

```html
<a href="链接" title="鼠标滑过显示的文本" target="_blank">链接文本</a>
```
##### mailto

**```mailto```属性：**在网页链接中实现链接email地址，使用```mailto```可以让访问者快速向网站管理者发送电子邮件。

收件人：电子邮件收件方；可以看到抄送方，看不到密抄方；

抄送：在发给收件人的同时，复制一份也发给抄送方；看得到收件方，看不见密抄方；```cc=```

密抄：在发送给收件人、抄送方的同时，秘密发送给的一方；看的见收件人、抄送方，但是多个密抄之间相互不可见。```bcc=```

```html
<a href="mailto:yy@imooc.com?cc=xiaoming@imooc.com&bcc=xiaoyu@imooc.com;xiaohong@imooc.com&subject=主题&body=邮件内容">点击文本</a>
```

```subject=```：邮件的主题；

```body=```：邮件的内容。

```mailto```可以通过单机链接，调用PC默认邮箱应用，并自动填入相应内容（收件人、抄送、密抄、邮件主题、邮件内容）

##### 图片

**```<img />```标签：**没有结束标签，为网页插入图片。

```html
<img src="图片地址" alt="下载失败时显示的文本" title="提示文本" />
```

```src```：图片的存储地址；

```alt```：当图像下载不成功时可以看见的提示文本；

```title```：对图片的描述，当鼠标滑过图片时可以看见的文本内容。

##### form

**```<form>···</form>```标签：**表单；

使用表单可以把浏览者输入的数据发送到服务器端，服务器可以处理用户发送过来的数据，然后反馈。

**语法：**

```html
<form  method="post/get" action="save.php">
	<label for="username">用户名:</label>
	<input type="text" name="username" />
	<label for="pass">密码:</label>
	<input type="password" name="pass" />
</form>
```

1. ```<form>···</form>```标签成对出现，一对```form```表示一个表单；
2. ``` action```：浏览者输入数据被传输到的地方，比如一个php页面（save.php）；
3. ```method```：数据传输的方式（post/get），属于后端考虑的问题。
4. 所有的表单控件（文本框```type="text"```、密码框```type="password"```、文本域```textarea```、单选框```type="radio"```、复选框```type="checkbox"```、下拉列表```select```、确定按钮```type="submit"```、重置按钮```type="reset"```、label等）都在```<form>···</form>```标签之间

##### 文本、密码输入

当用户需在表单中输入字母、数字等内容，需要使用输入框（文本框可以转化为密码框）。

语法：

```html
<form>
  <input type="text/password" name="名称" value="文本" />
</form>
```

1. ```type="text"```时：输入框为文本框；

   ```type="password"```时：输入框为密码框。（密码框中以黑点代替输入的内容显示）

2. ```name```：为文本框/密码框命名，供后台程序ASP、PHP使用。

3. ```value```：为输入框设置默认值（输入框中的提示字符）。 

##### 文本域

**```<textarea>···</textarea>```标签：**当用户需要在表单中输入大段文字时，需要用到文本域。

语法：

```html
<textarea rows="行数" cols="列数">默认值提醒</textarea>
```

1. ```rows```和```cols```分别代表输入框的行数和列数，这样个属性可以用css样式的```width```和```height```来代替；
2. ```<textarea>···</textarea>```之间是输入框中显示的默认值，可以用做提醒。

##### 单选框、复选框

在使用表单设计调查表时，使用选择框可以减少用户操作，html提供单选框和复选框两种。

语法：

```html
<input type="radio/checkbox" name="名称" value="值" checked="checked" />
```

1. ```type="radio"```时，控件为单选框；

   ```type="checkbox"```时，控件为复选框。

2. ```value```：提交到服务器的值；

3. ```name```：为控件命名，供后台ASP、PHP程序使用；

4. ```checked="checked"```时，该选项被默认选中。

**注意：**同一组单选按钮的```name```一定要一致，才能起到单选的作用。

##### 下拉列表

使用下拉列表节省网页的空间，可以单选，也可以复选（按住ctrl+单击鼠标）。

语法：

```html
<!--一个下拉表-->
<select mutiple="mutiple">
  <option value="read">read</option>
  <option value="write">write</option>
  <option value="listen" selected="selected">listen</option>
  <option value="speak">speak/option>
</select>
```

1. ```value```是向服务器提交的值，```<option>···</option>```是下拉列表个选项显示的值；
2. ```selected="selected"```属性：表示默认选中该项。
3. ```mutiple="mutiple"```属性：设置下拉列表可以复选，按住ctrl+鼠标单击。

##### submit按钮

在用户填写完成表单中的信息后，可以使用```submit```将表单信息提交到服务器供其处理并提供反馈。

语法：

```html
<input type="submit" value="提交" />
```

1. ```type="submit"```时，按钮才有提交作用；
2. ```value```：按钮上显示的文字。

##### reset按钮

在表单信息填写过程中发现有误，可以使用```reset```按钮将输入框恢复到初始状态，方便重新输入。

语法：

```html
<input type="reset" value="重置" />
```

1. ```type="reset"```时，按钮才有重置作用；
2. ```value```：按钮上显示的文字。

##### label

```<label>```标签的作用是将标签内的文本与其他控件相关联（使用相同的```id```属性），在鼠标选中```label```标签中的文本时，浏览器自动将焦点转到与其相关的控件上。比如单选按钮，选择```label```标签中的文字会选择与之相关的单选按钮。

语法：

```html
<label for="控件id属性名称">文本</label>
```

注：label标签的```for```属性中的值与相应控件的```id```属性值一定要相同。

例子：

```html
<form>
  <label for="male">male</label>
  <input type="radio" name="people" id="male" />
  <br />
  <label for="female">female</label>
  <input type="radio" name="people" id="female" />
</form>
```





























































































