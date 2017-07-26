# application-gateway-diagnostics.md

## 特殊定制

* 2 行，删除 performance logs 相关内容，删除 `performance logs,`

* 3 行，删除 performance logs 相关内容，删除 `and performance logs`

* 26 行，删除 performance logs 相关内容，删除 `You can also find the health of the back-end pools through the performance diagnostic logs.`

* 28 行，删除 performance logs 相关内容，删除 `performance,`

* 29-30 行，删除 Metrics 相关内容，删除 `* [Metrics](#metrics): Application Gateway currently has one metric. This metric measures the throughput of the application gateway in bytes per second.`

* 32 行，删除 performance logs 相关内容，删除 `You can also find an aggregated health summary of back-end pools through the performance diagnostic logs.`

* 59-60 行，添加 Azure CLI 2 的登录说明：`[!INCLUDE [azure-cli-2-azurechinacloud-environment-parameter](../../includes/azure-cli-2-azurechinacloud-environment-parameter.md)]`

* 97 行，删除 Log Analytics 相关内容，删除 `as [Log Analytics](../log-analytics/log-analytics-azure-networking-analytics.md),`

* 100-101 行，删除 performance logs 相关内容，删除 `* **Performance log**: You can use this log to view how Application Gateway instances are performing. This log captures performance information for each instance, including total requests served, throughput in bytes, total requests served, failed request count, and healthy and unhealthy back-end instance count. A performance log is collected every 60 seconds.`

* 109-110 行，删除 Log Analytics 相关内容，删除 `* **Log Analytics**: Log Analytics is best used for general real-time monitoring of your application or looking at trends.`

* 113 行，删除 performance logs 相关内容，删除 `and performance`

* 130 行，删除 performance logs 相关内容，删除 `and performance`

* 138-139 行，删除 performance logs 相关内容，删除 `* Performance log`

* 145 行，删除 Log Analytics 相关内容，删除 `In this example, Log Analytics stores the logs. Click **Configure** under **Log Analytics** to configure your workspace. You can also use event hubs and a storage account to save the diagnostic logs.`

* 145-146 行，删除 Log Analytics 相关内容，删除 `![Starting the configuration process][2]`

* 200-201 行，删除 performance logs 相关内容，删除整个关于 performance logs 的部分

* 259 行，删除 performance logs 相关内容，删除 `performance,`

* 260-261 行，删除 Log Analytics 相关内容，删除 `Azure [Log Analytics](../log-analytics/log-analytics-azure-networking-analytics.md) can collect the counter and event log files from your Blob storage account. It includes visualizations and powerful search capabilities to analyze your logs.`

* 261 行，删除 performance logs 相关内容，删除 `and performance`

* 267-268 行，删除 Metrics 相关内容，删除整个关于 Metrics 的部分

* 269-270 行，删除 Log Analytics 相关内容，删除 `* Visualize counter and event logs by using [Log Analytics](../log-analytics/log-analytics-azure-networking-analytics.md).`