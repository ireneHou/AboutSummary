# Markdown 文档

---

## Markdown 概述 [Overview]


-------------------------------------------------------------------------

### Markdown 标题 [Title]

__setext形式__ 使用来等号来表示一级标题, 使用连字符表示二级标题。任意长度的 <kbd>=</kbd> 或 <kbd>-</kbd> 都是可以的。

__atx形式__ 在行首插入 1 到 6 个 <kbd>#</kbd>，对应 1-6 级标题。

___语法示例：___ 
```javascript
我是一级标题
===========
我是二级标题
-----------

# 一级标题
## 二级标题
……
###### 六级标题
```

___效果如下：___

这是一级列表
===========

## 这是二级列表

-------------------------------------------------------------------------

### Markdown 段落格式 [Paragraph]

Markdown 段落没有特殊的格式，直接编写文字就好，段落的换行是使用**两个以上空格加上回车**  

__字体强调：__ 在文字两端加上星号 <kbd>*</kbd> 或下划线 <kbd>_</kbd> 可作为强调标记。斜体一个，粗体两个，斜粗体三个。  

__分隔线：__ 一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。 

__删除线：__ 如果段落上的文字要添加~~删除线~~，只需要在文字的两端加上两个波浪线 ~~ 即可。  

__下划线：__ <u>下划线</u>可以通过 HTML 的 <u\> 标签来实现。  

__脚注：__ 脚注是对文本的补充说明。[^RUNOOB]。  

_这个有问题_[^RUNOOB]: 菜鸟教程 -- 学的不仅是技术，更是梦想！！！

___语法示例：___ 
```javascript
**字体强调**
下面是分割线
---
~~删除线~~
<u>下划线</u>
```

___效果如下：___

**字体强调**    
~~删除线~~    
<u>下划线</u>    
创建脚注格式类似这样 [^RUNOOB]。

[^RUNOOB]: 菜鸟教程 -- 学的不仅是技术，更是梦想！！！

-------------------------------------------------------------------------

### Markdown 列表 [List]

Markdown 支持有序列表和无序列表。  

**无序列表** 使用星号 <kbd>*</kbd> 、加号 <kbd>+</kbd> 或是减号 <kbd>-</kbd> 作为列表标记，这些标记后面要添加一个空格，然后再填写内容。

**有序列表** 使用数字并加上 <kbd>.</kbd> 号来表示。 

**列表嵌套** 只需在子列表中的选项前面添加四个空格即可。

___语法示例：___ 
```javascript
* Red
+ Green
- Blue

1. Red
    * Green
2. Blue
```

___效果如下：___

* 无序列表 1
    1. 有序列表
* 无序列表 2
    - 无序列表 1

-------------------------------------------------------------------------

### Markdown 区块 [Block]

**区块引用** 是在段落开头使用 <kbd>></kbd> 符号，后面紧跟一个空格符号。区块是可以嵌套的，一个 > 符号是最外层，两个 > 符号是第一层嵌套，以此类推。块引用可以包含 Markdown 元素, 包括标题, 列表和代码块:

___语法示例：___ 
```javascript
> ## This is a header.
>
> 1. This is the first list item.
> 2. This is the second list item.
>
> > This is nested blockquote.
```

___效果如下：___

> ## This is a header.
>
> 1. This is the first list item.
> 2. This is the second list item.
>
> > This is nested blockquote.

-------------------------------------------------------------------------

### Markdown 代码 [Code]
 
要输出一个代码片段需要使用重音符号 <kbd>`</kbd>，不同于预格式的代码块, 代码片段只是在普通段落中标识出代码。要在代码片段中包含字面量的重音符号, 可以使用多个重音符号作为起始和结束标记。

__代码区块__ 使用 4 个空格或者一个制表符 <kbd>Tab</kbd> 键,也可以用 <kbd>```</kbd> 包裹一段代码，并指定一种语言（也可以不指定）    

___语法示例：___ 

    
    ```javascript
    alert('there show code')
    ```

    Use the `printf()` function.
    ``There is a literal backtick (`) here.``

___效果如下：___

```javascript
alert('there show code')
```
Use the `printf()` function.    
``There is a literal backtick (`) here.``    

-------------------------------------------------------------------------

### Markdown 链接 [Link]

Markdown 支持两种链接形式: 内联 和 引用，这两种形式下链接文本的定界符都是 [中括号]。   

__内联链接：__
+ 语法：`[链接名称](链接地址 "可选标题")` 或 `<链接地址>`
+ 只需在链接文本的右括号后面紧接一对圆括号，圆括号里面放所需的 URL 链接, 还可以放一个 可选 的链接标题, 标题要用引号包围。   
+ 如果是引用相同服务器下的本地资源, 还可以用相对路径。

__引用类型的链接：__
+ 语法：
    + `[链接名称][变量]`
    + 在文档的结尾为变量赋值`[变量]: 链接地址 “可选标题”` 或 `[变量]: 链接地址 (可选标题)`
+ 链接标签：
    + 方括号中包含链接标识符 (可以用三个以上的空白符来添加缩进);
    + 跟着是冒号;
    + 跟着是一个以上的空白符和水平制表符;
    + 跟着是链接的 URL;
    + 跟着是可选的标题属性, 可以用单引号, 双引号, 或者圆括号包围。

___语法示例：___ 
```text
This is [an example](http://example.com/ "Title") inline link.
See my [About](/about/) page for details.

This is [an example][inlineLink] reference-style link.

[inlineLink]: http://example.com/  "Optional Title Here"
```

___效果如下：___

This is [an example](http://example.com/ "Title") inline link.    
See my [About](/about/) page for details.    
This is [an example][inlineLink] reference-style link.

[inlineLink]: http://example.com/  "Optional Title Here"

-------------------------------------------------------------------------

### Markdown 图片 [Image]

Markdown 使用了类似链接的语法来插入图片, 包含两种形式: 内联 和 引用。  

__内联图片：__  
+ 语法：`![Alt 属性文本](图片地址 "可选标题")`
+ 一个感叹号: !;
+ 紧跟着一对方括号, 包含了图片的 alt 属性;
+ 紧跟着一对圆括号, 包含了图片的 URL 或者路径, 以及一个可选的用单引号或双引号包裹的 title 属性。  

_效果如下：_

![Alt text](http://static.runoob.com/images/runoob-logo.png "Optional title")

__引用图片：__ 
+ 语法：`![Alt 属性文本][变量]`
+ 在文档的结尾为变量赋值`[变量]: 图片地址 “可选标题”`

_效果如下：_

![Alt text][inlineImg]

[inlineImg]: http://static.runoob.com/images/runoob-logo.png "Optional title attribute"

> Markdown 没有语法指定图片尺寸; 如果需要指定图片尺寸, 可以使用 HTML <img> 标签.

-------------------------------------------------------------------------

### Markdown 表格 [Table]

Markdown 制作表格使用 | 来分隔不同的单元格，使用 - 来分隔表头和其他行。

__表格__
+ 语法：
    + `|  表头  | 表头  |`
    + `|  ----   |  ----  |`
    + `| 单元格 | 单元格 |`
    + `| 单元格 | 单元格 |`
+ 对齐方式：
    + __-:__ 设置内容和标题栏居右对齐。
    + __:-__ 设置内容和标题栏居左对齐。
    + __:-:__ 设置内容和标题栏居中对齐。     

_效果如下：_

 | 左对齐 | 右对齐 | 居中对齐 |
 | :-----| ----: | :----: |
 | 单元格 | 单元格 | 单元格 |
 | 单元格 | 单元格 | 单元格 |

-------------------------------------------------------------------------

### Markdown 高级技巧 [Advanced Skills]

__支持的 HTML 元素__    

不在 Markdown 涵盖范围之内的标签，都可以直接在文档里面用 HTML 撰写，目前支持的 HTML 元素有：`<kbd>` `<b>` `<i>` `<em>` `<sup>` `<sub>` `<br>`等。    

> 使用 <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Del</kbd> 重启电脑

__转义__

Markdown 使用了很多特殊符号来表示特定的意义，如果需要显示特定的符号则需要使用转义字符，Markdown 使用反斜杠转义特殊字符：

__公式__

当你需要在编辑器中插入数学公式时，可以使用两个美元符 $$ 包裹 TeX 或 LaTeX 格式的数学公式来实现。提交后，问答和文章页会根据需要加载 Mathjax 对数学公式进行渲染。

-------------------------------------------------------------------------

> ## 参考资料
> 
> 1. https://www.runoob.com/markdown/md-paragraph.html
> 2. https://markdown-zh.readthedocs.io/en/latest/
> 3. 

*************************************************************************

### 谷歌浏览器查看.md文件 [Mardown Preview In Chrome]

_1. 下载Chrome插件：Markdown Preview Plus_  
Step1：更多工具  
Step2：扩展程序  
Step3：点击左侧 “拓展程序” 底部的 “打开chrome网上应用商店”  
Step4：输入并下载 “Markdown Preview Plus”  
<u>**Important：**chrome的 “扩展程序” 中设置：勾选上 “允许访问文件网址” </u>  

_2. 使用_  
Step1：点击右侧icon图标，弹出小菜单  
Step2：取消勾选 “Disable render markdown”  
Step3：“Set theme for this page:” 行选择 “TopMarks”  (个人喜欢YetAnotherGithub)

_3. 重新刷新当前页面即可应用_  
