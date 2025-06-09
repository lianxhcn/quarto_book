# 使用 GitHub Pages 发布

本章以我的仓库 <https://github.com/lianxhcn/quarto_book> 为例，介绍如何使用 **GitHub Desktop** 创建 `gh-pages` 分支并完成 Quarto Book 的在线部署。

完成后，你可以通过访问 <https://lianxhcn.github.io/quarto_book/> 来查看部署效果。其他人可以通过该链接访问你的 Quarto Book。

## 发布流程

我们的目的是使用 `docs` 文件夹作为静态网页根目录，发布到 `lianxhcn.github.io/quarto_book`，推荐采用**项目级 Pages**方式，具体如下：

### 步骤一：确保 docs 文件夹在主分支

* 你已经把所有网页内容渲染到 `docs`，这是 GitHub Pages 推荐的目录名。

### 步骤二：推送本地代码到 GitHub

1. 在 **GitHub Desktop** 中确认你的更改（见第二问）。
2. 确保主分支（main/master）与 GitHub 仓库同步。

### 步骤三：在 GitHub 仓库中启用 Pages

1. 打开你的项目仓库页面：
   [https://github.com/lianxhcn/quarto\_book](https://github.com/lianxhcn/quarto_book)
2. 点击右上角的 **Settings** → 左侧栏选择 **Pages** 或 **Pages（Beta）**
3. 在 “Build and deployment” 下，**Source** 选择 “Deploy from a branch”
4. 选择：

   * Branch：`main`（或你当前的主分支）
   * Folder：`/docs`
5. 保存设置。

### 步骤四：访问网页

* 等待几分钟，GitHub 会自动生成页面。
* 访问：
  [https://lianxhcn.github.io/quarto\_book/](https://lianxhcn.github.io/quarto_book/)

### 注意事项

* 如果页面内容没更新，请确保每次用 `quarto render` 后及时将最新的 `docs` 文件夹**推送**到 GitHub。
* 你可以通过更改 `_quarto.yml` 或其他源码，然后再次 render → push → 自动更新网页。



## GitHub Desktop 实现 Pull 和 Push

以你的本地 `D:\Github_lianxh\quarto_book` 项目为例：

### 初始设置（仅首次需要）

1. 打开 GitHub Desktop，File → Add local repository，选择你的本地文件夹。
2. 仓库面板左上角应看到 `quarto_book` 项目名，远程仓库自动连接到 `https://github.com/lianxhcn/quarto_book`。

### 日常操作

**Pull（拉取最新远程内容到本地）**

1. 点击 GitHub Desktop 左上角的 “Current Branch”（确保在 main/master 分支）。
2. 点击右上角的 “Fetch origin”（如果有更新则会变成 “Pull origin”），点击它即可同步远程变更到本地。

**Push（推送本地更新到远程）**

1. 正常编辑、修改、增加或删除文件。
2. 在 GitHub Desktop 主界面下方看到 “Changes” 列表，输入 Commit message（如 `render new chapters`），点击 “Commit to main”。
3. 提交后，界面会出现 “Push origin” 按钮，点击即可推送本地更改到 GitHub 仓库。

### 补充说明

* **新文件/文件夹**：只要在本地新建（如新增章节），在 GitHub Desktop 中会自动识别到“Changes”，按上述流程提交。
* **删除或重命名**：同理，所有文件操作 GitHub Desktop 都会追踪。
* **冲突**：如遇 pull/push 冲突，按 GitHub Desktop 提示合并冲突后再 push。

### 常见问题

* **docs 里无变化？**
  确认用 `quarto render` 重新编译，且本地 docs 文件夹变动已被 Git 跟踪和推送。
* **访问慢？**
  GitHub Pages 有时需几分钟才能看到更新。
* **访问路径？**
  若你以后需要发布为 `lianxhcn.github.io` 的主站，则结构和设置略有不同，目前发布到 `lianxhcn.github.io/quarto_book` 是标准做法。

## 参考文档

* [GitHub Pages 官方指南](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages)
* [Quarto 官方关于发布到 GitHub Pages](https://quarto.org/docs/publishing/github-pages.html)


