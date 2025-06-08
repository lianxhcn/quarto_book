# 网页发布

本章以我的仓库 <https://github.com/lianxhcn/quarto_book> 为例，介绍如何使用 **GitHub Desktop** 创建 `gh-pages` 分支并完成 Quarto Book 的在线部署。

完成后，你可以通过访问 <https://lianxhcn.github.io/quarto_book/> 来查看部署效果。其他人可以通过该链接访问你的 Quarto Book。


## 步骤 1：克隆仓库到本地
1. 打开 **GitHub Desktop**，点击左上角 **File** > **Clone Repository**。  
2. 在 **URL** 栏输入你的仓库地址：  
   ```
   https://github.com/lianxhcn/quarto_book.git
   ```  
3. 选择本地保存路径（例如 `D:\Github_lianxh\quarto_book`），点击 **Clone**。  
   - 此时本地会生成一个与远程仓库同步的文件夹，默认分支为 `main`（或 `master`，取决于仓库初始设置）。


## 步骤 2：创建 `gh-pages` 分支
1. 在 GitHub Desktop 右上角，点击当前分支名称（默认是 `main`）。  
2. 在弹出的分支切换菜单中，点击 **New branch**。  
3. 输入分支名称：`gh-pages`，点击 **Create branch**。  
   - 此时你已切换到本地的 `gh-pages` 分支。


## 步骤 3：准备 Quarto 输出文件
1. 将 Quarto 编译生成的 `docs` 文件夹内的**所有内容**（如 `index.html`、静态资源等）复制到本地仓库的**根目录**。  
   - **注意**：确保根目录下的文件是 Quarto 站点的完整内容（即 `docs` 文件夹内的文件直接放在仓库根目录，而不是保留 `docs` 文件夹本身）。  
   - 例如：若 `docs` 文件夹内有 `index.html`，复制后仓库根目录应直接包含 `index.html`。


## 步骤 4：提交文件到本地分支
1. 在 GitHub Desktop 左侧的 **Changes** 选项卡中，会显示新增/修改的文件。  
2. 在 **Summary** 栏输入提交信息（如 “Add Quarto book files for gh-pages”）。  
3. 点击 **Commit to gh-pages** 完成本地提交。


## 步骤 5：推送 `gh-pages` 分支到远程仓库
1. 点击右上角的 **Push origin** 按钮（通常在分支名称右侧）。  
2. 确认推送操作，等待进度条完成。  
   - 此时远程仓库（`https://github.com/lianxhcn/quarto_book`）会新增 `gh-pages` 分支，并包含你的 Quarto 站点文件。


## 步骤 6：验证 GitHub Pages 部署
1. 登录 GitHub，进入你的仓库：[https://github.com/lianxhcn/quarto_book](https://github.com/lianxhcn/quarto_book)。  
2. 点击顶部菜单的 **Settings** > **Pages**（左侧栏）。  
3. 在 **Source** 部分，选择 **Branch: gh-pages**，并点击 **Save**。  
   - 稍等片刻（通常几分钟内），GitHub 会自动部署页面。  
4. 部署完成后，页面顶部会显示访问链接：  
   ```
   https://lianxhcn.github.io/quarto_book/
   ```  
   - 点击链接即可访问你的 Quarto Book。


## 常见问题与注意事项
1. **文件结构问题**：  
   - 若保留 `docs` 文件夹（即仓库根目录下有 `docs/index.html`），访问路径需改为：  
     ```
     https://lianxhcn.github.io/quarto_book/docs/
     ```  
     这可能不符合预期，建议直接将内容放在根目录。  

2. **分支名称**：  
   - GitHub Pages 默认识别 `gh-pages` 或 `main` 分支（需在设置中手动选择），确保分支名称正确。  

3. **更新内容**：  
   - 后续修改内容后，只需在本地 `gh-pages` 分支更新文件，重新提交并推送即可。  

4. **强制推送（可选）**：  
   - 若远程分支已有冲突，可尝试强制推送：  
     ```bash
     # 在 Git 终端执行（需先切换到本地 gh-pages 分支）
     git push origin gh-pages --force
     ```


通过以上步骤，你可以通过 GitHub Desktop 轻松创建并部署 `gh-pages` 分支，实现 Quarto Book 的在线访问。