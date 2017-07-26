# hdinsight-create-non-interactive-authentication-dotnet-applications.md

## 特殊定制

* 77 行，添加 BaseUri，添加 `private static Uri BaseUri = new Uri("https://management.chinacloudapi.cn/");`

* 87 行，使用 BaseUri，`new ResourceManagementClient(subCloudCredentials)` => `new ResourceManagementClient(BaseUri, subCloudCredentials)`

* 90 行，使用 BaseUri，`new HDInsightManagementClient(subCloudCredentials)` => `new HDInsightManagementClient(subCloudCredentials, BaseUri)`