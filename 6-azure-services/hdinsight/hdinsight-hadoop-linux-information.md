# hdinsight-hadoop-linux-information.md

## 特殊定制

* 36 行，添加 Azure CLI 2 的登录说明：`[!INCLUDE [azure-cli-2-azurechinacloud-environment-parameter](../../includes/azure-cli-2-azurechinacloud-environment-parameter.md)]`

* 39 行，删除 Domain Joined 相关内容，删除 `Unless [domain-joined](hdinsight-domain-joined-introduction.md),`

* 40, 130-139, 156-166, 192-201 行，删除 Domain Joined 相关内容。

* 100 行，删除 Data Lake Store 相关内容，`HDFS, Azure Storage, and Data Lake Store` => `HDFS and Azure Storage`

* 104 行，删除 Data Lake Store 相关内容，`either blobs in Azure Storage or Azure Data Lake Store` => `blobs in Azure Storage`

* 112 行，删除 Data Lake Store 相关内容，删除 `Azure Data Lake Store can grow dynamically to hold trillions of files, with individual files greater than a petabyte.` 和 `and [Data Lake Store](https://azure.microsoft.com/services/data-lake-store/)`

* 114 行，删除 Data Lake Store 相关内容，`either Azure Storage or Data Lake Store` => `Azure Storage`，删除 `regardless of whether it is stored on Azure Storage or Data Lake Store`