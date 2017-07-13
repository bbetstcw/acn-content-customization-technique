# hdinsight-hadoop-create-linux-clusters-azure-powershell.md

## 特殊定制

* 140 行，删除 R Server 相关内容，删除 `configure an R Server on HDInsight cluster type. The configuration enables an edge node, RStudio,`

* 154-64，删除 R Server 相关内容，只保留 `$config = New-AzureRmHDInsightClusterConfig -ClusterType Hadoop `