# git的相关操作
## 基础
+ `git help <command>` 获取git命令的帮助信息
+ `git init` 创建一个新的git仓库，其数据会被存放在一个名为'.git的目录下'
+ `git status` 显示当前的仓库状态
+ `git add <filename>` 添加文件到暂存区
  + `git add .` 把当前路径下的所有文件都添加到暂存你去（递归的），但是不包括'.gitignore'文件中声明的不被包含的文件
+ `git commit` 创建一个新的提交
+ `git log` 显示历史日志
+ `git log --all --graph --decorate` 可视化历史记录（有向无环图）
+ `git diff <filename>` 显示与暂存区文件的差异
+ `git diff <revisiokn> <filename>` 显示某个文件两个版本之间的差异
+ `git checkout <revision>` 更新HEAD和目前的分支
## 分支和合并
+ `git branch` 显示分支
+ `git branch <name>` 创建分支
+ `git checkout <name>` 切换到分支
  + `git checkout -b <name>` 创建分支并切换到该分支
+ `git merge <revision>` 合并分支到当前分支
+ `git mergetool` 使用工具来处理合并冲突
+ `git rebase` 将一系列补丁变基变为新的基线
## 远端操作
+ `git remote` 列出远端
+ `git remote add <name> <url>` 添加一个远端
+ `git push <remote> <local branch>:<remote branch>` 将对象传送至远端并更新远端引用
+ `git branch --set-upstream-to=<remote>/<remote branch>` 创建本地和远端分支的关联关系
+ `git fetch` 从远端获取对象/索引
+ `git pull` 相当于`git fetch; git merge`
+ `git clone` 从远端下载仓库
## 撤销
+ `git commit --amend` 编辑提交的内容或信息
+ `git reset HEAD <file>` 恢复暂存的文件
+ `git checkout -- <file>` 丢弃修改
## git高级操作
+ `git config` 可以设置git的相关参数
+ `git clone --depth=1` 浅克隆，不包括完整的版本历史信息
+ `git add -p` 交互式暂存
+ `git rebase -i` 交互式边基
+ `git blame` 查看最后修改某行的人
+ `git stash` 暂时移除工作目录下的修改内容
+ `git bisect` 通过二分查找搜索历史记录
