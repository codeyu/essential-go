# 基本类型

Go支持您期望从静态类型语言中获得的所有基本类型：

|    类型                                                            | 字面值        |
| ------------------------------------------------------------------ | ------------ |
| bool                                                               |  true, false |
| int, int8, uint8, in16, uint61, int32, uint32, int64, uint64       |  32          |
| char (alias of int8, a byte character)                             |  'a'         |
| float64, float32 (floating-point numbers)                          |  23.5, 2e-12 |
| rune (alias of int32, a unicode character)                         |  38          |
| string                                                             |  "foo", `bar`       |
| slice (variable-sized vector)                                      |  []int = {1, -3, 4} |
| array (fixed-size vector)                                          |  [2]int = {2, -3}   |
| map (known as dictionary or hash table in other languages)         |  map[string]int     |
| structs                                                            |  type Foo struct {} |
| constants                                                          |  const a = 8 |
