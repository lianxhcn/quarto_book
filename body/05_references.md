# 教程和参考资料

## Quarto Book 相关的资源

- [Quarto Book 官方指南](https://quarto.org/docs/books/) | [中文](https://www.aidoczh.com/quarto/docs/books/index.html) | [Options](https://quarto.org/docs/reference/projects/books.html)
- [How to self-publish a technical book on Leanpub and Amazon using Quarto](https://www.brodrigues.co/blog/2023-06-29-book_quarto/)
- 李东风，2023，R 语言教程. [22 Quarto格式文件](https://www.math.pku.edu.cn/teachers/lidf/docs/Rbook/html/_Rbook/quarto.html)
- R for Data Science, 2024. [Chapter 25: Quarto](https://r4ds.hadley.nz/quarto-formats.html). [Github](https://github.com/hadley/r4ds/), [_quarto.yml](https://github.com/hadley/r4ds/blob/main/_quarto.yml)

## 发布
- [Quarto: Publishing to GitHub Pages](https://mickael.canouil.fr/posts/2024-12-30-quarto-github-pages/)
- [How to Create and Publish a Quarto Book on GitHub](https://kalonjilabs.com/posts/how-to-publish-quarto/)
- [Quarto 官网：GitHub Pages](https://quarto.org/docs/publishing/github-pages.html)

Note: 

1. 考虑到国内很多读者无法访问 GitHub Pages，可以使用 [Gitee](https://gitee.com/) 或 [Coding](https://coding.net/) 等国内平台进行发布。
2. 我个人是将编译后的 `docs` 文件夹上传到 GitHub 的 `gh-pages` 分支中，这样可以直接通过 `https://<username>.github.io/<repository>/` 访问。


## 用 Quarto book 写的书

你可以选择自己喜欢的风格，然后将对应的仓库克隆下来，修改 `_quarto.yml` 文件和 `index.qmd` 文件，添加自己的内容。

- [数据分析与 Python 应用](https://github.com/arlionn/ds)
  - 我自己写的第一本 Quarto Book，可以很好地支持中文。
- [https://style.tidyverse.org/](https://github.com/tidyverse/style)
  - 不涉及任何 R 代码的执行问题，可以视为一个 Quarto-book 模板
- [R for Data Science](https://r4ds.hadley.nz/) | [Code](https://github.com/hadley/r4ds/) 
- [Visualization Curriculum](https://jjallaire.github.io/visualization-curriculum) | [Code](https://github.com/jjallaire/visualization-curriculum) 
- Oscar Baruffa, 2024, Big Book for R. [Read](https://www.bigbookofr.com/), [Github](https://github.com/oscarbaruffa/BigBookofR)
  - `    include-after-body: footer.html`
- The Epidemiologist R Handbook, 2024. [Read](https://epirhandbook.com/en/), [Github](https://github.com/appliedepi/epiRhandbook_eng)
  - R 安装和帮助文件等写的非常细致
- Scheuch, C., Voigt, S., & Weiss, P. (2023). Tidy Finance with R (1st ed.). Chapman and Hall/CRC. [-Link-](https://doi.org/10.1201/b23237). [Read](https://www.tidy-finance.org/r/index.html), [github](https://github.com/tidy-finance/r-tidyfinance), [Quarto book](https://github.com/tidy-finance/website/tree/main)
  - [_quarto.yml](https://github.com/tidy-finance/website/blob/main/_quarto.yml)
- Nicholas Tierney.  **Quarto for Scientists** .  **2024** . [book](https://qmd4sci.njtierney.com/), [github](https://github.com/njtierney/qmd4sci), [_quarto.yml](https://github.com/njtierney/qmd4sci/blob/main/_quarto.yml)
- 使用 Quarto Website 的形式写的书
  - to be added
- 更多：[awesome-quarto](https://github.com/mcanouil/awesome-quarto)

## 一些 Github 仓库

这些仓库提供了形式各样的 Quarto Book 模板，你可以根据自己的需要进行修改。

- [coatless-tutorials / quarto-book-template](https://github.com/coatless-tutorials/quarto-book-template)
  - Template repository for creating a book powered by Quarto and Rendered by GitHub Actions onto GitHub Pages. 
  - 介绍了如何使用 github page 发布你的书稿
- [tufte-quarto](https://github.com/fredguth/tufte-quarto) &rarr; [website](https://fredguth.github.io/tufte-quarto/)
  - Tufte book layout for Quarto. 可以将部分图片显示在网页的右侧边栏处。
- [NOAA-quarto-book](https://github.com/nmfs-opensci/NOAA-quarto-book)
  - A Quarto book project with html, pdf and Word output types.



## Quarto for Scientists 中提到的资料

> Source: Nicholas Tierney.  **Quarto for Scientists** .  **2024** . [book](https://qmd4sci.njtierney.com/), [github](https://github.com/njtierney/qmd4sci), [_quarto.yml](https://github.com/njtierney/qmd4sci/blob/main/_quarto.yml)

Here are some resources that I really liked for learning Quarto:

-   [The Quarto "get started" guide](https://quarto.org/docs/get-started/hello/rstudio.html)
-   [The Quarto guide "Quarto manuscripts"](https://quarto.org/docs/manuscripts/)
-   [The Quarto chapter in "R for data science"](https://r4ds.hadley.nz/quarto)
-   [Making shareable documents with Quarto from](https://openscapes.github.io/quarto-website-tutorial/), from OpenScapes
-   [Alison Hill's blog post: "we don't talk about Quarto"](https://www.apreshill.com/blog/2022-04-we-dont-talk-about-quarto/)
-   [Mine Çentinkaya-Rundel's talk "Quarto for academics"](https://quarto.org/docs/blog/posts/2023-05-22-quarto-for-academics/)



