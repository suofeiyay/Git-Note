# Introduction

Gitbook 安装

$ npm install gitbook-cli -g



Gitbook 创建

$ gitbook init



Gitbook 编译&预览

$ gitbook serve 

(本地打开：http://localhost:4000)



Gitbook支持输出

格式：HTML，PDF，JSON

PDF输出：

$ npm install gitbook -pdf -g



git 新建分支

git checkout -b mdr_branch  

git 切换分支

git checkout mdr_branch  

git  切换到主分支

git checkout master  

git 分支提交

git push origin mdr_branch  

git 删除分支（切换到其他分支）

本地：git branch -d mdr_branch   （ -D  强制删除）

远程： git push origin --delete mdr_branch  

git 查看所有分支

git branch -a

git 从分支拉取代码

 git fetch origin mdr_branch

git 分支代码合并（其他分支）

 git merge mdr_branch

