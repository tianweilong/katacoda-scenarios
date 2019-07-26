第一步：

## 任务

更新apt-get

`sudo apt-get update`{{execute}}

查看Go版本，gRPC需要go 1.6版本或更高

`go version`{{execute}}

获取GRPC-GO代码代码库

`go get -u -v google.golang.org/grpc`{{execute}}

安装Protocol Buffers v3

- 安装wget

  `sudo apt-get install wget`{{execute}}
 
- 获取二进制安装包
  
  `wget https://github.com/protocolbuffers/protobuf/releases/download/v3.9.0/protoc-3.9.0-linux-x86_64.zip`{{execute}}
  
- 解压文件

  `sudo apt-get install unzip && mkdir protoc && unzip -d protoc -o protoc-3.9.0-linux-x86_64.zip`{{execute}}
  
- 设置protoc环境变量
 
  `export PATH=/home/scrapbook/tutorial/protoc/bin:$PATH`{{execute}}
  
- 安装protoc插件
  
  `go get -u github.com/golang/protobuf/protoc-gen-go`{{execute}}

- 设置GOBIN环境变量
  
  `export PATH=$PATH:$GOPATH/bin`{{execute}}






