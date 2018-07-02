#### git获取分支:
如何只克隆git仓库中的一个分支？ : git clone -b <branch> <remote_repo>   例如： git clone -b 指定的分支名字 git地址

> 推荐Android studio 版本管理插件
  .ignore

## Git提交 
 > 提交步骤:
 1. 打开 Gitbash
 2. 使用 cd 命令用于切换到对应仓库的目录，cd .. 用于切换到上级目录，ls 用于查看当前目录下面的文件/夹
 3. 当修改了一段代码后，使用 git status 查看当前改动
 4. 如果需要把所有改动提交上去，使用 git add . 提交到缓冲区（此时文件并没有提交到远程仓库）
 5. 填写提交说明，使用 git commit -m '此处填写修改的内容' 命令
 6. 使用 git pull origin master 获取远程仓库master分支的最新改动。（如果远程仓库有更新，没有执行此步骤，无法进行下一步）
 7. 使用 git push origin master 提交改动到远程仓库
 8. github 的 Demo 默认使用 gh-pages 分支，Demo 地址是：http://用户名.github.io/仓库名/ 可以使用 git checkout gh-pages 切换到该分支(默认没有这     个分支，需要使用git checkout -b gh-pages创建该分支)。

## Git pull 并强制覆盖本地文件
- git fetch --all
- git reset --hard origin/master
- git pull

- $ git push origin :test              // 刚提交到远程的test将被删除，但是本地还会保存的，不用担心
- 删除分支：$ git branch -d [name]  -d选项只能删除已经参与了合并的分支，对于未有合并的分支是无法删除的。如果想强制删除一个分支，可以使用-D选项
- 本地分支push到远程(创建远程分支)：$ git push origin [name]

## 重命名本地和远程分支的名字
- git branch -m old_branch new_branch         # Rename branch locally    
- git push origin :old_branch                 # Delete the old branch    
- git push --set-upstream origin new_branch   # Push the new branch, set local branch to track the new remote

## 将开发完成的分支合并到master
- $ git checkout master ;// 先切换到主分支
- $ git merge dev ;//然后把开发好的dev分支合并到master
- ($ git branch -d dev);//删除dev分支,当然也可以不删
- $ git push origin master (提交到远程库)

## 如何使用某一分支(切换分支之前，一定要提交当前分支的修改)
- git branch -r #查看远程分支
- git branch -a #查看所有分支
- git checkout origin/daily/1.4.1  //使用某一分支

## git忽略规则及.gitignore规则不生效的解决办法
- git rm -r --cached .
- git add .
- git commit -m "update .gitignore"

## 移除某目录的版本管理
- git rm  UMLibrary/build -r -f  
- git commit 
