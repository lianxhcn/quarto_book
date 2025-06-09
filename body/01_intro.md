# 创建流程

Quarto book 是一个基于 [quarto](https://quarto.org/docs/books/) 的书籍项目：你可以将多个章节文档通过一个名为 `_quarto.yml` 的文件组织成一本书，然后将其编译为一本电子书 (HTML 或 PDF 格式均可)，进而通过 GitHub Pages 发布。

以本项目为例：

- 本地文件夹：`D:\Github_lianxh\quarto_book`
- Github 仓库：<https://github.com/lianxhcn/quarto_book>
- 最终发布的主页：<https://lianxhcn.github.io/quarto_book/>

创建一本 Quarto Book 非常简单。你可以使用 VScode 或 RStudio 来创建和编辑你的书籍项目。这里以 VScode 为例进行说明。

你可以通过两种方式来创建 Quarto Book：

1. 使用现有的模板项目；
2. 从头开始创建一个新的 Quarto Book 项目。

对于初学者而言，建议采用第一种方式。你只需要将现有的模板项目克隆或下载到本地，然后简单修改相关配置和内容即可。

## 使用模板创建书稿 (推荐)

在执行如下步骤之前，请先确保你已经完成了 [环境配置](02_install_setting.md) 的相关工作。

1. **Clone 模板**：
   - 将 [quarto_book](https://www.github.com/lianxhcn/quarto_book) 仓库克隆或下载到本地。
2. **测试环境配置**：
   - 在 VScode 中打开项目根目录，进而打开 `_quarto.yml` 文件。
   - 按快捷键 `Ctrl+~` 打开 Terminal >> 输入 `quarto render` 即可开始编译。完成后项目根目录下会自动生成 `/docs` 子文件夹，其中包含编译后的 HTML 文件。
   - 通过我的电脑地址栏打开 `/docs` 文件夹，双击 `index.html` 文件即可在浏览器中预览书籍。
   以上步骤若能成功完成，说明你的 Quarto 环境配置正常。
3. **修改书籍基本信息**：
   - 在 VScode 中打开项目根目录下的 `_quarto.yml` 文件，修改书籍的标题、作者等信息。
   - 打开 `index.qmd` 文件，编辑书籍简介。

4. **撰写你的书稿**：
   - 各章书稿存放于 `body/` 目录下。你可以在该目录下创建新的 `.md`, `.qmd` 或 `.ipynb` 文件，或编辑现有的章节文件。
   - 完成后，请参照第 3 步，更新 `_quarto.yml` 文件中的章节列表。
5. **编译和预览书籍**：
   - 在 VScode 中按 `Ctrl+~` 打开 Terminal >> 输入 `quarto render` 即可重新编译书籍。
   - 预览方式同上，双击 `/docs/index.html` 文件即可在浏览器中查看最新编译结果。
     - Note: 如果浏览器无法显示最新内容，请尝试清理浏览器缓存或使用无痕模式打开。

   <img style="width: 450px" src="https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/20250609180318.png">
6. **发布书籍**：参见 [使用 GitHub Pages 发布](04_github_page.md)。




## 从头开始创建书稿

虽然不建议初学者从头开始创建 Quarto Book 项目，但如果你希望完全自定义书籍结构和内容，可以按照以下步骤操作：

- 在 VScode 中按 `Ctrl+Shift+P`，输入 `Quarto: Create Project` 来创建一个新的 Quarto Book 项目。
- 在弹出的对话框中选择 **Book** 模板。
- 输入项目名称和保存路径。
- 打开生成的 `_quarto.yml` 文件，修改书籍的标题、作者等信息。
- 编辑 `index.qmd` 文件，添加书籍的内容。
- 编译和预览方式与「使用模板创建书稿」相同。



## Quarto Book 项目结构

Quarto book 本质上是将多个文档组织在一起，使它们能够作为一本书来编译和预览：

- 支持多种文档格式，且可以同时使用多种格式的文档。包括：`.qmd`，`.md`，`.Rmd` 和 `.ipynb` 等。
- 配置文件：Quarto Book 项目会通过 `_quarto.yml` 文件来定义书籍的元数据和结构。
- `index.qmd` 文件：这是书籍的入口文件，通常包含书籍的封面和介绍等内容。编译时会将其作为书籍或网站的首页。

一个典型的 Quarto Book 项目结构如下：

```md
quarto_book/
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
quarto_book/
├── _quarto.yml         # 配置文件，定义书籍的元数据和结构
├── index.qmd           # 书籍的入口文件
├── chapters/           # 存放章节文件
│   ├── chapter1.qmd    # 第一章内容   
│   ├── chapter2.qmd    # 第二章内容
│   ├── chapter3.qmd    # 第三章内容
├── images/             # 存放书籍中使用的图片
├── data/               # 存放书籍中使用的数据文件
└── references.bib      # 参考文献文件（可选）
``` 

同理，你也可以为每个章节创建一个独立的目录，例如 `chapter1/`，`chapter2/` 等，进而在 `chapter1/` 目录下创建 `data/`, `images/` 等子目录来组织相关资源。这样可以使项目结构更加清晰。



## 参考资料

- quarto book: [官方指南](https://quarto.org/docs/books/)

- [Quarto 发布基础](https://www.aidoczh.com/quarto/docs/publishing/index.html)
- [github pages](https://www.aidoczh.com/quarto/docs/publishing/github-pages.html)
