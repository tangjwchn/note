# GitHub
GitHub 是一个基于 Git 的代码托管与协作平台，2008 年上线，2018 年被微软收购。它不仅是程序员的“云盘”，更是全球最大的开源社区和开发者社交网络。


## 1. GitHub 的说明

**GitHub = Git 的“社交平台” + 代码仓库 + 协作工具 + 开源生态**，程序员用它来托管代码、协作开发、参与开源，甚至找工作（招聘者会看 GitHub 贡献）。

**核心功能：**

| 功能               | 说明                                              |
| ----------------- | -----------------------------------------------  |
| **代码托管**       | 用 Git 管理代码版本，支持公有/私有仓库。               |
| **协作开发**       | Pull Request（合并请求）、Issue（任务讨论）、Code Review（代码审查）。 |
| **开源社区**       | 数百万开源项目（如 Linux、React、TensorFlow）在此共享。|
| **GitHub Actions** | 内置 CI/CD 工具，自动化测试、部署。                  |
| **Pages**          | 免费搭建个人/项目网站（如 `username.github.io`）。   |

**实际应用场景：**

1. 个人开发者
* 备份代码到云端，记录每次修改历史。
* 用 GitHub Pages 搭建博客或项目官网。
2. 团队协作
* 多人开发时，通过分支（Branch）和 Pull Request 避免代码冲突。
3. 开源贡献
* 向知名项目提交改进（如修复 Python 的某个库）。
* 流程：Fork 项目 → 改代码 → 发起 Pull Request → 原作者审核合并。

## 2. 在 GitHub 上创建账户

### 2.1 创建账户步骤
1. 导航到 https://github.com/
2. 单击”sign up“
3. 按照提示创建个人账户

## 3. GitHub 的 Hello World

### 3.1 创建存储库（repositories）
存储库就好比包含相关项的文件夹，例如文件、图像、视频，甚至其他文件夹。存储库通常会将属于同一”项目“或正在处理的事务的项组合在一起。通常，存储库包括一个 README 文件，其中具有项目的相关信息。  

1. 在任何页面的右上角，选择 + ，然后单击”New repository“
2. Repository name：输入项目存储库名
3. Description：键入简短描述
4. 选择存储库是 ”Public“ 还是 ”Private“
5. 勾选 ”Add a README file“
6. Add .gitignore：忽略文件，指示 Git 在提交时要忽略哪些文件和目录。
7. Choose a license：选择许可证，默认None（默认的无许可证，保留所有权利。他人无权复制、修改或分发代码，仅可以查看和Fork。）
8. 单击 ”Create repository“

### 3.2 创建分支（branch）
默认情况下，存储库有一个名为 main(旧版：master) 的分支，它被视为主分支，可从 main 创建其他分支，要在不更改主要代码源的情况下向项目添加新功能时，分支将非常实用。

从 main 分支创建分支时，创建的是 main 在当时的快照。如果其他人在你处理分支时对 main 分支进行了更改，可拉取这些更新。

1. 单击 Repositories, 进入 hello-world 存储库界面
2. 在文件列表上方，单击 “Branch” 菜单
3. 单击 “New branch”，填入 “New branch name” 分支名 readme-edits，”Source“ 选择 main 主分支

现在你有两个分支： main 和 readme-edits 。现在，它们看起来完全相同。然后需要向新的 readme-edits 分支添加更改。

### 3.3 提交更改
在 GitHub 上保存的更改称为提交，每个提交都有一个关联的提交消息，该消息是解释为什么进行特定更改的说明。  
1. 切换至 readme-edits 分支下，单击 README.md 文件
2. 单击编辑图标
3. 在编辑器中，编写一些关于自己的内容
4. 单击 “Commit changes”
5. 在 “Commit changes” 框中，编写一段 ”Commit message“
6. 单击 “Commit changes”

这些更改将仅适用于 readme-edits 分支上的 README 文件，所以此分支现包含 main 中没有的内容。  

### 3.4 使用 Pull Request（PR）流程，将分支合并至主分支
团队协作用 **Pull Request** 更安全规范，禁止直推。

1. 打开 GitHub → 进入仓库 → 点击 **“Compare & pull request”**
2. 选择 `feature` → `main`
3. 填写标题和描述 → 提交 PR
4. “Merge pull request”

### 3.5 删除分支
远端分支可在页面上进行删除操作，本地分支可通过 git branch -d XXX 进行删除。

### 3.6 结束
hello-world 的演示流程到这里就完成了。  