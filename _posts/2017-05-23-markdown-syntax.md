---
layout: post
title:  Markdown 语法学习
date:   2017-05-23 16:12:01 +0800
categories: document
tag: 其他
---

* content
{:toc}

简介
-------------
Markdown 是从文本到html的一种转换工具，相比于html，markdown更易读和写，下面就简单介绍一些markdown的基本语法。

对HTML的兼容
-------------
在markdown语言中可以兼容html标签，但是某些标签插入的时候有些特别，比如<div>、<table>、<p>、<pre>等，这些标签要独自成一行，才会被识别，不然就直接被当做文本了。

常用语法
-------------

#### **标题的显示**

setext显示标题的语法（注意在标题前面要空一行）

    这是 H1
    =============

    这是 H2
    -------------

atx显示标题的语法（注意#和文字之间的空格）
    # 这是 H1

    ## 这是 H2

    ###### 这是 H6

#### **引用**
    >   代表blockquote
    >>  区块里面内嵌区块

效果如下
>   代表blockquote
>>  区块里面内嵌区块

#### **列表**

##### 无序列表使用星号、加号或是减号作为列表标记
    * 第一项列表
    + 第二项列表
    - 第三项列表

效果如下：
* 第一项列表
+ 第二项列表
- 第三项列表

###### 有序列表则使用数字接着一个英文句点
    1. 第一项列表
    2. 第二项列表
    3. 第三项列表

效果如下：
1. 第一项列表
2. 第二项列表
3. 第三项列表

#### **代码块**
普通的段落缩进4个空格或者一个制表符

#### **分割线** （以下任意一种都行）

    * * *

    ***

    *****

    - - -

    ---------------------------------------

效果如下：

---------------------------------------

#### **链接**
行内式

行内式的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可。

    This is [an example](http://example.com/ "Title") inline link.

效果如下：

This is [an example](http://example.com/ "Title") inline link.

参考式

1.   参考式的链接是在链接文字的括号后面再接上另一个方括号，而在第二个方括号里面要填入用以辨识链接的标记。

2.   也可以选择性地在两个方括号中间加上一个空格，接着，在文件的任意处，你可以把这个标记的链接内容定义出来。

3.   也可以用隐式链接标记，只要在链接文字后面加上一个空的方括号

标记的链接内容定义：

+ 方括号（前面可以选择性地加上至多三个空格来缩进），里面输入链接文字

+ 接着一个冒号

+ 接着一个以上的空格或制表符

+ 接着链接的网址

+ 选择性地接着 title 内容，可以用单引号、双引号或是括弧包着

下面是用隐式链接的例子

    I get 10 times more traffic from [Google][] than from
    [Yahoo][] or [MSN][].

      [google]: http://google.com/        "Google"
      [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
      [msn]:    http://search.msn.com/    "MSN Search"

效果如下：

I get 10 times more traffic from [Google][] than from
[Yahoo][] or [MSN][].

  [google]: http://google.com/        "Google"
  [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
  [msn]:    http://search.msn.com/    "MSN Search"

#### **强调**
用 * 或者 _ 表示强调，一个 * 或者 _ 表示\<em>，两个表示\<strong>,如果要显示\*或者\_符号，可以直接在符号两边加个空格或者加上反斜杠\

    *single asterisks*

    _single underscores_

    **double asterisks**

    __double underscores__

效果如下：

*single asterisks*

_single underscores_

**double asterisks**

__double underscores__

#### **图片**
行内式

一个惊叹号 !，接着一个方括号，里面放上图片的替代文字，接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上 选择性的 'title' 文字。

    ![Alt text]({{ '/styles/images/logo.jpg' | prepend: site.baseurl  }} "Optional title")

效果如下：

![Alt text]({{ '/styles/images/logo.jpg' | prepend: site.baseurl  }} "Optional title")

参考式
一个惊叹号 !，接着一个方括号，里面放上图片的替代文字，接着一个方括号，是图片参考的名称，图片参考的定义方式则和连结参考一样

    ![Alt text][id]

    [id]: {{ '/styles/images/logo.jpg' | prepend: site.baseurl  }}  "Optional title attribute"

效果如下：

![Alt text][id]

[id]: {{ '/styles/images/logo.jpg' | prepend: site.baseurl  }}  "Optional title attribute"

