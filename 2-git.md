#### 常用Git命令清单

> 工作区（Workspace）； 暂存区（Index/Stage）； 仓库区（Repository）； 远程仓库（Remote）

###### 1.新建代码库

```bash
$ git init  #在当前目录新建一个Git代码库
$ git clone [url]  #下载一个项目和它的整个代码历史
```

###### 2.增加/删除文件

```bash
$ git add .  #添加文件到暂存区
$ git rm file1  #删除工作区文件，并且将这次删除放入暂存区
```

###### 3.代码提交

```bash
$ git commit -m [message]  #提交暂存区到仓库区
```

###### 4.分支

```bash
$ git branch  #列出所有本地分支
$ git branch -r  #列出所有远程分支
$ git branch [branch-name]  #新建一个分支，但是停留在当前分支
$ git checkout -b [branch] [remote-branch] #新建一个分支，并切换到该分支
$ git branch --track [branch] [remote-branch]  #新建一个分支，与指定远程分支建立追踪关系
$ git checkout [branch-name]  #切换到指定分支，并更新工作区
$ git branch --set-upstream [branch] [remote-branch]  #建立追踪关系，在现有分支与指定远程分支之间
$ git merge [branch] --no-ff -m [message] #合并指定分支到当前分支
$ git branch -d [branch-name]  #删除远程分支
$ git push origin local-branch:remote-branch #推送本地代码到远程分支
$ git push origin :remote-branch #删除远程分支
```

###### 5.查看信息

```bash
$ git status  #显示有变更的文件
$ git diff  #显示暂存区和工作区的差异
$ git stash  #暂存本地代码
$ git stash pop  #恢复暂存代码
```

###### 6.远程同步

```bash
$ git remote add shortname  #增加一个新的远程仓库，并命名
$ git remote rm origin  #删除远程分支
$ git pull remote  #取回远程仓库的变化，并与本地分支合并
$ git push remote  #上传本地指定分支到远程仓库
$ git remote set-url origin [url]  #修改远程地址
```

###### 7.撤销

```bash
$ git checkout .  #恢复暂存区的指定文件到工作区
$ git reset --hard  #重置暂存区与工作区，与上一次commit一致
```

#### 实战

###### 1. 合并远程分支代码并处理冲突

```bash
$ git pull  #拉所有远程代码
$ git checkout iteration_1  #切换到远程对应的本地分支
$ git pull  #保证代码最新再拉一次
$ git checkout customForm  #切换回本地分支
$ git merge iteration_1 --no-ff  #合并分支代码
#解决冲突:tortiseGit-->Resolve查看区别，然后解决冲突
$ git commit  #提交代码
$ git push  #推到远程
```