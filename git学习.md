# Git基础设置

1.&emsp;设置用户名

git config --global user.name 'username'

2.&emsp;设置用户名邮箱

git config --global user.email '邮箱'

3.&emsp;查看配置信息

git config --list

4.&emsp;初始化仓库

git init

# git有三个部分：

1.工作区 

2.暂存区 

3.仓库

# git文件的提交流程：

1.&emsp;**git status** : 查看文件状态

2.&emsp;**git add 'filename'**：添加工作区的文件到暂存区

3.&emsp;**git status**：查看文件状态

4.&emsp;**git commit -m '描述'**：提交文件到git仓库

5.&emsp;**git status**：查看文件状态

# git文件删除流程：

1.&emsp;工作区中删除文件

2.&emsp;git rm 文件名：暂存区中删除文件

3.&emsp;git commit -m '提交描述'：提交删除操作

# git 远程仓库

## git 克隆操作：

&emsp;git clone 仓库地址

## git 提交到远程仓库

&emsp;文件提交或删除流程

&em sp;git push

# github 远程添加文件

Get started by creating a new file or uploading an existing file. We recommend every repository include a README, LICENSE, and .gitignore.



…or create a new repository on the command line  
echo "# 19970126ljl.github.io" >> README.md  
git init  
git add README.md  
git commit -m "first commit"  
git remote add origin https://github.com/19970126ljl/19970126ljl.github.io.git  
git push -u origin master  



…or push an existing repository from the command line  
git remote add origin https://github.com/19970126ljl/19970126ljl.github.io.git  
git push -u origin master  
…or import code from another repository  
You can initialize this repository with code from a Subversion, Mercurial, or TFS project.  

# 个人站点

## 访问:  
_https://用户名.github.io_

## 搭建

1.&emsp;新建仓库（仓库名必须为 用户名.github.io）

2.&emsp;在仓库下新建index.html

# 项目站点

## 访问：

_https://用户名.github.io/仓库名_

## 搭建：

1.&emsp;进入项目主页点击settings

2.&emsp; 在settings页面，点击 **GitHub Pages** 内部的按钮





