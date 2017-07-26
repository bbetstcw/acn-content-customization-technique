# websites-dotnet-webjobs-sdk-service-bus.md

## 特殊定制

* 22-24 行，添加开发差异说明：`[!INCLUDE [azure-sdk-developer-differences](../../includes/azure-sdk-developer-differences.md)]`

* 53, 54 行，给 Azure Storage 的连接字符串添加 EndpointSuffix，`connectionString="DefaultEndpointsProtocol=https;AccountName=[accountname];AccountKey=[accesskey]"` => `connectionString="DefaultEndpointsProtocol=https;AccountName=[accountname];AccountKey=[accesskey];EndpointSuffix=core.chinacloudapi.cn"`