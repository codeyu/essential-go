# Mac OS 系统安装和设置
## 安装
### 使用官方安装包
从 https://golang.org/dl/ 下载 .pkg 安装程序并运行它。

### 使用Homebrew
* 如果您没有安装 Homebrew，请按照[说明](https://brew.sh/)进行安装
* `brew install go`

## 设置
安装后，您需要配置`GOPATH`环境变量。

从 Go 1.8 开始，GOPATH环境变量的默认值为`$HOME/go`，因此您可以跳过设置它。

创建 go 目录 `mkdir $HOME/go`。

将以下内容添加到您的 `~/.bash_profile` 文件中：
```bash
 export  GOPATH = $HOME/go
 export  PATH = $PATH:$GOPATH/bin
```
运行 `source ~/.bash_profile` 或启动新终端以使更改生效。

### 说明
默认情况下，文件 `~/.bash_profile` 在 bash shell 启动时执行。

通过添加命令，我们在每个shell会话中都可以使用 `GOPATH`。

方便起见，添加`$GOPATH/bin`到`PATH`。当您用 `go get ...`安装Go程序时，您将能够在不键入完整路径的情况下调用它们。例如，你会运行`gotest1`而不是运行`$HOME/go/bin/gotest1`。

### 更多配置
要快速 `cd` 到Go源代码的目录，我将 `bash alias` 添加到`~/.bash_profile`：
```bash
alias cdgo="cd $GOPATH/src/github.com/kjk"
```
您需要更改 `github.com/kjk` 为您的GitHub帐户。

您应该了解 `GOPATH` 在 go 工具中的作用。
