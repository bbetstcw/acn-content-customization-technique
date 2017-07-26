# hdinsight-hadoop-development-using-azure-resource-manager.md

## 特殊定制

* 148-149 行，删除 Data Lake Store 相关内容。

* 163, 179 行，`-Version "3.2"` => `-Version "3.5"`

* 273, 290 行，添加 BaseUri，`new HDInsightManagementClient(creds)` => `new HDInsightManagementClient(creds, new Uri("https://management.chinacloudapi.cn/"))`