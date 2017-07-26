# app-service-web-arm-with-sql-database-provision.md

## 特殊定制

* 22-24 行，添加开发差异说明：`[!INCLUDE [azure-sdk-developer-differences](../../includes/azure-sdk-developer-differences.md)]`

* 43-44, 433-434 行，删除 Application Insights 相关内容。

* 48-50 行，添加 ARM 模板可能需要编辑的说明。

* 438 行，由于该模板确实需要编辑才能在 Azure 中国使用，所以不能直接使用 URI 发布，`-TemplateUri https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/201-web-app-sql-database/azuredeploy.json` => `-TemplateFile path/to/azuredeploy.json`

* 443, 449 行，由于该模板确实需要编辑才能在 Azure 中国使用，所以不能直接使用 URI 发布，`--template-uri https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/201-web-app-sql-database/azuredeploy.json` => `--template-uri path/to/azuredeploy.json`

* 447-448 行，添加 Azure CLI 2 的登录说明：`[!INCLUDE [azure-cli-2-azurechinacloud-environment-parameter](../../includes/azure-cli-2-azurechinacloud-environment-parameter.md)]`