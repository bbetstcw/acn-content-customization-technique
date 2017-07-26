# encrypt-disks.md

## 特殊定制

* 27-28 行，添加 Azure CLI 2 的登录说明：`[!INCLUDE [azure-cli-2-azurechinacloud-environment-parameter](../../../includes/azure-cli-2-azurechinacloud-environment-parameter.md)]`

* 72, 206 行，替换 CentOS 7.2n 镜像，这个镜像在 Azure 中国不可用，`**CentOS 7.2n**` => `**Ubuntu 14.04**`

* 78, 212 行，替换 CentOS 7.2n 镜像，这个镜像在 Azure 中国不可用，`OpenLogic:CentOS:7.2n:7.2.20160629` => `Canonical:UbuntuServer:14.04.3-LTS:latest`

* 146 行，删除 G 和 GS 系列的相关内容，`A, D, DS, G, and GS series` => `A, D, and DS series`