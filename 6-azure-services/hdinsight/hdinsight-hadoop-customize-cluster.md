# hdinsight-hadoop-customize-cluster.md

## 特殊定制

* 220 行，添加 BaseUri，添加 `private static Uri BaseUri = new Uri("https://management.chinacloudapi.cn/");`

* 243 行，使用 BaseUri，`new HDInsightManagementClient(authToken)` => `new HDInsightManagementClient(authToken, BaseUri)`

* 297 行，使用 BaseUri，`new ResourceManagementClient(new TokenCredentials(authToken.Token))` => `new ResourceManagementClient(BaseUri, new TokenCredentials(authToken.Token))`