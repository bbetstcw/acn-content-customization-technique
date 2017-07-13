# hdinsight-hadoop-install-presto.md

## 特殊定制

* 45 行，删除 Data Lake Store 相关内容，删除 `Using Presto on a cluster that uses Azure Data Lake Store as the storage option is not yet supported.`

* 116-118 行，删除新版 ARM 模板部署 UI 的截图，删除 `as shown in the following screenshot` 和 `![HDInsight install Airpal on Presto cluster](./media/hdinsight-hadoop-install-presto/hdinsight-install-airpal.png)`

* 120 行，滚回 ARM 模板部署 UI，`Click **Purchase**.` => `Review the **Legal Terms**, and clickt the **Purchase** button for both the Legal terms and template.`