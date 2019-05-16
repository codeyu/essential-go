# 基本类型

Go 支持您期望从静态类型语言中获得的所有基本类型：

|    类型                                                            | 字面值        |
| ------------------------------------------------------------------ | ------------ |
| bool                                                               |  true, false |
| int, int8, uint8, in16, uint61, int32, uint32, int64, uint64       |  32          |
| char (int8 的别名, 1 字节字符)                                      |  'a'         |
| float64, float32 (浮点数)                                          |  23.5, 2e-12 |
| rune (int32 的别名, 1 unicode(4 字节) 字符)                         |  38          |
| string                                                             |  "foo", `bar`       |
| slice (可变大小的向量)                                              |  []int = {1, -3, 4} |
| array (固定长度的向量)                                              |  [2]int = {2, -3}   |
| map (在别的语言中被称为字典或哈希表)                                  |  map[string]int     |
| structs                                                            |  type Foo struct {} |
| constants                                                          |  const a = 8 |
