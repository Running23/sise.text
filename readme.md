## **学习笔记**
**_2019.09.12._** 查看Linux是否安装好对应开发环境  
SVN--version;  
ls -al:显示隐藏的文件  
**_2019.09.19._** CentOS下搭建git服务器  (https://www.runoob.com/git/git-server.html)  
**a**.使用yum源在线安装git服务器:yum install -y git；  
**b**.创建一个git用户,用来运行git服务:adduser git;  
**c**.修改git用户密码：passwd git;  
**d**.创建一个目录，用作Git仓库；  
**e**.初始化git仓库:git init --bare VersionControlServer.git,初始化空的 Git 版本库于 /home/git/  
**f**.把仓库的owner改为git用户:chown -R git:git  /home/git/  
**g**.客户端git配置  
* ssh:登录
git clone ssh://git@sxq.ngrok2.xiaomiqiu.cn:9922/home/git/VersionControlServer.git  
* 修改配置文件,服务器直接登录，配置文件路径C:\Users\Administrator\.ssh\config，修改内容如下：  
****  
    Host sxq.ngrok2.xiaomiqiu.cn  
    HostName sxq.ngrok2.xiaomiqiu.cn  
    User git  
    Port 9922  
****  
修改完上面配置后，即可通过下面方式拉取代码库  
git clone sxq.ngrok2.xiaomiqiu.cn:/home/git/VersionControlServer.git  
* ssh登录
ssh -p 9922 git@sxq.ngrok2.xiaomiqiu.cn


[参考文档]：https://git-scm.com/book/en/v2/Git-on-the-Server-Setting-Up-the-Server  
**_2019.09.21._** https://ken.io/note/centos7-jenkins-install-tutorial
