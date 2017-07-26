# app-service-continuous-deployment.md

## 特殊定制

* 22-24 行，添加开发差异说明：`[!INCLUDE [azure-sdk-developer-differences](../../includes/azure-sdk-developer-differences.md)]`

* 25 行，删除 TFS 和 Bitbucket 连续发布的相关内容，删除 `BitBucket,` 和 `and [Visual Studio Team Services (VSTS)](https://www.visualstudio.com/team-services/)`

* 34-52 行，替换成使用 Kudu 和 Webhook 设置连续发布的步骤。

* 57-59 行，添加 VS 登录说明：`[!INCLUDE [azure-visual-studio-login-guide](../../includes/azure-visual-studio-login-guide.md)]`

* 86-87 行，删除 "Try App Service" 相关内容。