# 字符和 rune

Go有两种类型的字符：

* `byte` 是一个 1 字节的值，`uint8` 类型的别名
* `rune` 是一个 4 字节的 Unicode 代码点，`int32` 类型的别名

`byte` 和 `rune` 的[零值](zero-values.md)为 0。

## 使用 byte 遍历 string

<iframe src='https://glot.io/snippets/fapbqod2xr/embed' frameborder='0' scrolling='no' sandbox='allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts' width='600' height='400'></iframe>
 
## 使用 rune 遍历 string
 
 <iframe src='https://glot.io/snippets/fapbqp3ez8/embed' frameborder='0' scrolling='no' sandbox='allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts' width='600' height='400'></iframe>
 
一个字符串是一个 byte 数组。

当将字符串迭代为 rune 时，我们假设该字符串是 Unicode 字符串，编码为 UTF-8。

UTF-8 是一种可变长度编码，其中 rune 可以编码为 1,2,3 或 4 个字节。

返回的索引 `i` 是 rune 开始的字符串中的字节位置。这不是一个 rune 计数。
