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



## git reset

#### git reset --hard HEAD^
- 退回到上个版本

#### git reset --hard HEAD~n
- 退回到上n个版本

#### git reset --hard command_id
- 回到第command_id版本id的版本上



## git reflog

#### git reflog 
- 记录每一次对仓库产生影响的命令，比如commit,reset



## git checkout

#### git checkout -- file
- file 自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态
- file 已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态



