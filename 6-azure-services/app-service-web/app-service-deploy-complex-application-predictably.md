# app-service-deploy-complex-application-predictably.md

## 特殊定制

* 22-24 行，添加开发差异说明：`[!INCLUDE [azure-sdk-developer-differences](../../includes/azure-sdk-developer-differences.md)]`

* 27 行，删除 Logic App 相关内容，删除 `and logic apps`

* 37 行，删除 Application Insights 相关内容，删除 `Application insights,`

* 43 行，删除应用市场模板的相关内容，删除 `A complex template from the [Azure Marketplace](/marketplace) like the [Scalable WordPress](/marketplace/partners/wordpress/scalablewordpress/) app can include the MySQL database, storage accounts, the App Service plan, the web app itself, alert rules, app settings, autoscale settings, and more, and all these templates are available to you through PowerShell.`

* 48-50 行，添加 VS 登录说明：`[!INCLUDE [azure-visual-studio-login-guide](../../includes/azure-visual-studio-login-guide.md)]`

* 59-60, 171-172 行，删除 Resource Explorer 相关内容。

* 66-67 行，替换发布 ToDoApp 的步骤。

* 169 行，`You can use the default value `false` for the specified repository only if you have configured the owner’s GitHub credentials in the [Azure portal](https://portal.azure.com/) before. In other words, if you have set up source control to GitHub or BitBucket for any app in the [Azure Portal](https://portal.azure.com/) previously, using your user credentials, then Azure will remember the credentials and use them whenever you deploy any app from GitHub or BitBucket in the future. However, if you haven’t done this already, deployment of the JSON template will fail when Azure Resource Manager tries to configure the web app’s source control settings because it cannot log into GitHub or BitBucket with the repository owner’s credentials.` => `Even if you own the GitHub Repo, in Azure China, setting up GitHub Credential is not supported yet.`

* 224 行，删除 Resource Explorer 相关内容，删除 `and the [Azure Resource Explorer](https://resources.azure.com) tool`

* 242 行，删除不适用链接，删除 `and advanced deployment techniques like [flighting deployment](app-service-web-test-in-production-controlled-test-flight.md) easily`