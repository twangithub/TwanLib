#### git获取分支:
如何只克隆git仓库中的一个分支？ : git clone -b <branch> <remote_repo>   例如： git clone -b 指定的分支名字 git地址


## git提交常用 
 > 提交步骤:
 1. 打开 Gitbash
 2. 使用 cd 命令用于切换到对应仓库的目录，cd .. 用于切换到上级目录，ls 用于查看当前目录下面的文件/夹
 3. 当修改了一段代码后，使用 git status 查看当前改动
 4. 如果需要把所有改动提交上去，使用 git add . 提交到缓冲区（此时文件并没有提交到远程仓库）
 5. 填写提交说明，使用 git commit -m '此处填写修改的内容' 命令
 6. 使用 git pull origin master 获取远程仓库master分支的最新改动。（如果远程仓库有更新，没有执行此步骤，无法进行下一步）
 7. 使用 git push origin master 提交改动到远程仓库
 8. github 的 Demo 默认使用 gh-pages 分支，Demo 地址是：http://用户名.github.io/仓库名/ 可以使用 git checkout gh-pages 切换到该分支(默认没有这     个分支，需要使用git checkout -b gh-pages创建该分支)。
