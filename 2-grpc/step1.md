第一步：

## 任务

更新apt-get

`sudo apt-get update`{{execute T1}}

查看Go版本，gRPC需要go 1.6版本或更高

`go version`{{execute T1}}

获取GRPC-GO代码代码库

`go get -u -v google.golang.org/grpc`{{execute T1}}

安装Protocol Buffers v3

- 安装wget

  `sudo apt-get install wget`{{execute T1}}
 
- 获取二进制安装包
  
  `wget https://github.com/protocolbuffers/protobuf/releases/download/v3.9.0/protoc-3.9.0-linux-x86_64.zip`{{execute T1}}
  
- 解压文件

  `sudo apt-get install unzip && mkdir protoc && unzip -d protoc -o protoc-3.9.0-linux-x86_64.zip`{{execute T1}}
  
- 设置protoc环境变量
 
  `echo 'export PATH=/home/scrapbook/tutorial/protoc/bin:$PATH' >> ~/.bashrc && source ~/.bashrc`{{execute T1}}
  
- 安装protoc插件
  
  `go get -u -v github.com/golang/protobuf/protoc-gen-go`{{execute T1}}

- 设置GOBIN环境变量
  
  `echo 'export PATH=$PATH:$GOPATH/bin' >> ~/.bashrc && source ~/.bashrc`{{execute T1}}


运行服务端代码：

`cd $GOPATH/src/google.golang.org/grpc/examples/helloworld`{{execute T1}}

`go run greeter_server/main.go`{{execute T1}}


运行客户端代码:

`cd $GOPATH/src/google.golang.org/grpc/examples/helloworld`{{execute T2}}

`go run greeter_client/main.go`{{execute T2}}





