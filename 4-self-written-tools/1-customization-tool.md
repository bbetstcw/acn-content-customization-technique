# 定制工具

## 概述

这已经是这个定制工具的第三版。从最初的 Steven 开始的只是简单地使用正则表达式对文字进行替换，加上我写的，使用 python 内置比较器，通过文档比较保留之前定制的进阶版；到后来的合并到 SourceTreeScript 项目，并对文字替换工具进行了优化，把进阶版与 Git 结合使用；在到最后，文字替换工具基本稳定，而且可扩展，而进阶版放弃了 python 内置比较器，而改用内置的 SequenceMatcher。这个工具可以说已经基本完善，已经达到非智能工具，非 NLP 工具所能达到的极致。虽然目前还有一些小 Bug，不过应该在后续的更新中逐步修复。

正如之前所说，这个工具分两个部分。

* 不对比定制：只是简单的使用正则表达式进行文字替换。
* 对比定制：在使用正则表达式进行文字替换的基础上，跟之前的定制进行比较，保留大部分之前的定制。

## 学习之前

在了解这个工具之前，请先确保学习了 [python 与正则表达式](TODO)，同时还需要对 [ACN 文档定制](TODO)有一定的了解。

## 不对比定制

这个定制工具分为 4 个步骤。

1. 常量替换。
1. 全正则表达式替换。
1. 半正则表达式替换。
1. 更正替换。

### 常量替换

这个替换主要针对 EndPoints、链接和特有名词。规则保存在 `rules/constant.json` 文件当中，以键值对的形式出现。键是要被替换的文字，而值是用来替换的文字。

出于运行效率的考虑，常量替换是通过把所有常量规则合并成一个正则表达式来进行替换，规则的替换是没有先后顺序的，所以在制定规则的时候，要注意以下两点。

#### 1. 被替换的文字不能存在一个包含另外一个。

如果存在两个规则，一个规则的被替换文字包含于另外一个规则的被替换文字。那么这两个规则合成的正则表达式在匹配长规则的时候，就有可能匹配到短规则，于是替换出来的结果可能并不是想要的。

举例说明，看以下两个规则：

```json
{
    "www.windowsazure.com": "www.azure.cn",
    "https://www.windowsazure.com/services/virtual-network/": "https://www.azure.cn/home/features/networking/"
}
```

`https://www.windowsazure.com/services/virtual-network/` 是包含 `www.windowsazure.com` 的。使用这个两个规则合成的正则表达式为 `(www\.windowsazure\.com|https\://www\.windowsazure\.com/services/virtual-network/)`。当这个正则表达式在匹配字符串 `https://www.windowsazure.com/services/virtual-network/` 时，它有可能匹配到这个链接，也有可能只匹配到当中的域名部分。于是，替换的结果就有两种：`https://www.azure.cn/home/features/networking/`（匹配了整个链接）或者 `https://www.azure.cn/home/features/virtual-network/`（只匹配了域名）。显然第二个结果并不正确。

想要解决这个问题其实很简单，只要保留短规则。然后把替换后的长规则移到后续的几个步骤中。具体到上面的例子，可以保留 `"www.windowsazure.com": "www.azure.cn"`，然后把第二个规则变成 `"https://www.azure.cn/services/virtual-network/": "https://www.azure.cn/home/features/networking/"` 移到更正替换里。当然移到全正则表达式替换或者半正则表达式替换中也是可以的，但是出于运行效率的考虑，移到更正替换里会比较好。

#### 2. 被替换的文字在文档出现时不能有相互重叠。

跟上面的情况类似，出现被替换文字有重叠的情况也会只匹配到其中一个规则，于是乎替换出来的结果可能也并不是想要的。

例如以下的两个规则：

```json
{
    "https://azure.microsoft.com/pricing/": "https://www.azure.cn/pricing/",
    "/pricing/details/virtual-network/": "/pricing/details/networking/"
}
```

字符串 `https://azure.microsoft.com/pricing/details/virtual-network/` 都能匹配到以上两个规则，于是替换之后的文字要么变成 `https://www.azure.cn/pricing/details/virtual-network/`，要么变成 `https://azure.microsoft.com/pricing/details/networking/`。两个都不对，因为最终想要的结果是 `https://www.azure.cn/pricing/details/networking/`。

这种情况跟第一种情况相比，要更加隐秘。理论上，任何两个规则，只有一个规则的被替换文字的后半部分，与另一个规则的被替换文字的前半部分相重叠，就有可能发生这种情况。然而，这样的规则如果在文档中没有出现重叠，它们依旧是被允许的。

解决方法与之前一种情况类似。只要把其中一个规则移到另外一个替换步骤中即可。

### 全正则表达式替换

首先，以下是这一部分中规则定义的一个例子。这是我当前定义的规则里，最复杂的一个了。当然，如果能灵活运用正则表达式，也可以定义出更加复杂的规则。

```json
{
  "regex": "//azure\\.microsoft\\.com/documentation/templates(/\\w|/?.)",
  "replacements": [
    {
      "conditions": [
        {
          "parameter": 0,
          "match": "/\\w"
        }
      ],
      "replacement": "//github.com/Azure/azure-quickstart-templates/tree/master\\1"
    },
    {
      "conditions": [],
      "replacement": "//github.com/Azure/azure-quickstart-templates\\1"
    }
  ]
}
```

以下是规则中每一个变量所代表的含义。

* `regex`：正则表达式，也就是被替换文字所要匹配的正则表达式。
* `replacements`：替换的文字，是一个数组，也就是可以定义在不同情况下，替换不同的文字。
    * `conditions`：替换这个文字所要达到的条件，是一个数组，使用的是和逻辑。也就是说，需要达成所有条件才使用这个替换文字。可以是空数组，空意味着不需要达成任何额外的条件。
        * `parameter`：需要匹配的元组下标。
        * `match`：以上元组元素所要匹配的正则表达式，匹配成功则条件成立。
    * `replacement`：用来替换的文字。

根据以上的含义，来看一看上面示例可以达到的效果。

首先是需要匹配的正则表达式为 `//azure\\.microsoft\\.com/documentation/templates(/\\w|/?.)`。这里有两个可以匹配成功的字符串 1. `[templates](https://azure.microsoft.com/documentation/templates/)` 和 2. `[a template](https://azure.microsoft.com/documentation/templates/active-directory-new-domain-ha-2-dc/)`

字符串 1 匹配到的部分为 `//azure.microsoft.com/documentation/templates/)`，而字符串 2 匹配到的字符串为 `//azure.microsoft.com/documentation/templates/a`。我们来看一下替换 1 中的条件，（替换 2 的条件为空，也就是所有不符合替换 1 的都使用替换 2）。`parameter` 为 0，也就是要看匹配元组的第一个元素。在正则表达式中，只有一组圆括号，所以对应要看的字符串为这一对圆括号所匹配到的字符串。

这唯一的圆括号正则表达式为 `(/\\w|/?.)`，它所匹配的字符串为 `template` 后面的 1. `/)` 和 2. `/a`。

### 半正则表达式替换

### 更正替换