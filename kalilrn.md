# kali linux 安装Tor浏览器

tor github地址：
https://github.com/TheTorProject/gettorbrowser
本地文件 tor-browser
解压后进入Browser/start-tor-browser,搜索root,把0改为其他数字
配置适当的参数后即可运行

# kali linux 安装shadowsocks
 第一步： 下载软件包到kaliLinux上。

wget https://github.com/shadowsocks/shadowsocks/archive/master.zip

第二步： 解压软件包，进入解压后的目录，进行安装

unzip master.zip 　　--解压
切换到解压后的目录下
cd master
python setup.py install ---安装

第三步:配置shadowsocks配置文件，启动shadowsocks
先配置shadowsocks配置文件
copy 目录中的config.json.sample 改下名
copy config.json.sample config.json
vi config.json

{
"server":"服务器IP或域名",
"server_port":服务器提供的端口,
"password":"密码",
"local_port": 本地提供的端口 这里假设1111 ,
"timeout":300,
"method":"加密方式 这里假设rc4-md5"
}

启动shadowsocks
sslocal -c config.json -d start

配置完毕后，需要打开火狐浏览器，设置socks代理
输入代理ip为127.0.0.1 端口为1080 即可


# 火狐浏览器插件Hoxx VPN Proxy
查找free-ss.site寻找免费ss代理 
