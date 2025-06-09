

# _quarto.yml 文件


## 简介
`_quarto.yml` 文件是 Quarto Book 项目的配置文件，用于定义书籍的元数据、结构和输出格式。以下是一个简单的 `_quarto.yml` 文件示例：

```yaml
project:
  type: book
  output-dir: docs  # 输出目录，可以自定义

book:
  title: "你的书名"
  author: "作者姓名"
  date: today
  date-format: iso
  chapters:
    - index.qmd
    - chapters/chapter1.qmd
    - chapters/chapter2.qmd
    - chapters/chapter3.qmd

# 输出格式设置，可按需调整
format:
  html:
    toc: true
    toc-depth: 3
    number-sections: true
    theme: cosmo
    code-fold: true
    code-summary: "显示代码"
    df-print: paged
    highlight-style: github
  pdf:
    documentclass: book
    toc: true
    toc-depth: 3
    number-sections: true
```

你还可以在 `_quarto.yml` 文件中添加更多配置选项，如自定义样式、引用管理、输出格式等。具体的配置选项可以参考 [Quarto Book 官方指南](https://quarto.org/docs/books/)。

## 实例

你也可以查看如下示例的 `_quarto.yml` 文件，从中截取你需要的部分：

- Hadley Wickham, R for Data Science, 2024. [Chapter 25: Quarto](https://r4ds.hadley.nz/quarto-formats.html). [Github](https://github.com/hadley/r4ds/).
  - [_quarto.yml](https://github.com/hadley/r4ds/blob/main/_quarto.yml)
- Nicholas Tierney.  **Quarto for Scientists** .  **2024** . [book](https://qmd4sci.njtierney.com/), [github](https://github.com/njtierney/qmd4sci)
  - [_quarto.yml](https://github.com/njtierney/qmd4sci/blob/main/_quarto.yml)
- 连玉君, 2025, [数据分析与 Python 应用](https://github.com/arlionn/ds). 
  - [_quarto.yml](https://github.com/arlionn/ds/blob/main/_quarto.yml)

## 更多配置选项

如果你想对 `_quarto.yml` 文件进行更深入的了解和配置，可以参考以下资源：

- [Quarto Book 官方指南](https://quarto.org/docs/books/)
- [Quarto Book Options](https://quarto.org/docs/reference/projects/books.html)
- [Quarto Book Configuration](https://quarto.org/docs/reference/projects/configuration.html)
- [Quarto Book YAML Reference](https://quarto.org/docs/reference/projects/yaml.html)

你也可以使用如下提示词，借助 ChatGPT, DeepSeek, 豆包等 AI 工具来学习和配置 `_quarto.yml` 文件：

::: {.callout-tip}
### 提示词

- 分享一个完整的 quarto book 中的 _quarto.yml 配置讲义
- 解释 _quarto.yml 文件中的每个配置项的作用
- 如何在 _quarto.yml 文件中配置书籍网站主页的页脚
- 如何设置代码块的语法高亮和折叠功能
- 如何在 _quarto.yml 文件中添加自定义样式和主题

::: 