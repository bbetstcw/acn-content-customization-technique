# hdinsight-hadoop-use-blob-storage.md

## 特殊定制

* 3 行，删除 Data Lake Store 相关内容，删除 `and Azure Data Lake Store`

* 4 行，删除 Data Lake Store 相关内容，删除 `data lake store,`

* 24 行，添加开发差异说明：`[!INCLUDE [azure-sdk-developer-differences](../../includes/azure-sdk-developer-differences.md)]`

* 25 行，删除 Data Lake Store 相关内容，`either in Azure Storage, Azure Data Lake Store, or both` => `in Azure Storage`

* 27 行，删除 Data Lake Store 相关内容，`either Azure Storage or Azure Data Lake Store as the default files system with a few exceptions` => `Azure Storage as the default files system`，删除 `For the supportability of using Data Lake Store as both the default and linked storage, see [Availabilities for HDInsight cluster](#availabilities-for-hdinsight-clusters]).`

* 29 行，删除 Data Lake Store 相关内容，删除 `To learn how Data Lake Store works with HDInsight clusters, see [Use Azure Data Lake Store with Azure HDInsight clusters](hdinsight-hadoop-use-data-lake-store.md).`

* 104 行，删除 Data Lake Store 相关内容，删除 `from Data Lake Store or`

* 300 行，删除 Data Lake Store 相关内容。