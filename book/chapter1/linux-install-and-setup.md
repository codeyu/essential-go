# Linux 系统安装和设置
## 在 Ubuntu 上安装

### 使用 Ubuntu 提供的包

```bash
$ sudo apt-get update
$ sudo apt-get install golang-go
```
Ubuntu 提供的软件包经常过时。每6个月发布一个新版本的Go，但Ubuntu发行速度较慢。

通常可以通过`ppa:gophers/archive`包存储库获得更新的版本：

```bash
$ sudo add-apt-repository ppa:gophers/archive
$ sudo apt-get update
$ sudo apt-get install golang-1.11-go
```
如果那些版本仍然不满足要求，你可以安装linux二进制安装包。

### 使用二进制安装包
这些说明适用于大多数Linux发行版：

```bash
$ sudo apt-get update
$ sudo apt-get install -y build-essential git curl wget
$ wget https://storage.googleapis.com/golang/go<versions>.gz
```

您可以在[此处](https://golang.org/doc/install)找到版本列表。

```bash
# 下载 go1.12.4 安装包
$ wget https://storage.googleapis.com/golang/go1.12.4.linux-amd64.tar.gz

# 解压文件
$ sudo tar -C /usr/local -xzf go1.12.4.linux-amd64.tar.gz
$ sudo chown -R $USER:$USER /usr/local/go
$ rm go1.12.4.linux-amd64.tar.gz
```

## 设置
安装后，您需要配置 `GOPATH` 环境变量。

从 Go 1.8 开始，`GOPATH` 环境变量的默认值为 `$HOME/go`，因此您可以跳过设置它。

使用 `mkdir $HOME/go` 创建 go 目录。

在 `~/.bashrc` 文件末尾添加以下两行
```bash
export GOPATH=$HOME/go
export PATH=$GOPATH/bin:/usr/local/go/bin:$PATH
```
执行以下命令使更改生效：
```bash
$ source ~/.bashrc
```
通过运行`go version`测试安装是否成功。

您应该了解 `GOPATH` 在 go 工具中的作用。

**更多资源：**

* https://golang.org/dl/ 是Go官方下载页面
* https://golang.org/doc/install 是官方安装说明
* https://github.com/golang/go/wiki/Ubuntu 是Ubuntu的官方安装说明
