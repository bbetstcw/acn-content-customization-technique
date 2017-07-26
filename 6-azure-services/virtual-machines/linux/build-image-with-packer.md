# build-image-with-packer.md

## 特殊定制

* 29-30 行，添加 Azure CLI 2 的登录说明：`[!INCLUDE [azure-cli-2-azurechinacloud-environment-parameter](../../../includes/azure-cli-2-azurechinacloud-environment-parameter.md)]`

* 82 行，添加 cloud_environment_name 参数，添加 ```| *cloud_environment_name* | It's `AzureChinaCloud` |```

* 110 行，添加 cloud_environment_name 参数，添加 `"cloud_environment_name": "AzureChinaCloud",`

* 252 行，删除 Ansible 相关内容，删除 `Ansible,`