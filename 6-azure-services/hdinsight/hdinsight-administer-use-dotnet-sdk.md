# hdinsight-administer-use-dotnet-sdk.md

## 特殊定制

* 26-27 行，添加开发差异说明：`[!INCLUDE [azure-sdk-developer-differences](../../includes/azure-sdk-developer-differences.md)]`

* 65 行，添加 BaseUri，添加 `private static Uri BaseUri = new Uri("https://management.chinacloudapi.cn/");`

* 74 行，使用 BaseUri，`new HDInsightManagementClient(authToken);` => `new HDInsightManagementClient(authToken, BaseUri);`

* 104 行，使用 BaseUri，`new ResourceManagementClient(new TokenCredentials(authToken.Token))` => `new ResourceManagementClient(BaseUri, new TokenCredentials(authToken.Token))`