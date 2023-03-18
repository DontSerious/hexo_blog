---
title: markdown in vscode
date: 2023-03-12 15:28:35
categories:
- VSCode

tags:
- Memo
- Markdown
---
- [1. 基础语法](#1-基础语法)
  - [1.1. 标题](#11-标题)
  - [1.2. 段落](#12-段落)
  - [1.3. 换行](#13-换行)
  - [1.4. 粗体和斜体](#14-粗体和斜体)
  - [1.5. 引用](#15-引用)
  - [1.6. 列表](#16-列表)
    - [1.6.1. 有序列表](#161-有序列表)
    - [1.6.2. 无序列表](#162-无序列表)
  - [1.7. 代码](#17-代码)
  - [1.8. 分割线](#18-分割线)
  - [1.9. 链接](#19-链接)
  - [1.10. 图片](#110-图片)
  - [1.11. 表格](#111-表格)
    - [1.11.1. 对齐](#1111-对齐)
  - [1.12. 删除线](#112-删除线)
  - [1.13. 任务列表](#113-任务列表)
- [2. Markdown Support for Visual Studio Code](#2-markdown-support-for-visual-studio-code)
  - [2.1. Table of contents](#21-table-of-contents)
  - [2.2. Table formatter](#22-table-formatter)

# 1. 基础语法

## 1.1. 标题
以#号的数量代表标题级别，越少级别越高。
```markdown
// 一定在井号后面留空格
# 一级标题
## 二级标题
### 三级标题
```

## 1.2. 段落
空白一行或多行进行分隔。
```markdown
第一行

第二行
```
*不要用空格（spaces）或制表符（ tabs）缩进段落。*

## 1.3. 换行
在一行的末尾添加两个或多个空格，然后按回车键，即可创建一个换行。

## 1.4. 粗体和斜体
都是使用星号(*)包裹，下划线(_)也可
```markdown
*斜体*
_斜体_
**粗体**
__粗体__
***又粗又斜***
___又粗又斜___
```

## 1.5. 引用
```markdown
> 代表引用
>> 可嵌套
```
效果如下：  
> 代表引用
>> 可嵌套

## 1.6. 列表
引用和列表可以相互嵌套
### 1.6.1. 有序列表
```markdown
1. 
2. 
    1. 
    2. 
3. 
```
### 1.6.2. 无序列表
```markdown
- 1
- 2
- 3
```
效果如下：  
- 1
- 2
- 3

## 1.7. 代码
要将单词或短语表示为代码，请将其包裹在反引号 (`) 中。
```markdown
At the command prompt, type `nano`.
```
效果如下：  
At the command prompt, type `nano`.

如果你要表示为代码的单词或短语中包含一个或多个反引号，则可以通过将单词或短语包裹在双反引号(``)中。
```markdown
``Use `code` in your Markdown file.``
```
效果如下：  
``Use `code` in your Markdown file.``

## 1.8. 分割线
要创建分隔线，请在单独一行上使用三个或多个星号 (***)、破折号 (---) 或下划线 (___) ，并且不能包含其他内容。  
以上三个分隔线的渲染效果看起来都一样，效果：

---

*记得在分割线上下添加空白行*
```markdown
Try to put a blank line before...

---

...and after a horizontal rule.
```

## 1.9. 链接
超链接Markdown语法代码：`[超链接显示名](超链接地址 "超链接title")`
```markdown
这是一个链接 [Markdown语法](https://markdown.com.cn)。
```
效果如下：
这是一个链接 [Markdown语法](https://markdown.com.cn)。

## 1.10. 图片
要添加图像，请使用感叹号 (!), 然后在方括号增加替代文本，图片链接放在圆括号里，括号里的链接后可以增加一个可选的图片标题文本。

插入图片Markdown语法代码：`![图片alt](图片链接 "图片title")。`

给图片增加链接，请将图像的Markdown 括在方括号中，然后将链接添加在圆括号中。  
例如：
`[![沙漠中的岩石图片](/assets/img/shiprock.jpg "Shiprock")](https://markdown.com.cn)`

## 1.11. 表格
要添加表，请使用三个或多个连字符（---）创建每列的标题，并使用管道（|）分隔每列。您可以选择在表的任一端添加管道。
```markdown
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |
```
效果如下：
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |
### 1.11.1. 对齐
您可以通过在标题行中的连字符的左侧，右侧或两侧添加冒号（:），将列中的文本对齐到左侧，右侧或中心。
```markdown
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |
```
效果如下：
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |

## 1.12. 删除线
您可以通过在单词中心放置一条水平线来删除单词。结果看起来像这样。此功能使您可以指示某些单词是一个错误，要从文档中删除。若要删除单词，请在单词前后使用两个波浪号~~。
```markdown
~~世界是平坦的。~~ 我们现在知道世界是圆的。
```
效果如下：  
~~世界是平坦的。~~ 我们现在知道世界是圆的。

## 1.13. 任务列表
任务列表使您可以创建带有复选框的项目列表。在支持任务列表的Markdown应用程序中，复选框将显示在内容旁边。要创建任务列表，请在任务列表项之前添加破折号-和方括号[ ]，并在[ ]前面加上空格。要选择一个复选框，请在方括号[x]之间添加 x 。
```markdown
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
```
效果如下： 
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media

# 2. Markdown Support for Visual Studio Code
## 2.1. Table of contents
- tab `shift + ctrl + p` and type "Create Table of Contents" to insert a new table of contents.
- Easily add/update/remove section numbering
    - tab `shift + ctrl + p` and type "section" and find Add/Update section numbers
    - tab `shift + ctrl + [` or `]` to change the title
## 2.2. Table formatter
- tag `alt + shift + f`

*sort from [Markdown语法](https://markdown.com.cn)*