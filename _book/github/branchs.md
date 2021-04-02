# Github branchs

常用git操作：[链接](https://www.bootcss.com/p/git-guide/)

git 新建分支

*git checkout -b mdr_branch*  

git 切换分支

*git checkout mdr_branch*  

git  切换到主分支

*git checkout master*  

git 分支提交

*git push origin mdr_branch*  

git 删除分支（切换到其他分支）

本地：*git branch -d mdr_branch*   （ -D  强制删除）

远程： *git push origin --delete mdr_branch*  

git 查看所有分支

*git branch -a*

git 从分支拉取代码

 *git fetch origin mdr_branch*

git 分支代码合并（其他分支）

 *git merge mdr_branch*