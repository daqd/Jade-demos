## 前言
之后再补充

> 实例代码传送门：

> git@github.com:daqd/Jade-demos.git

## 安装
 跟一般的npm安装依赖包没太大的区别，一行命令就此带过：
 
 `npm install -g jade `


## 完整小实例

输出一个hello word!

创建一个*.jade文件，写入一下代码：

```
doctype html
html
	head
		title hello world
	body
		p hello world
```
进入终端，切换至jade文件所在目录，输入以下命令编译文件：

`jade test.jade`

格式化输出文件

`jade -P test.jade`

格式化并监控自动编译文件

`jade -P -w test.jade`

编译输出的文件应该是酱紫的：

```
<!DOCTYPE html>
<html>
  <head>
    <title>hello world</title>
  </head>
  <body>
    <p>hello world</p>
  </body>
</html>
```
So easy~~

开始jade基础语法的练习。

## Jade 基础语法

### 标签
html的标签分为两种，闭合标签和自闭合标签，在jade里，都一视同仁了，如果想输出一个div,直接在jade文件里，输入：

```
	div
```
编译完应该是酱紫的：

```
	<div></div>
```
如果想输出一个自闭合的标签，如input,img等，直接像上面一样编写就可以了。

### 标签属性
每一个标签都有各自的属性，jade中的标签的属性也是So easy~

#### class/id

```
	div.className1
	div#idName1
```
也可以简写成：

```
	.className1
	#idName1
```
编译完，应该是酱紫的：

```
	<div class="className1"></div>
	<div id="idName1"></div>
```
#### 其它属性

如img的`src`，`style`，`data-XXX`的自定义属性值，可以这么来写：

```
img(src="./img/demo1.png",data-XXX="米小米")
```











