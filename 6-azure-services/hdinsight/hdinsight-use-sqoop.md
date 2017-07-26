# hdinsight-use-sqoop.md

## 特殊定制

* 26-27 行，添加开发差异说明：`[!INCLUDE [azure-sdk-developer-differences](../../includes/azure-sdk-developer-differences.md)]`

* 89-91 行，添加 ARM 模板可能需要编辑的说明。

* 458 行，给 Storage 的连接字符串添加 EndpointSuffix，`DefaultEndpointsProtocol=https;AccountName=$defaultStorageAccountName;AccountKey=$defaultStorageAccountKey` => `DefaultEndpointsProtocol=https;AccountName=$defaultStorageAccountName;AccountKey=$defaultStorageAccountKey;EndpointSuffix=core.chinacloudapi.cn`