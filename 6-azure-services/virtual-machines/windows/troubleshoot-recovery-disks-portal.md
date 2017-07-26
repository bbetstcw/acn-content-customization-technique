# troubleshoot-recovery-disks-portal.md

## 特殊定制

* 127 行，`Click the **Deploy to Azure** button as follows:` => `Do not click the **Deploy to Azure** in the GitHub Repo, because that is for Global Azure. Instead, click the one below:`

* 129 行，替换 Github 里的 "Deploy to Azure" 链接，`![Deploy VM from template from Github](./media/troubleshoot-recovery-disks-portal/deploy-template-from-github.png)` => `[![Deploy VM from template from Github](./media/troubleshoot-recovery-disks-portal/deploy-template-from-github.png)](https://portal.azure.cn/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fazure%2Fazure-quickstart-templates%2Fmaster%2F201-vm-specialized-vhd-existing-vnet%2Fazuredeploy.json)`

* 131-132 行，删除新 ARM 门户发布 UI。