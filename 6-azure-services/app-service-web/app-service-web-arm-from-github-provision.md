# app-service-web-arm-from-github-provision.md

## 特殊定制

* 22-24 行，添加开发差异说明：`[!INCLUDE [azure-sdk-developer-differences](../../includes/azure-sdk-developer-differences.md)]`

* 40-42 行，添加 ARM 模板可能需要编辑的说明。

* 106-108 行，添加 `IsManualIntegration` 必须为真的说明。

* 121-122 行，添加 Azure CLI 2 的登录说明：`[!INCLUDE [azure-cli-2-azurechinacloud-environment-parameter](../../includes/azure-cli-2-azurechinacloud-environment-parameter.md)]`