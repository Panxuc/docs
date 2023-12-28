# 正则表达式

正则表达式（Regular expression，即 regex），是一种用简单字符串来描述、匹配指定格式的字符串的方法，现在很多文本编辑器、程序设计语言都支持用正则表达式操作匹配指定格式的字符串。

在日常生活中很多地方都可以用到正则表达式，比如撰写 `.gitignore` 文件、搜索文件、替换文本、爬虫等等。

## 正则表达式元字符和特性

### 字符匹配

- 普通字符：普通字符按照字面意义进行匹配，例如匹配字母 "a" 将匹配到文本中的 "a" 字符。
- 元字符：元字符具有特殊的含义，例如 `\d` 匹配任意数字字符，`\w` 匹配任意字母数字字符，`.` 匹配任意字符（除了换行符）等。

### 量词

- `*`：匹配前面的模式零次或多次。
- `+`：匹配前面的模式一次或多次。
- `?`：匹配前面的模式零次或一次。
- `{n}`：匹配前面的模式恰好 n 次。
- `{n,}`：匹配前面的模式至少 n 次。
- `{n,m}`：匹配前面的模式至少 n 次且不超过 m 次。

### 字符类

- `[ ]`：匹配括号内的任意一个字符。例如，`[abc]` 匹配字符 "a"、"b" 或 "c"。
- `[^ ]`：匹配除了括号内的字符以外的任意一个字符。例如，`[^abc]` 匹配除了字符 "a"、"b" 或 "c" 以外的任意字符。

### 边界匹配

- `^`：匹配字符串的开头。
- `$`：匹配字符串的结尾。
- `\b`：匹配单词边界。
- `\B`：匹配非单词边界。

### 分组和捕获

- `( )`：用于分组和捕获子表达式。
- `(?: )`：用于分组但不捕获子表达式。

### 特殊字符

- `\`：转义字符，用于匹配特殊字符本身。
- `.`：匹配任意字符（除了换行符）。
- `|`：用于指定多个模式的选择。

## 正则表达式语法

### 普通字符

- `a`：匹配字符 "a"。
- `abc`：匹配字符串 "abc"。
- `[ABC]`：匹配字符 "A"、"B" 或 "C"。
- `[^ABC]`：匹配除了字符 "A"、"B" 或 "C" 以外的任意字符。
- `[A-Z]`：匹配任意大写字母。
- `.`：匹配任意字符（除了换行符（`\n`、`\r`））。
- `\`：转义字符，用于匹配特殊字符本身。
- `\d`：匹配任意数字字符，等价于 `[0-9]`。
- `\D`：匹配任意非数字字符，等价于 `[^0-9]`。
- `\w`：匹配任意字母数字下划线字符，等价于 `[A-Za-z0-9_]`。
- `\W`：匹配任意非字母数字下划线字符，等价于 `[^A-Za-z0-9_]`。

### 非打印字符

- `\cx`：匹配由 `x` 指明的控制字符。例如，`\cM` 匹配一个 Control-M 或回车符。
- `\f`：匹配一个换页符。
- `\n`：匹配一个换行符。
- `\r`：匹配一个回车符。
- `\s`：匹配任意空白字符，等价于 `[\f\n\r\t\v]`。
- `\S`：匹配任意非空白字符，等价于 `[^\f\n\r\t\v]`。
- `\t`：匹配一个制表符。
- `\v`：匹配一个垂直制表符。