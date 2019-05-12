# 离线访问文档

要在本地浏览完整文档，请运行：
```bash
$ godoc -http=localhost:9000
```
然后在浏览器中打开 [localhost:9000](http://localhost:9000/)。它将显示与https://golang.org/doc/ 相同的内容。

您可以在本地运行官方指南：

```bash
$ go get golang.org/x/tour/gotour
$ go tool tour
```
这在本地运行 https://tour.golang.org/ 。

您可以使用 `godoc` 快速参考命令。例如，要查看以下文档 `fmt.Print`：

```bash
$ godoc cmd/fmt Print
```
命令行中也提供了常规帮助：

```bash
$ go help [command]
```
例如，要查看`go build`命令的帮助文档，使用 `go help build`。