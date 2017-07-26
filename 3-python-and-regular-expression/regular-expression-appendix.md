# 正则表达式附录

这些是 ACN 内容定制的常用正则表达式。

## `/support/legal/sla/([\w\-]+)`

JSON 转义版：`"/support/legal/sla/([\\w\\-]+)"`

这是用于匹配某个 Azure 服务 SLA 在 Azure 国际版的 URL。`([\\w\\-]+)` 匹配的是某个 Azure 服务，例如 `virtual-machines`。

因为 Azure.cn 的 SLA 链接与国际版不太一样。例如，国际版的虚拟机 SLA 为 `/support/legal/sla/virtual-machines`，而 Azure.cn 的为 `/support/sla/virtual-machines`。所以匹配到的字符串需要做以下的替换 `/support/sla/\\1`。

## `(ms\.date: +['"]?[\d/]+['"]?[ \t\r\f\v]*)\n`

JSON 转义版：`"(ms\\.date: +['\"]?[\\d/]+['\"]?[ \\t\\r\\f\\v]*)\n"`

这是用于匹配 meta data 中的 ms.date 的一整行。

这个正则表达式可以用于添加 wacn.date。使用以下的字符串替换，即可添加一个空的 wacn.date：`\\1\nwacn.date: ''\n`

### OPS 变形：`(ms\.date: +(['"]?[\d/]+['"]?)[ \t\r\f\v]*)\n`

JSON 转义版：`"(ms\\.date: +(['\"]?[\\d/]+['\"]?)[ \\t\\r\\f\\v]*)\n"`

这个正则表达式只是在之前那个里简单了加了一对括号而已。由于在 OPS 中，我们要使用 ms.date 替换 wacn.date，而用 origin.date 代替原来的 ms.date，所以用括号括住日期，便可以做适当的替换。用以下的字符串替换，即可得到适合 OPS 的日期形式：`origin.date: \\2\nms.date: ''\n`。

### 其他变形

#### `ms\.date: +['"]?(\d)/(\d/)(\d\d\d\d)['"]?`

JSON 转义版：`"ms\\.date: +['\"]?(\\d)/(\\d/)(\\d\\d\\d\\d)['\"]?"`

#### `ms\.date: +['"]?(\d)/(\d\d/)(\d\d\d\d)['"]?`

JSON 转义版：`"ms\\.date: +['\"]?(\\d)/(\\d\\d/)(\\d\\d\\d\\d)['\"]?"`

#### `ms\.date: +['"]?(\d\d)/(\d/)(\d\d\d\d)['"]?`

JSON 转义版：`"ms\\.date: +['\"]?(\\d\\d)/(\\d/)(\\d\\d\\d\\d)['\"]?"`

## `\[([^\[\]]*)\]\s*\(https?://azure\.microsoft\.com/(en-us/)?services/([\w|\-]+)/?\)`

JSON 转义版：`"\\[([^\\[\\]]*)\\]\\s*\\(https?://azure\\.microsoft\\.com/(en-us/)?services/([\\w|\\-]+)/?\\)"`

## `(\]:\s*|href\s*=\s*["']|\]\(|redirect_url:\s*)(https?://docs\.microsoft\.com)?(/en-us)?/(\w+)(/[\w\-\d]+|)`

JSON 转义版：`"(\\]:\\s*|href\\s*=\\s*[\"']|\\]\\(|redirect_url:\\s*)(https?://docs\\.microsoft\\.com)?(/en-us)?/(\\w+)(/[\\w\\-\\d]+|)"`

## `(A|a)zure(\s+)(P|p)ortal`

JSON 转义版：`"(A|a)zure(\\s+)(P|p)ortal"`

## `//azure\.microsoft\.com/documentation/templates(/\w|/?.)`

JSON 转义版：`"//azure\\.microsoft\\.com/documentation/templates(/\\w|/?.)"`

## ``