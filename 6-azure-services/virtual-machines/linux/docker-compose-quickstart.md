# docker-compose-quickstart.md

## 特殊定制

* 28-30 行，添加 ARM 模板可能需要编辑的说明。

* 35-36 行，添加 Azure CLI 2 的登录说明：`[!INCLUDE [azure-cli-2-azurechinacloud-environment-parameter](../../../includes/azure-cli-2-azurechinacloud-environment-parameter.md)]`

* 52 行，使用 `--template-file`，因为 ARM 模板需要编辑才适用于 Azure 中国。