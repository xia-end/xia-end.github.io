# Node.js笔记
## Node.js的下载安装
>下载地址:https://nodejs.org/en/download/
>安装:
>Ubuntu 源码安装 Node.js
以下部分我们将介绍在 Ubuntu Linux 下使用源码安装 Node.js 。 其他的 Linux 系统，如 Centos 等类似如下安装步骤。

>在 Github 上获取 Node.js 源码：

>$ sudo git clone https://github.com/nodejs/node.git
>Cloning into 'node'...
>修改目录权限：
>$ sudo chmod -R 755 node
>使用 ./configure 创建编译文件，并按照：
 >$ cd node
>$ sudo ./configure
>$ sudo make
>$ sudo make install
>查看 node 版本：
$ node --version
v0.10.25
Ubuntu apt-get命令安装
命令格式如下：
sudo apt-get install nodejs
sudo apt-get install npm

## Node.js的特性
>1. 单线程
>2. 非阻塞I/O
>3.事件驱动event-driven
