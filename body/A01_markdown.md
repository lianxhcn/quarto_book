# Markdown

## 何谓 Markdown？

Markdown 是一种轻量级的标记语言，允许你使用易读易写的纯文本格式编写文档，然后转换成结构化的 HTML, PDF, Word 等多种格式的文档。Markdown 语法简单易学，适合用来撰写笔记、文档、幻灯片等。

大家在网上看到的很多[博客文章](https://www.lianxh.cn/details/1456.html)，程序[说明文档](https://docs.python.org/3/tutorial/index.html)，甚至是在线书籍 ([Python for Data Analysis, 3E](https://wesmckinney.com/book/))，都是用 Markdown 写的。

## 语法速览

![Markdown 语法对照](https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/md-syntax-5mins-codes-preview.png){#fig-md-syntax-quick}

你可以在如下网站按部就班地学习 Markdown 的基本用法，大概五分钟后你就可以掌握常用 Markdown 语法规则了：

> <https://www.markdowntutorial.com/zh-cn>


## Markdown 基本语法

> Source: [markdownguide.org/cheat-sheet/](https://www.markdownguide.org/cheat-sheet/)

这份 Markdown 备忘单介绍了常用的 Markdown 语法。为了便于您快速了解基本的语法规则，这里略去了很多细节信息，详情参见：[基础语法](https://www.markdownguide.org/basic-syntax/) 和 [扩展语法](https://www.markdownguide.org/extended-syntax/)。

以下是 [John Gruber](https://en.wikipedia.org/wiki/John_Gruber) 原始设计文档中列出的基本元素，所有 Markdown 应用程序都支持这些元素。

| 元素            | Markdown 语法                                                  |
| :-------------- | :------------------------------------------------------------- |
| 标题            | `# 一级标题`<br>`## 二级标题`<br>`### 三级标题`                |
| 粗体            | `**粗体文本**`                                                 |
| 斜体            | `*斜体文本*`                                                   |
| 引用块          | `> 引用内容`                                                   |
| 有序列表        | `1. 第一项`<br>`2. 第二项`<br>`3. 第三项`                      |
| 无序列表        | `- 第一项`<br>&emsp; `  -  第一条`<br>`- 第二项`<br>`- 第三项` |
| 代码高亮显示            | \`代码\` (\`xtreg\` &rarr; `xtreg`)                                                       |
| 水平线          | `---`                                                          |
| 链接            | `[连享会主页](https://www.lianxh.cn)`                          |
| 图片            | `![图片标题](/Fig/image.jpg)` 或 `![](图片网址)`                 |

### 表格

```md
| 命令    | 范例                 |
| :------ | :------------------- |
| xtreg   | `xtreg y x, fe`      |
| reghdfe | `reghdfe y x, a(id)` |
```

| 命令    | 范例                 |
| :------ | :------------------- |
| xtreg   | `xtreg y x, fe`      |
| reghdfe | `reghdfe y x, a(id)` |


### 数学公式

- 单行数学公式用 `$$` 符号包围起来；
- 行内数学公式用 `$` 符号包围起来；
- 包围符号内侧不要有空格，否则在有些 Markdown 编辑器中无法正常显示公式
  - 正确：`$y = f(x)$`
  - 错误：`$ y = f(x) $` 或 `$y = f(x) $`
- 有关 LaTeX 数学公式的语法和工具，参见：
  - [Markdown常用LaTex数学公式](https://www.lianxh.cn/details/243.html)
  - [神器-数学公式识别工具-mathpix](https://www.lianxh.cn/details/284.html)

```markdown
模型设定为：

$$y_{it} = \alpha_i + x_{it}\beta + u_{it}$$

其中，$y_{it}$ 为被解释变量，$\alpha_i$ 为个体效应。
```

模型设定为：

$$y_{it} = \alpha_i + x_{it}\beta + u_{it}$$

其中，$y_{it}$ 为被解释变量，$\alpha_i$ 为个体效应。

### 代码块

````markdown
```python
import pandas as pd

df = pd.DataFrame({
    'A': [1, 2, 3],
    'B': [4, 5, 6]
})
```

```stata
sysuse "auto.dta", clear
regress mpg weight
display "Results: " 2 + 3
```
````

渲染效果：

```python
import pandas as pd

df = pd.DataFrame({
    'A': [1, 2, 3],
    'B': [4, 5, 6]
})
```

```stata
sysuse "auto.dta", clear
regress mpg weight
display "Results: " 2 + 3
```

### 扩展阅读

  - 初虹, 2024, [让「记录」变得简单：Markdown使用详解](https://www.lianxh.cn/details/1456.html), 连享会 No.1456.
  - 初虹, 2021, [学术论文写作新武器：Markdown-上篇](https://www.lianxh.cn/details/603.html), 连享会 No.603.
  - 初虹, 2021, [学术论文写作新武器：Markdown-下篇](https://www.lianxh.cn/details/604.html), 连享会 No.604.
  - 初虹, 2021, [学术论文写作新武器：Markdown-中篇](https://www.lianxh.cn/details/605.html), 连享会 No.605.
  - 连玉君, 2024, [VScode插件：安装、配置和使用](https://www.lianxh.cn/details/1490.html), 连享会 No.1490.
  - 连玉君, 2024, [VScode：实用 Markdown 插件推荐](https://www.lianxh.cn/details/1390.html), 连享会 No.1390.


## marp 幻灯片

在 VScode 中安装 `Marp` 插件后，你可以使用 Markdown 语法来创建幻灯片。使用 Marp 最大的好处是你可以专注于内容，而不必担心幻灯片的格式和样式。Marp 会自动将你的 Markdown 文档转换为美观的幻灯片。

![](https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/20220525154453.png)

### 模版 1：最基本的设定

以下是一个简单的 Marp 幻灯片模板，你只需要新建一个 `.md` 文件，输入如下内容，然后在 VScode 中打开该文件即可：

```markdown
---
marp: true
---

# 幻灯片标题

---

## 第一页幻灯片

- xxx
- xxx

---

## 第二页幻灯片

- xxx
- xxx
```


### 模版 2：更多的设定

该模板的主要功能包括：

- 幻灯片的标题、作者、页码、脚注
- 幻灯片的字号
- 标题的颜色和页面背景颜色

```markdown
---
marp: true
size: 16:9      # 宽版：4:3
paginate: true  # 显示页码
footer: '脚注文本或 [xxx](URL)'
---

<style>
/*一级标题局中*/
section.lead h1 {
  text-align: center; /*其他参数：left, right*/
}
section {
  font-size: 22px;      /* 正文字号 */
}
h1 {
  color: blackyellow;   /* 标题的颜色 */
  /*font-size: 28px; */ /* 标题的字号, 其它标题也可以这样修改 */
}
h2 {
  color: green;
}
h3 {
  color: darkblue;
}

/* 右下角添加页码 */
section::after {
  content: attr(data-marpit-pagination) '/' attr(data-marpit-pagination-total); 
}
header,
footer {
  position: absolute;
  left: 50px;
  right: 50px;
  height: 25px;
}
</style>

<!--顶部文字-->
[lianxh.cn](https://www.lianxh.cn/news/46917f1076104.html) 

<br>

<!--封面图片-->
![bg right:50% w:400 brightness:. sepia:50%](https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/20220722114227.png) 

<!--幻灯片标题-->
# Marp 参数设置

<br>
<br>

<!--作者信息-->
[连玉君](https://www.lianxh.cn) (中山大学)
arlionn@163.com

<br>
---
<!-- backgroundColor: #FFFFF9 -->
## 第一页幻灯片

- 背景是淡黄色的，可以根据需要修改颜色

---
<!-- backgroundColor:white -->
## 第二页幻灯片

- 背景是纯白色
- 下面的图片在右侧，占页面 60% 的宽度

![bg right:60% w:800](图片网址)

```

详情参见：

  - 宋森安, 2021, [用Markdown制作幻灯片-五分钟学会Marp（上篇）](https://www.lianxh.cn/details/656.html), 连享会 No.656.
  - 宋森安, 2021, [用Markdown制作幻灯片-五分钟学会Marp（下篇）](https://www.lianxh.cn/details/657.html), 连享会 No.657.
  - 连玉君, 2022, [Marp幻灯片模板：用Markdown快速写幻灯片](https://www.lianxh.cn/details/1059.html), 连享会 No.1059.


