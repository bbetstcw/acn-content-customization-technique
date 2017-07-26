# dockerextension-nodejs.md

## 特殊定制

* 24 行，删除 Azure Container 相关内容，删除 `and Azure Container Services`

* 27-28, 201-end 行，删除 Azure Container 相关内容。

* 43-45 行，添加 ARM 模板可能需要编辑的说明。

* 58 行，使用 `--template-file` 代替 `--template-uri`，因为这个模板确实需要编辑过，才适用于 Azure 中国。