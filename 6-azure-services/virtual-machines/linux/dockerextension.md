# dockerextension.md

## 特殊定制

* 27 行，删除 Azure Container 相关内容，删除 `and Azure Container Services`

* 29-30, 147-end 行，删除 Azure Container 相关内容。

* 33-35 行，添加 ARM 模板可能需要编辑的说明。

* 36-37 行，添加 Azure CLI 2 的登录说明：`[!INCLUDE [azure-cli-2-azurechinacloud-environment-parameter](../../../includes/azure-cli-2-azurechinacloud-environment-parameter.md)]`

* 53 行，使用 `--template-file` 代替 `--template-uri`，因为这个模板确实需要编辑过，才适用于 Azure 中国。