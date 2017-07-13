# hdinsight-hadoop-create-linux-clusters-dotnet-sdk.md

## 特殊定制

* 78 行，添加 BaseUri，添加 `private static Uri BaseUri = new Uri("https://management.chinacloudapi.cn/");`

* 115 行，使用 BaseUri，`new HDInsightManagementClient(authToken)` => `new HDInsightManagementClient(authToken, BaseUri)`

* 182 行，使用 BaseUri，`new ResourceManagementClient(new TokenCredentials(authToken.Token))` => `new ResourceManagementClient(BaseUri, new TokenCredentials(authToken.Token))`

* 209 行，使用 BaseUri，`new HDInsightManagementClient(authToken)` => `new HDInsightManagementClient(authToken, BaseUri)`

* 338 行，使用 BaseUri，`new HDInsightManagementClient(authToken)` => `new HDInsightManagementClient(authToken, BaseUri)`