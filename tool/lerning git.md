# lerning git
Git 是一种可以智能追踪文件中更改的版本控制系统，将文件上传到 GitHub 时，会将其存储在“Git 存储库”中。这意味着，对 GitHub 中的文件进行更改（或“提交”）时，Git 会自动开始跟踪和管理更改。

## 1. Git 的下载
**下载地址：**https://git-scm.com/downloads

## 2. 在 GitHub 上创建账户

### 2.1 创建账户步骤
1. 导航到 https://github.com/
2. 单击”注册“
3. 按照提示创建个人账户

## 3. Git 的 Hello World

### 3.1 创建存储库
首先我们需要创建一个存储库。存储库就好比包含相关项的文件夹，例如文件、图像、视频，甚至其他文件夹。存储库通常会将属于同一”项目“或正在处理的事务的项组合在一起。  

通常，存储库包括一个 README 文件，其中具有项目的相关信息。  

GitHub 可在新建存储库的同时添加 README 文件。GitHub 还提供了其他常用选项，例如许可证文件。  

可在 hello-world 存储库中存储灵感和资源，甚至与他人进行共享和讨论。  

1. 在任何页面的右上角，选择 + ，然后单击”New repository“
2. 在”存储库名称“框中，键入 hello-world
3. 在”说明“框中，键入简短说明
4. 选择存储库是”公共“还是”专用“
5. 选择”添加 README 文件“
6. 单击”创建存储库“

### 第2步：创建分支（branch）
通过分支，可以同时拥有不同版本的存储库。  
默认情况下，存储库有一个名为 main(旧版：master) 的分支，它被视为最终分支。可在存储库中从 main 创建其他分支。要在不更改主要代码源的情况下向项目添加新功能时，分支将非常实用。在合并主分支之前，在不同分支上完成的工作不会显示在主分支上。  

从 main 分支创建分支时，创建的是 main 在当时的副本或快照。如果其他人在你处理分支时对 main 分支进行了更改，可拉取这些更新。  

创建分支：  
* 单击 hello-world 存储库的“代码”选项卡
* 在文件列表上方，单击“main”下拉菜单
* 在文本框中键入分支名称 readme-edits
* 单击“创建分支：Create branch：readme-edits from ‘main’

现在你有两个分支： main 和 readme-edits 。现在，它们看起来完全相同。然后需要向新的 readme-edits 分支添加更改。  

### 第3步：进行和提交更改
在 GitHub 上，保存的更改称为提交。每个提交都有一个关联的提交消息，该消息是解释为什么进行特定更改的说明。提交消息会捕获你更改的历史记录，以便其他参与者可以了解您执行了哪些操作及其原因。  
1. 在你创建的 readme-edits 分支下，单击 README.md 文件。
2. 若要编辑文件，请单击编辑图标。
3. 在编辑器中，编写一些关于自己的内容。
4. 单击“提交更改”。
5. 在“提交更改”框中，编写描述更改的提交消息。
6. 单击“提交更改”。

这些更改将仅适用于 readme-edits 分支上的 README 文件，所以此分支现包含 main 中没有的内容。  

### 第4步：打开一个拉取请求
现在你已在从 main 创建的分支中进行了更改，接下来可打开拉取请求。  

拉取请求是 GitHub 上协作的核心。在这一步中，你将在自己的存储库中打开一个拉取请求，然后自行合并。这是在处理大型项目之前练习 GitHub 流程的好方法。  
1. 单击 hello-world 存储库的“拉取请求”选项卡。
2. 单击“新建拉取请求”。
3. 在“示例比较”框中，选择你创建的分支 readme-edits，与 main 进行比较。
4. 在 Compare （比较）页面上的差异中查看您的更改，确保它们是您要提交的内容。
5. 单击“创建拉取请求”。
6. 为拉取请求指定一个标题，并写下更改的简要说明。
7. 单击“创建拉取请求”。

### 第5步：合并拉取请求
在最后一步中，你将 readme-edits 分支合并到 main 分支中。合并拉取请求后，readme-edits 分支上的更改将合并到 main。  

有时，拉取请求可能会引入与 main 上的现有代码冲突的代码更改。如果存在任何冲突，GitHub 将提醒你有关冲突代码的信息，并防止合并，直到冲突解决为止。  

分支合并到主分支中。
1. 在拉取请求底部，单击“合并拉取请求”以将更改合并到 main 中。
2. 单击“确认合并”。您将收到一条消息，指出请求已成功合并且请求已关闭。
3. 单击“删除分支”。现在你的拉取请求已合并，并且你的更改位于 main 上，接下来你可安全地删除 readme-edits 分支。如果要对项目进行更多更改，可以随时创建新分支并重复此过程。
4. 单击返回 hello-world 存储库的“代码”选项卡，以在 main 上查看已发布的更改。

### 第6步：结束
hello-world 的演示流程到这里就完成了。  

## 常用命令
### 身份标识
在 Git 里使用 user.name 和 user.email 进行配置是很重要的，它们主要用于标识代码提交者的身份信息。  
* 明确提交者，每次在使用 git commit 命令提交代码时，Git 会把 user.name 和 user.email 记录在提交信息中。这有助于团队成员在查看提交历史时，了解每一次代码修改是由谁完成的。
* 关联 GitHub 等平台账号，在使用 Git 与远程仓库进行交互时，配置的 user.email 要和平台上注册的邮箱一致。这样，当你把代码推送到远程仓库后，提交记录就能正确关联到你的平台账号，在平台上显示为你的贡献。

* 配置方法
``` bash
git config user.name "Your Name"
git config user.email "your_email@example.com"
```

### 仓库操作
* `git init` ：在当前目录下初始化一个新的 Git 仓库。
``` bash
git init
```

* `git clone <远程仓库地址>`：将远程仓库克隆到本地。
``` bash
git clone https://github.com/username/repo.git
```

### 提交操作
* `git add <文件路径>`：将指定文件添加到暂存区
``` bash
git add file.txt
git add .  // 使用.可添加当前目录下的所有文件。
```

* `git commit -m "提交信息"`：将暂存区的文件提交到本地仓库，-m后面需添加本次提交的简要描述。
``` bash
git commit -m "添加新功能"
```

* `git status`：查看当前工作区和暂存区的状态，了解哪些文件被修改、添加或删除。
``` bash
git status
```
### 分支操作
* `git branch`：查看本地所有分支，当前所在分支会以特殊颜色显示，且前面有星号。
``` bash
git branch
```

* `git branch <分支名>`：创建一个新的本地分支。
``` bash
git branch feature
```

* `git checkout <分支名>`：切换到指定的本地分支。从 Git 2.23版本开始，也可用 `git switch <分支名>`替代。
``` bash
git checkout feature
git switch feature
```

* `git checkout -b <分支名>`：创建并切换到新的本地分支
``` bash
git checkout -b new-feature
```

* `git merge <分支名>`：将指定分支的修改合并到当前分支
``` bash
git merge feature
```

* `git branch -d <分支名>`：安全删除已经合并到其他分支的本地分支，若要强制删除使用 `git branch -D <分支名>`
``` bash
git branch -d feature
git branch -D old-feature
```

### 远程仓库操作
* `git push <远程仓库名> <分支名>`：将本地分支的修改推送到远程仓库
``` bash
git push origin main
```

* `git push <远程仓库名> <分支名>`：将本地分支的修改推送到远程仓库
``` bash
git push origin main
```

* `git pull <远程仓库名> <分支名>`：从远程仓库拉取指定分支的更新，并合并到本地分支。
``` bash
git pull origin main
```

### 撤销操作
* `git reset <提交哈希值> `：将当前分支的指针移动到指定的提交，可用于撤销提交。
``` bash
git reset HEAD~1  // 撤销上一次提交
```
