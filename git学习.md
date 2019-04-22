# Git基础设置

1.&emsp;设置用户名

git config --global user.name 'username'

2.&emsp;设置用户名邮箱

git config --global user.email '邮箱'

(以上--global表示设置全局用户，--local设置本地用户,本地用户信息在.git/config下查看，全局用户信息在系统用户家目录下.gitconfig查看)
\#\# 查看本地用户信息
cat .git/config

\#\# 查看系统用户信息
cd \#进入家目录
cat .gitconfig



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

4.&emsp;**git commit -m '描述' [filename]**：提交文件到git仓库

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

# 将本地项目上传至GitHub

1.&emsp;git init

2.&emsp;git add . 或者 git add 文件夹

3.&emsp;git commit -m "注释"

4.&emsp;(若没有SHH KEY) ```ssh-keygen -t rsa -C "youremail@example.com"``` &emsp;用户目录下会出现id_rsa和id_rsa.pub.后者是公钥，添加到github的settings中的SSH and GPG keys 中

5.&emsp;GitHub上新建仓库，```git remote add origin git@github.com:smfx1314/test2.git``` 建立关联

6.&emsp;```git push -u origin master```将内容推送到远程仓库（若远程仓库不为空则先 ```git pull --rebase origin master```,然后再 ```git push origin master```）

7.&emsp;以后再次从本地仓库上传内容只需 ```git push origin master```



# 版本前进后退

git log 查看日志
git log --pretty=oneline 或 git reflog

\# 基于索引值的操作
git reset --hard 局部索引值

\# 使用^符号,几个^符号就后退几步
git reset --hard HEAD^
\#使用~符号接数字，表示后退几步
git reset --hard HEAD~7

\# git reset --hard --soft --mixed 三个参数对比

--soft仅在本地库移动HEAD指针
--mixed在本地库移动HEAD指针,重置暂存区
--hard在本地库移动HEAD指针，重置暂存区和工作区


# 比较文件差异
git diff [文件名] \#将工作区的文件和暂存区的文件比较
git diff [本地库中的历史版本] [文件名] \#将工作区中的文件和本地历史库记录比较
\#不带文件名比较多个符号

# 创建分支

master hot_fix feature_a feature_b ...

\#查看分支 
git branch -v

\# 创建分支
git branch [分支名]

\#查看分支
git branch -v

\# 切换分支
git checkout [分支名]
