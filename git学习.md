# Git基础设置

1.&emsp;设置用户名

git config --global user.name 'username'

2.&emsp;设置用户名邮箱

git config --global user.email '邮箱'

3.&emsp;查看配置信息

git config --list

4.&emsp;初始化仓库

git init

## git有三个部分：1.工作区 2.暂存区 3.仓库

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





