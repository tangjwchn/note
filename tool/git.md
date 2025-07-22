# Git
Git 是一个分布式版本控制系统（DVCS），由 Linus Torvalds（Linux 之父）在 2005 年用两周时间写成，专门用来追踪文件的每一次变化，尤其是代码。它的核心目标是：让多人协作时，既能高效管理版本，又能避免代码冲突。

## 1. Git 的说明
**下载地址：**https://git-scm.com/downloads

**核心概念：**

| Git 术语             | 比喻解释                                           |
| ------------------ | ---------------------------------------------- |
| **仓库（Repository）** | 项目的“历史档案馆”，存着所有版本的代码。                          |
| **提交（Commit）**     | 每次“存档”一个快照，记录“谁、何时、改了什么”。                      |
| **分支（Branch）**     | 平行宇宙：主分支（master/main）是主线，其他分支（如“dev”）可独立开发新功能。 |
| **合并（Merge）**      | 把不同宇宙的修改融合到主线。                                 |
| **远程仓库（Remote）**   | 云端的“备份档案馆”（如 GitHub/GitLab）。                   |

**为什么用git：**

1. 分布式：每人电脑上有完整仓库，即使断网也能工作。
2. 高效分支：创建/合并分支极快（秒级），比传统工具（如 SVN）快 100 倍。
3. 数据完整性：用 SHA-1 哈希保证代码永不丢失或损坏。

## 2. 常用命令

### 2.1 身份标识
在 Git 里使用 user.name 和 user.email 进行配置是很重要的，它们主要用于标识代码提交者的身份信息。  
* 明确提交者，每次在使用 git commit 命令提交代码时，Git 会把 user.name 和 user.email 记录在提交信息中。这有助于团队成员在查看提交历史时，了解每一次代码修改是由谁完成的。
* 关联 GitHub 等平台账号，在使用 Git 与远程仓库进行交互时，配置的 user.email 要和平台上注册的邮箱一致。这样，当你把代码推送到远程仓库后，提交记录就能正确关联到你的平台账号，在平台上显示为你的贡献。

* 配置方法
``` bash
git config user.name "Your Name"
git config user.email "your_email@example.com"
```

### 2.2 仓库操作
* `git init` ：在当前目录下初始化一个新的 Git 仓库。
``` bash
git init
```

* `git clone <远程仓库地址>`：将远程仓库克隆到本地。
``` bash
git clone https://github.com/username/repo.git
```

### 2.3 提交操作
* `git add <文件路径>`：将指定文件添加到暂存区
``` bash
git add file.txt
git add .    # 使用.可添加当前目录下的所有文件。
```

* `git commit -m "提交信息"`：将暂存区的文件提交到本地仓库，-m后面需添加本次提交的简要描述。
``` bash
git commit -m "添加新功能"    # 提交一个版本快照
```

* `git status`：查看当前工作区和暂存区的状态，了解哪些文件被修改、添加或删除。
``` bash
git status
```
### 2.4 分支操作
* `git branch`：查看本地所有分支，当前所在分支会以特殊颜色显示，且前面有星号。
``` bash
git branch
```

* `git branch <分支名>`：创建一个新的本地分支。
``` bash
git branch feature-x    # 创建新分支“feature-x”
```

* `git checkout <分支名>`：切换到指定的本地分支。从 Git 2.23版本开始，也可用 `git switch <分支名>`替代。
``` bash
git checkout feature-x    # 切换到该分支
git switch feature-x    # 切换到该分支
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

### 2.5 远程仓库操作
* `git push <远程仓库名> <分支名>`：将本地分支的修改推送到远程仓库
``` bash
git push origin main    # 把本地提交推到 GitHub 的 main 分支
```

* `git pull <远程仓库名> <分支名>`：从远程仓库拉取指定分支的更新，并合并到本地分支。
``` bash
git pull origin main    # 拉取远程 main 分支的最新代码
```

### 2.6 撤销操作
* `git reset <提交哈希值> `：将当前分支的指针移动到指定的提交，可用于撤销提交。
``` bash
git reset HEAD~1  // 撤销上一次提交
```
