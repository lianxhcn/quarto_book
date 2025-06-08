# Quarto book

quarto book 是一个基于 [quarto](https://quarto.org/docs/books/) 的书籍项目：你可以将多个章节文档通过一个名为 `_quarto.yml` 的文件组织成一本书，然后将其编译为一本电子书 (HTML 或 PDF 格式均可)，进而通过 GitHub Pages 发布。

以本项目为例：

- 本地文件夹：`D:\Github_lianxh\quarto_book`
- Github 仓库：<https://github.com/lianxhcn/quarto_book>
- 最终发布的主页：<https://lianxhcn.github.io/quarto_book/>

创建一本 Quarto Book 非常简单。你可以使用 VScode 或 RStudio 来创建和编辑你的书籍项目。以下是一些基本的步骤和资源，帮助你快速上手。

## 创建 Quarto Book 的方式

你可以通过两种方式来创建 Quarto Book：

1. 使用现有的模板项目；
2. 从头开始创建一个新的 Quarto Book 项目。


### 方式 1：使用模板

- 将 [quarto_book_template](https://gitee.com/arlionn/quarto_book_template) 仓库克隆或下载到本地。
- 在 VScode 中打开该项目根目录下的 `quarto.yml` 文件，修改书籍的标题、作者等信息。
- 打开 `index.qmd` 文件，编辑书籍的内容。
- 在 VScode 中按 `Ctrl+Shift+P`，输入 `Quarto: Render Book` 来编译书籍。
  - 命令行方式：按快捷键 `Ctrl+~` 打开 Terminal >> 输入 `quarto render` 即可
- 预览书籍：
  - 方式 1：点击右上角的 **Preview** 按钮；
  - 方式 2：按快捷键 `Ctrl+~` 打开 Terminal >> 输入 `quarto preview`；
  - 方式 3：(推荐) 在输出目录中双击 `index.html` 文件（需要清理浏览器缓存以查看最新内容）。

### 方式 2：从头开始创建
- 在 VScode 中按 `Ctrl+Shift+P`，输入 `Quarto: Create Project` 来创建一个新的 Quarto Book 项目。
- 在弹出的对话框中选择 **Book** 模板。
- 输入项目名称和保存路径。
- 打开生成的 `quarto.yml` 文件，修改书籍的标题、作者等信息。
- 编辑 `index.qmd` 文件，添加书籍的内容。
- 编译和预览方式与「方式 1」相同。



## Quarto Book 项目结构

Quarto book 本质上是将多个文档组织在一起，使它们能够作为一本书来编译和预览：

- 支持多种文档格式，且可以同时使用多种格式的文档。包括：`.qmd`，`.md`，`.Rmd` 和 `.ipynb` 等。
- 配置文件：Quarto Book 项目会通过 `_quarto.yml` 文件来定义书籍的元数据和结构。
- `index.qmd` 文件：这是书籍的入口文件，通常包含书籍的封面和介绍等内容。编译时会将其作为书籍或网站的首页。

一个典型的 Quarto Book 项目结构如下：

```md
quarto_book_template/
├── _quarto.yml          # 配置文件，定义书籍的元数据和结构
├── index.qmd           # 书籍的入口文件
├── chapter1.qmd        # 第一章内容
├── chapter2.qmd        # 第二章内容
├── chapter3.qmd        # 第三章内容
├── images/             # 存放书籍中使用的图片
├── data/               # 存放书籍中使用的数据文件
└── references.bib      # 参考文献文件（可选）
```

如果章节较多，或希望每个章节有独立的目录，可以将章节文件放在 `chapters/` 目录下，结构如下：

```md   
quarto_book_template/
├── _quarto.yml          # 配置文件，定义书籍的元数据和结构
├── index.qmd           # 书籍的入口文件
├── chapters/           # 存放章节文件
│   ├── chapter1.qmd     # 第一章内容   
│   ├── chapter2.qmd     # 第二章内容
│   ├── chapter3.qmd     # 第三章内容
├── images/             # 存放书籍中使用的图片
├── data/               # 存放书籍中使用的数据文件
└── references.bib      # 参考文献文件（可选）
``` 

同理，你也可以为每个章节创建一个独立的目录，例如 `chapter1/`，`chapter2/` 等，进而在 `chapter1/` 目录下创建 `data/`, `images/` 等子目录来组织相关资源。这样可以使项目结构更加清晰。



## book
- quarto book: [官方指南](https://quarto.org/docs/books/)

  - 在 VScode 中：
    - **Ctrl+P** &rarr; `>quarto creat project` 
    - 改写相应的页面
    - 编译：`Ctrl+~` 打开 Terminal >> 输入 `quarto render` 即可
    - 预览：
      - 方法 1：到输出 book 的文件夹中，双击 index.html 即可在本地浏览全书 (需要及时清理浏览器缓存才能看到更新后的网页)
      - 方法 2：点击右上角 **Preview** (`Ctrl+Shift+K`)
  - RStudio 中我还没有尝试，应该更简单

## 通过 github 发布
- [Quarto 发布基础](https://www.aidoczh.com/quarto/docs/publishing/index.html)
- [github pages](https://www.aidoczh.com/quarto/docs/publishing/github-pages.html)
