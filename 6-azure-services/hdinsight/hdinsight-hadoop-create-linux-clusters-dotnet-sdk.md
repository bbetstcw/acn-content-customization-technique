# hdinsight-hadoop-create-linux-clusters-dotnet-sdk.md

## 特殊定制

* 79 行，添加 BaseUri，添加 `private static Uri BaseUri = new Uri("https://management.chinacloudapi.cn/");`

* 117 行，使用 BaseUri，`new HDInsightManagementClient(authToken)` => `new HDInsightManagementClient(authToken, BaseUri)`

* 183 行，使用 BaseUri，`new ResourceManagementClient(new TokenCredentials(authToken.Token))` => `new ResourceManagementClient(BaseUri, new TokenCredentials(authToken.Token))`

* 211 行，使用 BaseUri，`new HDInsightManagementClient(authToken)` => `new HDInsightManagementClient(authToken, BaseUri)`

* 340 行，使用 BaseUri，`new HDInsightManagementClient(authToken)` => `new HDInsightManagementClient(authToken, BaseUri)`