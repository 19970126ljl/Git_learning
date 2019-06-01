## 隐藏任务栏和顶栏  
sudo vi /usr/share/gnome-shell/theme/gnome-classic.css  
/* TOP BAR */处height改为0

sudo rm -rf /usr/share/gnome-shell/extensions/window-list@gnome-shell-extensions.gcampax.github.com  
alt+F2 输入r

## 安装chrome  
sudo vi /etc/yum.repos.d/google-chrome.repo  

输入：  
[google-chrome] 

name=google-chrome 

baseurl=http://dl.google.com/linux/chrome/rpm/stable/$basearch 

enabled=1

gpgcheck=1 

gpgkey=https://dl-ssl.google.com/linux/linux_signing_key.pub

保存退出后  yum -y install google-chrome-stable --nogpgcheck

## supertab
直接下载

下载以后放到~/.vim文件夹中

http://www.vim.org/scripts/script.php?script_id=1643

【插件配置】

在~/.vimrc中添加以下配置

let g:SuperTabRetainCompletionType=2
其中

" 0 - 不记录上次的补全方式
" 1 - 记住上次的补全方式,直到用其他的补全命令改变它
" 2 - 记住上次的补全方式,直到按ESC退出插入模式为止
