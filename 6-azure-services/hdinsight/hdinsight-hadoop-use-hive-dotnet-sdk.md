# hdinsight-hadoop-use-hive-dotnet-sdk.md

## 特殊定制

* 69 行，添加 StorageAccountSuffix，添加 `private const string StorageAccountSuffix = "core.chinacloudapi.cn";`

* 115 行，使用 StorageAccountSuffix，`new AzureStorageAccess(DefaultStorageAccountName, DefaultStorageAccountKey, DefaultStorageContainerName)` => `new AzureStorageAccess(DefaultStorageAccountName, DefaultStorageAccountKey, DefaultStorageContainerName, StorageAccountSuffix)`