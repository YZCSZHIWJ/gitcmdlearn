git cmd use test
===

## git init

#### git init
- 初始化一个仓库



## git config

#### git config -l
- 查看配置

#### git config --global user.name name
- 全局配置

#### git config --global --unset user.name
- 取消全局配置

#### git config [--global] --edit
- 直接编辑配置项



## git add

#### git add .
- 添加所有改动

#### git add file1, file2
- 添加文件file1,file2



## git commit

#### git commit -m 'xx'
- 提交到本地仓库



## git status

#### git status 
- 查看仓库当前的状态



## git diff

#### git diff file
- 查看比较历史与修改过的文件file



## git log

#### git log
- 查看提交的历史记录

#### git log --pretty=oneline
- 提交历史单行显示

#### git log --graph
- 显示分支合并图



## git reset

#### git reset --hard HEAD^
- 退回到上个版本

#### git reset --hard HEAD~n
- 退回到上n个版本

#### git reset --hard command_id
- 回到第command_id版本id的版本上

#### git reset HEAD file
- 把暂存区file的修改撤销掉（unstage），重新放回工作区（即撤销git add file操作）



## git reflog

#### git reflog 
- 记录每一次对仓库产生影响的命令，比如commit,reset



## git checkout

#### git checkout -- file
- 把readme.txt文件在工作区的修改全部撤销，这里有两种情况:
- file 自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态
- file 已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态

#### git checkout -b dev
- 新建dev分支，并且切换到dev分支上

#### git checkout dev
- 切换到dev分支



## git rm

#### git rm file
- 用于删除一个文件file



## git remote

#### git remote add origin https://github.com/YZCSZHIWJ/gitcmdlearn.git
- 添加一个远程仓库命名为origin

### git remote -v
- 查看远程仓库信息

#### git remote rm origin
- 删除已有的GitHub远程库



## git push

#### git push -u origin master
- 将本地仓库推送至远程仓库的master分支
- 首次推送加上了-u参数，Git不但会把本地的master分支内容推送到远程新的master分支上，还会把本地的master分支和远程的master分支关联起

#### git push origin --tags
- 推送全部未推送过的本地标签到远程仓库

#### git push origin <tagname>
- 将标签推送到远程仓库

#### git push origin :refs/tags/<tagname>
- 删除一个远程标签



## git clone

#### git clone https://github.com/YZCSZHIWJ/gitcmdlearn.git
- 克隆远程的仓库到本地



## git branch 

#### git branch 
- 列出所有分支，当前分支前面会标一个*

#### git branch dev
- 新建dev分支

#### git branch -d dev
- 删除dev分支

#### git branch --set-upstream dev origin/dev
- 指定本地dev分支与远程origin/dev分支的链接



## git merge 

#### git merge dev
- 合并dev分支到当前分支中

#### git merge --no-ff -m 'commit commend' dev
- 强制使用普通模式合并，合并后的历史有分支，能看出来曾经做过合并



## git stash

#### git stash 
- 冻结当前操作

#### git stash list
- 查看当前冻结栈

#### git stash apply 
- 恢复冻结，但不删除冻结信息

#### git stash drop
- 删除冻结信息

#### git stash pop 
- 恢复并删除冻结信息



## git tag

#### git tag
- 查看所有的标签

#### git tag <name>
- 在当前分支的当前位置打上标签

#### git tag <name> commit_id
- 在当前分支的commit_id的提交位置打上标签

#### git tag -a <tagname> -m "comment" commit_id
- 在当前分支的commit_id上打上带备注的标签

#### git tag -d <tagname>
- 可以删除一个本地标签



## git show

#### git show <tagname>
- 查看标签的信息