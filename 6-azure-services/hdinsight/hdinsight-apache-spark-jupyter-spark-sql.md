# hdinsight-apache-spark-jupyter-spark-sql.md

## 特殊定制

* 40 行，添加 ARM 模板可能需要编辑的说明。

* 43 行，删除新版 ARM 模板部署 UI 的截图。

* 55 行，滚回 ARM 模板部署 UI，`Select **I agree to the terms and conditions stated above**, select **Pin to dashboard**, and then click **Purchase**.` => `Select **Pin to dashboard**; in **Legal terms**, click **Purchase**; and then, click **Create**.`

* 58 行，删除 Data Lake Store 相关内容，删除 `You can also create a Spark cluster that uses [Azure Data Lake Store](../data-lake-store/data-lake-store-overview.md) as additional storage, in addition to Azure Storage Blobs as the default storage. For instructions, see [Create an HDInsight cluster with Data Lake Store](../data-lake-store/data-lake-store-hdinsight-hadoop-use-portal.md).`

* 166 行，删除 Application Insights 相关内容。