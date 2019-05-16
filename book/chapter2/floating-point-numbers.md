# 浮点数

Go 具有与 [IEEE 754 标准](https://zh.wikipedia.org/wiki/IEEE_754)相符合的浮点数：

* `float32` 是一个 4 字节的浮点数（在 C 语言中称为 `float`）
* `float64` 是一个 8 字节的浮点数（在 C 语言中称为 `double`）

`float32` 和 `float64` 的[零值](zero-values.md)是 0.0。

## 用 `FormatFloat` 函数将 float 转换为 string
<iframe src='https://glot.io/snippets/fapbqjsht0/embed' frameborder='0' scrolling='no' sandbox='allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts' width='600' height='400'></iframe>

## 用 `Sprintf` 函数将 float 转换为 string
<iframe src='https://glot.io/snippets/fapbqlbua1/embed' frameborder='0' scrolling='no' sandbox='allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts' width='600' height='400'></iframe>

与 `fmt.Sprintf` 相比， `strconv.FormatFloat` 更快。

## 用 `ParseFloat` 函数将 string 转换为 float
<iframe src='https://glot.io/snippets/fapbqmctgl/embed' frameborder='0' scrolling='no' sandbox='allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts' width='600' height='400'></iframe>

## 用 `Sscanf` 函数将 string 转换为 float
<iframe src='https://glot.io/snippets/fapbqn55tw/embed' frameborder='0' scrolling='no' sandbox='allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts' width='600' height='400'></iframe>
