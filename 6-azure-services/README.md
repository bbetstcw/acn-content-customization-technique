# 常见的定制

* 如果文档提到 Azure CLI 2.0，请添加 CLI 2.0 的说明，例如 `[!INCLUDE [azure-cli-2-azurechinacloud-environment-parameter](../../includes/azure-cli-2-azurechinacloud-environment-parameter.md)]`，请注意 includes 文件的相对路径，不然发布会出错。

* 如果文档提到在 GitHub 使用 "Click to deploy" 或者 "Deploy to Azure"，请改成在使用命令行发布，或者提供一个发布到 Azure 中国的链接。如果文档是以命令行发布，但是使用了 `-TemplateURI`（PowerShell）或者 `--template-uri`（CLI），而你又确定那个模板不太适用于 Azure 中国，那么就改成使用 `-TemplateFile` 和 `--template-file`。另外还要说明 ARM 模板可能需要编辑一下才能适用于 Azure 中国。

* 目前在 Azure 中国，门户发布 ARM 模板的 UI 是旧的，所以如果看到新版 UI，请改成旧的 UI。

* 删除一些国际版 Azure 区域的内容，Azure 中国只有两个区域，所以任何涉及到 3 个或者 3 个以上区域的内容都是不合适的。

* 有一些服务会涉及到很多其他服务，但是它们不一定在 Azure 中国上线，例如，Security Center, Log Analytics, Application insights, Azure Container Services, Cloud Shell, Biztalk Services, Azure Notebook, Azure Data Factory, Azure Data Lake Store 等，这些内容都得删掉。

* index 中，国际版 Azure 的视频都得删掉，还有 Reference 部分也要删掉。

* Stack Overflow 的链接最好都删掉，还有一些国际版的链接，能找到替换的尽量替换掉。

* Google, Facebook, Twitter 的内容最好都删掉。

* MSDN or Visual Studio Subscriber benefit 的内容都要删掉。

* 有些内涉及到跨国公司，或者说到“全球”，这些内容都是不合适的，应该改成“全国”。

* 国际版应用市场的链接都是不适用的，如果能找到 Azure 门户里对应的链接，可以替换掉，如果找不到，就删掉吧。

* 跟开发相关的文档最好是添加开发差异说明，例如 `[!INCLUDE [azure-sdk-developer-differences](../../includes/azure-sdk-developer-differences.md)]`，请注意 includes 文件的相对路径，不然发布会出错。

* 跟 Visual Studio 相关的文档最好添加 Visual Studio 登录说明，例如 `[!INCLUDE [azure-visual-studio-login-guide](../../includes/azure-visual-studio-login-guide.md)]`，请注意 includes 文件的相对路径，不然发布会出错。

* 跟 Azure Tools 相关的文档最好添加 Azure Tools 登录说明，例如 `[!INCLUDE [azure-eclipse-login-guide](../../includes/azure-eclipse-login-guide.md)]` 或者 `[!INCLUDE [azure-intellij-login-guide](../../includes/azure-intellij-login-guide.md)]`，请注意 includes 文件的相对路径，不然发布会出错。

* Resource Explorer 在 Azure 中国不适用，所以应该删掉这些内容，如果真的不想删，可以用 REST API 替换对应的内容。

* YouTube 的视频都应该删掉。

* Azure Storage 的连接字符串添加 EndpointSuffix，`EndpointSuffix=core.chinacloudapi.cn`

* 涉及到 MySQL 和 CDN 的文档都要小心，如果能找到替换方案，就替换掉；如果不能用，就删掉相关内容。

* 关于 User Voice 的内容都删掉。

* Azure .NET SDK 里，很多 Client 需要用到 BaseURI：`private static Uri BaseUri = new Uri("https://management.chinacloudapi.cn/");`。例如，HDInsight 里，`new HDInsightManagementClient(authToken, BaseUri);`，Resource Manager 里，`new ResourceManagementClient(BaseUri, new TokenCredentials(authToken.Token))`

* 一些 Feature Request, Support Request 的链接都要替换成 Azure 中国的支持链接。