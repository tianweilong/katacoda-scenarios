This is your first step.

## Task

apt-get 升级更新 

`sudo apt-get update && sudo apt-get -y upgrade`{{execute}}

获取Go 1.12 安装包

`wget https://dl.google.com/go/go1.12.6.linux-amd64.tar.gz`{{execute}}

解压安装包，移动go文件夹到/usr/local下

`sudo tar -xvf go1.12.6.linux-amd64.tar.gz`{{execute}}

`sudo mv go /usr/local`{{execute}}

设置相关环境变量

`export GOROOT=/usr/local/go`{{execute}}

`mkdir -p $HOME/Projects/Demo && export GOPATH=$HOME/Projects/Demo` {{execute}}


验证安装

`go version`{{execute}}

`go env` {{execute}}

