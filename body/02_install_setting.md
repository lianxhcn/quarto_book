# 环境配置

在 VScode 环境下高效编写和发布 Quarto Book，需要提前完成相关软件的安装与基本配置。以下流程适用于大部分 Windows、macOS 和 Linux 用户。



## 必要安装

### 安装 VScode 编辑器

访问 [Visual Studio Code 官网](https://code.visualstudio.com/)，下载安装最新版 VScode。建议安装稳定版，无需安装 Insiders 预览版。

### 安装 Quarto

访问 [Quarto 官网](https://quarto.org/docs/get-started/)，下载并安装适合你操作系统的 Quarto。安装后，建议在命令行（终端/PowerShell）中运行 `quarto --version` 检查是否安装成功。

### 安装 VScode 插件
在 VScode 左侧扩展（Extensions）面板搜索并安装下列插件：

* Quarto（官方插件，支持 `.qmd` 文件的语法高亮与预览）
* Markdown All in One（增强 Markdown 编辑体验）
* Jupyter（如需直接在 VScode 内编辑 `.ipynb` 文件）
* Python、R（分别对应需要用到的语言）
  * 如果你的书稿中不涉及 Python 或 R 代码块，可以不安装对应的插件。
  * 同理，如果书稿中涉及可执行的 Stata 代码块，则需安装 Stata 相关的插件。


## 可选安装

## 安装 R 或 Python 环境

* 如果你的文档包含 R 代码块，需安装 [R](https://cran.r-project.org/)。
* 如果包含 Python 代码块，需配置好 Python 运行环境。建议安装 Anaconda 套装，访问 [Anaconda 官网](https://www.anaconda.com/products/distribution) 下载并安装。Anaconda 包含了 Python 及常用的数据科学库，安装后可通过 Anaconda Navigator 或命令行使用。
  - 国内用户，可以参照 [6  Python：安装和环境配置](https://book.lianxh.cn/ds/body/01_1_install-Python-Anocanda.html) 配置 Python 环境。

### Github 相关

- github 账号（推荐）
  - 如果你计划将 Quarto Book 发布到 GitHub 或其他代码托管平台，建议注册一个 [GitHub](https://www.github.com/) 账号。注册后，你可以创建仓库来存储和管理你的 Quarto Book 项目。
- github desktop（推荐）
  - 如果你不熟悉 Git 命令行操作，可以安装 [GitHub Desktop](https://desktop.github.com/)，它提供了图形化界面，方便进行版本控制和仓库管理。
- 安装 Git（可选）
    熟悉 Git 的用户，建议安装 [Git](https://git-scm.com/) 并在 VScode 中完成初步配置。这样可实现版本管理、远程仓库同步、多人协作等功能。

## 其它问题

### 配置环境变量（如有需要）
确保 quarto、R、python 等命令可在终端/命令行直接调用。对于 Windows 用户，如出现命令无法识别，可在“系统环境变量”中添加相应路径。

### 检查依赖是否正常
在终端分别运行以下命令，确认环境配置成功：

```bash
quarto --version
python --version      # 若需支持 Python
R --version           # 若需支持 R
jupyter --version     # 若需支持 .ipynb
```


完成上述准备工作后，你就可以在 VScode 环境下流畅地新建、编辑和预览 Quarto Book 项目了。

