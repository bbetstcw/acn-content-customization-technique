# cli-ps-findimage.md

## 特殊定制

* 28-29 行，添加 Azure CLI 2 的登录说明：`[!INCLUDE [azure-cli-2-azurechinacloud-environment-parameter](../../../includes/azure-cli-2-azurechinacloud-environment-parameter.md)]`

* 48-49 行，删除 RHEL 镜像，这个镜像通过命令行是可以搜出来的，但是不能使用它，所以我删掉了，避免误会。