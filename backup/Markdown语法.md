## 1 Markdown.com.cn 简介

- 支持自定义样式的 Markdown 编辑器
- 支持微信公众号、知乎和稀土掘金
- 点击右上方对应图标，一键复制到各平台

## 2 Markdown语法教程

### 2.1 标题

Markdown 支持两种标题的语法，类 Setext 和类 atx 形式。

* 类 Setext 形式是用底线的形式来区分标题，利用等号（=）和减号（-）分别表示一级标题和二级标题。

这是一级标题
=================

这是二级标题
-----------------

* 类 Atx 形式则是在行首插入 1 到 6 个 # ，对应到标题 1 到 6 级。

# 这是一级标题
## 这是二级标题
### 这是三级标题
#### 这是四级标题
##### 这是五级标题
###### 这是六级标题

### 2.2 字体

粗体**、*斜体、***粗体和斜体，两个波浪删除线`~~`，需要在文字前后加不同的标记符号 。如下：

**这个是粗体**

*这个是斜体*

***这个是粗体加斜体***

~~要被加上删除线的文字~~

* 下划线
语法：通过 HTML 的 <u>​ 标签来实现

<u>带下划线的文本</u>


注：如果想给字体换颜色、字体或者居中显示，需要使用内嵌HTML来实现。

### 2.3 无序列表

无序列表使用星号（*）、加号（+）或是减号（-）作为列表标记。

- 无序列表 1
- 无序列表 2
- 无序列表 3

如果要控制列表的层级，则需要在符号`*`或者`+`或者`-`前使用空格。如下：

- 无序列表 1
- 无序列表 2
  - 无序列表 2.1
  - 无序列表 2.2


### 2.4 有序列表

有序列表的使用，在数字及英文符号`.`后加空格后输入内容，如下：

1. 有序列表 1
2. 有序列表 2
3. 有序列表 3

### 2.5 引用

引用的格式是在符号`>`后面书写文字。块引用可以嵌套在符号`>>`还支持如下：

> 第一层
>> 第二层
>>>第三层

> 区块中使用列表
> 1. 第一项
> 2. 第二项
> * 111
> * 222


### 2.6 任务列表

- [ ] 未完成的任务
- [x] 已完成的任务


### 2.7 链接

Markdown 支持两种形式的链接语法：行内式和参考式。

* 行内式链接只要在方块括号后面紧接着圆括号并插入网址链接即可。

[链接名称](链接地址)

也可以用尖括号将 URL 或 Email 地址变为可点击的链接，示例：

<http://www.google.com>

这里得额外说下，链接还可以用变量来代替。

什么意思呢？有些情况下，一个超链接会经常出现在文章中，那么文章内容就会显得很冗余：

```
[谷歌](http://www.google.com)（Google），这个全球知名的科技公司，
以其卓越的技术和丰富的产品线，深刻影响着我们的生活。
以下，我将带您领略[谷歌](http://www.google.com)的魅力，探索其丰富的互联网生态。

[谷歌](http://www.google.com)，这个充满创新和智慧的科技公司，
正以其强大的技术实力和丰富的产品线，不断改变着我们的世界。
让我们一起感受[谷歌](http://www.google.com)的魅力，探索更多未知的精彩！
```

此外，这样还有一个缺点，就是如果网址失效了，还得逐个替换。

为此，我们可以用变量的语法（注意，两个都是方括号）：

[Google][1]

然后在文档的结尾（或其他位置），给这个变量 1​ 复制：

 [1]: http://www.google.com/


### 2.8 图片

插入图片，图片的语法和链接很像，区别在一个 ! 开头，格式如下：

![图片说明](图片链接)


![图片](https://raw.githubusercontents.com/xugaoyi/image_store/master/blog/md_logo.png)
![图片](C:\Documents\wife.png)

此外，还可以使用 HTML 的 img 标签，优点是可以设置图片宽高：

<img src="https://raw.githubusercontents.com/xugaoyi/image_store/master/blog/md_logo.png" width="50px" height="30px">

PS：图片也可以用超链接的那个变量语法

![图片][img]

[img]: https://raw.githubusercontents.com/xugaoyi/image_store/master/blog/md_logo.png


### 2.9 分割线

可以在一行中用三个以上的减号` - ` 或 星号` *` 底线`-`来建立一个分隔线，也可以在星号或是减号中间插入空格，同时需要在`分隔线`的上面**空一行**。如下：

---
或

***
或

- - -



### 2.10 表格

Markdown 使用管线图来创建表格，每列用 | 分隔，表头与表身用 ---|---|---分隔。可以使用冒号来定义表格的对齐方式，

```
​-:​ ​：设置内容和标题栏居右对齐
:-​： 设置内容和标题栏居左对齐
:-​ : 设置内容和标题栏居中对齐
```
效果如下：

| 左对齐 | 右对齐 | 居中对齐 |
| :-----| ----: | :----: |
| 单元格 | 单元格 | 单元格 |
| 单元格 | 单元格 | 单元格 |


支持 emoji

在 emoji 表情的英文名前后加上冒号即可，语法：
:smirk:

想知道更多 emoji，可以去搜索，例如 [webfx.com/tools/emoji-cheat-sheet](https://www.webfx.com/tools/emoji-cheat-sheet/)

## 3. 特殊语法

### 3.1 脚注

* 脚注是对文本的补充说明，语法：

[^脚注]

然后在文件末尾或其他位置给“脚注”添加内容，语法格式：

[^脚注]: 这是脚注的内容


* 脚注与链接的区别如下所示：

```markdown
链接：[文字](链接)
脚注：[文字](脚注解释 "脚注名字")
```

有人认为在[大前端时代](https://en.wikipedia.org/wiki/Front-end_web_development "Front-end web development")的背景下，移动端开发（Android、IOS）将逐步退出历史舞台。

[全栈工程师](是指掌握多种技能，并能利用多种技能独立完成产品的人。 "什么是全栈工程师")在业务开发流程中起到了至关重要的作用。

注意：有些网站/编辑器不支持该语法

### 3.2 上标/下标

有时候需要输入上标或者下标，例如：

2^2^
H~2~O

注意：部分编辑器不支持，Typora 的话需要在设置里开启该功能。

### 3.3 代码块


如果在一个行内需要引用代码，只要用反引号引起来就好，如下：

Use the `printf()` function.

在需要高亮的代码块的前一行及后一行使用三个反引号，同时**第一行反引号后面表示代码块所使用的语言**，如下：

```java
// FileName: HelloWorld.java
public class HelloWorld {
  // Java 入口程序，程序从此入口
  public static void main(String[] args) {
    System.out.println("Hello,World!"); // 向控制台打印一条语句
  }
}
```

支持以下语言种类：

```
bash
clojure，cpp，cs，css
dart，dockerfile, diff
erlang
go，gradle，groovy
haskell
java，javascript，json，julia
kotlin
lisp，lua
makefile，markdown，matlab
objectivec
perl，php，python
r，ruby，rust
scala，shell，sql，swift
tex，typescript
verilog，vhdl
xml
yaml
```

如果想要更换代码高亮样式，可在上方**代码主题**中挑选。

其中**微信代码主题与微信官方一致**，有以下注意事项：

- 带行号且不换行，代码大小与官方一致
- 需要在代码块处标志语言，否则无法高亮
- 粘贴到公众号后，用鼠标点代码块内外一次，完成高亮

diff 不能同时和其他语言的高亮同时显示，且需要调整代码主题为微信代码主题以外的代码主题才能看到 diff 效果，使用效果如下:

```diff
+ 新增项
- 删除项
```

**其他主题不带行号，可自定义是否换行，代码大小与当前编辑器一致**

### 3.4 数学公式


行内公式使用方法，比如这个化学公式：$\ce{Hg^2+ ->[I-] HgI2 ->[I-] [Hg^{II}I4]^2-}$

块公式使用方法如下：

$$H(D_2) = -\left(\frac{2}{4}\log_2 \frac{2}{4} + \frac{2}{4}\log_2 \frac{2}{4}\right) = 1$$

矩阵：

$$
  \begin{pmatrix}
  1 & a_1 & a_1^2 & \cdots & a_1^n \\
  1 & a_2 & a_2^2 & \cdots & a_2^n \\
  \vdots & \vdots & \vdots & \ddots & \vdots \\
  1 & a_m & a_m^2 & \cdots & a_m^n \\
  \end{pmatrix}
$$

公式由于微信不支持，目前的解决方案是转成 svg 放到微信中，无需调整，矢量不失真。

目前测试如果公式量过大，在 Chrome 下会存在粘贴后无响应，但是在 Firefox 中始终能够成功。

### 3.6 设置目录TOC

TOC 全称为 Table of Content，列出全部标题。

自动根据该文件的所有标题来生成一个目录，一般在文章最顶部使用。语法：

[TOC]

注意：有些编辑器不支持。

> [!TIP]
> 如果你使用 VuePress 搭建博客，请使用 [[toc]]​，不过 VuePress 一般会自动生成目录，不用额外在文章顶部用该语法

### 3.6 注音符号

支持注音符号，用法如下：

Markdown Nice 这么好用，简直是{喜大普奔|hē hē hē hē}呀！

### 3.7 横屏滑动幻灯片

通过`<![](url),![](url)>`这种语法设置横屏滑动滑动片，具体用法如下：

<![蓝1](https://markdown.com.cn/images/blue.jpg),![绿2](https://markdown.com.cn/images/green.jpg)>


## 4 GitHub 风格的警报

### 4.1 `笔记`、`提示`、`重要的`、`警告`、`警告` 。

> [!NOTE]
> 突出显示用户应该考虑的信息，即使用户浏览时也应考虑.

> [!TIP]
> 帮助用户取得更大成功的可选信息.

> [!IMPORTANT]
> 用户成功所必需的关键信息.

> [!WARNING]
> 由于存在潜在风险，关键内容需要用户立即关注.

> [!CAUTION]
> 某一行为的潜在负面后果.


## 5 其他语法

### 5.1 HTML

支持原生 HTML 语法，请写内联样式，如下：

<span style="display:block;text-align:right;color:orangered;">橙色居右</span>
<span style="display:block;text-align:center;color:orangered;">橙色居中</span>

不在 Markdown 语法涵盖范围之内的标签，都可以直接在文档里面用 HTML 撰写。

目前支持的 HTML 元素有：<kbd> <b> <i> <em> <sup> <sub> <br>等等 ，如：

使用 <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Del</kbd> 重启电脑


### 5.2 UML

### 5.3 转义符号

之前说过，井号 #​ 是 Markdown 的标题标记，>​ 是引用标记。

而有时候我们想单独展示某个 Markdown 的标记，也就是不想让 Markdown 标记生效，可以在标记的每个符号前加上反斜杠（\​），这样这些符号将按原样显示，不再具有 Markdown 中的特殊意义。如：

不想让引用块标记生效，可以使用 \>​，这样页面将渲染为 >​

不想让二级标题标记生效，可以使用 \#\#​，将显示为 ##​

