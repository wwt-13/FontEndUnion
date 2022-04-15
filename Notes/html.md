# day1

可以直接类比面向对象的思想

所有的标签都是一个object(具备属性和方法)

## 关于HTML的基本骨架(HTML skeleton)

1. head
   
2. body
   
3. footer(可选)

## head部分

### 关于meta标签的通用属性

> (head element参考工具书)[https://htmlhead.dev/]

```html
<meta charset="UTF-8" />
<meta http-equiv="X-UA-Compatible" content="IE=edge" />
<meta name="robots" content="index, follow">
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<meta name="description" content="教导熊猫相关的基本知识" />
<meta name="author" content="Wwt" />
```

### base标签

- Base tag specify the *base attributes* of all elements inside the HTML file
- base必须定义一个target和href(这里不讨论)
- base元素中的href属性用于指定一个文档包含的所有相对url的根url，一个html文件中只能有一份base元素

这里详细讲讲base元素的另外一个属性**target**
> 默认浏览上下文的关键字或者作者定义的名称，当没有明确目标的链接a或者表单form
> 导致导航被激活时显示其结果

- _self: 载入结果到当前浏览上下文中。（该值是元素的*默认值*）。
- _blank: 载入结果到一个新的未命名的浏览上下文。
- _parent: 载入结果到父级浏览上下文（如果当前页是内联框）。如果没有父级结构，该选项的行为和_self一样。
- _top: 载入结果到顶级浏览上下文（该浏览上下文是当前上下文的最顶级上下文）。如果没有父级，该选项的行为和_self 一样。

## body部分

### 常见标签汇总

#### 标题标签h1-h6

`注意`：标题标签真正决定的是标题的重要程序，大小样式都可以在css样式表中设定

> so easy, 可以直接跳过
> 如果标题不够用的话，可以进行自定义标题或者重新架构你的网页结构
> （因为正常的网页也不需要那么多详细分级，可以考虑开子网页了）

#### anchor tag

> 是用于建立超链接用的（非常简单，不赘述）
> 讲一些如何跳转到新页面(不覆盖原本页面)
> 这种功能需要定义在head标签里

`<a href="https://www.baidu.com"></a>`

#### img tag

找无版权图片的话

1. google搜索+tools设置为无版权
2. (unplash)[https://unsplash.com/]

img标签的使用也非常简单
- src:是文件的绝对路径 or 相对路径
- alt:是alternative，在你打错路径或者某些地方出错的话就会显示alt中的内容


`<img src="your image path" alt="alternative content">`

#### 列表ul和ol

> HTML中的两种列表:无序列表+有序列表
> (因为这些之前已经学过了，所以不多说)

#### HTML表格

> thead和tbody完全就是为了规范代码而写的，其实没啥用
> tfoot的话，可以用于指定一行特殊的行，比方说求和什么的

```html
<table>

</table>
```

#### **HTML表单**

> HTML中的表单需要进行前后端的交互，前端输入数据，并将数据传送给后端

各种参数介绍

- action:你的资料传送的目的地


##### input types

1. checkbox
2. email
3. file
4. number
5. password
6. radio
7. range

##### input attributes

1. checked
2. max
3. min
4. maxlength
5. minlength
6. placeholder
7. required
8. value


### block and inline elements

> 大体上可以把html的标签分为两类，一类是block，另外一类是inline

block的特点，"width=device"，排版的时候长度等于页面长度
但是这样说其实还是不太准确
使用css解释的话，应该是
tag{
    witdh:100%;
}
也就是说width=100parent element's width


就像img标签和a标签就是，同时放置两个标签，新的标签会默认出现在旧的标签的右侧(inline,不会默认换行)

而h标题标签就是典型的block标签(自带换行)

- 常见的块级元素：DIV, FORM, TABLE, P, PRE, H1~H6, DL, OL, UL
- 常见的内联元素：SPAN, A, STRONG, EM, LABEL, INPUT, SELECT, TEXTAREA, IMG, BR 等。
- 一般来说，可以通过display:inline和display:block的设置来改变元素的布局

### div,br,hr的基本使用

- div:The Content Division element,它没有任何渲染效果，它是一个通用的容器(纯容器),可以把一个inline元素包裹为block元素，其余渲染效果全部通过设置css渲染实现
- br:就是一个简单的换行标签(非常简单)
- hr:就是简单的分割线标签(同样非常简单)

### entity codes(实体代码)

> 比较好的一个特性就是，它不是一张图片，而是文字
> 1. HTML处理效率会高很多
> 2. 内存占用也很小
> 3. 能被css和文字相关的样式渲染
> 关键是处理效率非常高
> 在HTML中如果想要打出各种特殊符号(比如各种罗马字符、音乐符号等等)，就需要使用entity codes
(HTML Symbols)[https://www.htmlsymbols.xyz/]

### index.html

> why index.html?
> 全世界公认，index.html是默认html项目中最中心的项目文件

### icon设定

> 就像下面这幅图，小标签左侧显示的就是网页的标签(比如说我自己写的网站未配置icon，显示的就是默认图标)
![](https://gitee.com/ababa-317/image/raw/master/images/image-20220408165229532.png)
> 需要写在head里面