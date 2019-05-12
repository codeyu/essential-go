# GOPATH, GoROOT, GOBIN

## GOPATH
如果您有其他编程语言的经验，您可能习惯将源代码放在文件系统的任何位置。

但 Go tools 需要一定的源代码布局。

`GOPATH` 是**工作区**的根，包含以下文件夹：

* src - 源文件的位置：`.go`，`.c`，`.g`，`.s`
* pkg - 已编译软件包（`.a`文件）的位置
* bin - Go构建的可执行文件的位置

与 `PATH` 环境变量一样，`GOPATH` 的值是一个用 `:`（在Windows上是`;`）分隔的目录列表。

Go 根据 `GOPATH` 的目录列表查找包（库）。

`go get` 工具将包下载到 `GOPATH` 的第一个目录中。

从 Go 1.8 开始，如果未设置环境变量 `GOPATH`，则在 Unix/Linux 系统中默认为`$HOME/go`，在 Windows 系统中默认为 `%USERPROFILE%/go`。

有些工具假设 `GOPATH` 只包含一个目录。

## GOBIN

运行 `go install`和`go get` 命令编译 main 包生成可执行文件的位置。

通常将其设置在系统 `PATH` 环境变量中的某个位置，以便可以轻松运行和发现已安装的可执行文件。

路径一般为：`$GOPATH/bin`，如无特殊需求不需单独设置 `GOBIN`。

## GOROOT
这是Go安装的位置。它用于查找标准库。

由于Go将构建路径嵌入到工具链中，所以很少需要设置此变量。如果安装目录和构建目录（或构建时所设置的值）不同。需要设置 `GOROOT`。 

有关环境变量的完整列表，请参阅 `go env`。