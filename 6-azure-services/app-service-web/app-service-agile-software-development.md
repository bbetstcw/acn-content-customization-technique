# app-service-agile-software-development.md

## 特殊定制

* 20 行，添加开发差异说明：`[!INCLUDE [azure-sdk-developer-differences](../../includes/azure-sdk-developer-differences.md)]`

* 71 行，删除 Visual Studio subscriber benefits 相关内容。

* 73 行，删除 "Try App Service" 相关内容。

* 78-83 行，替换连续发布说明，告诉用户连续发布只能通过 Kudu 和 Webhook 设置，而且只能对 Github 的公共 Repo 设置。

* 97 行，添加说明告诉用户如何修改官方示例，才能使其能够发布到 Azure 中国。

* 128 行，添加说明告诉用户如何修改官方示例，才能使其能够发布到 Azure 中国。

* 263 行，删除不适用链接，删除 `For a common testing-in-production scenario, see [Flighting deployment (beta testing) in Azure App Service](app-service-web-test-in-production-controlled-test-flight.md).`