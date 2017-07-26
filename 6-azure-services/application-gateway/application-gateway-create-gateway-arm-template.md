# application-gateway-create-gateway-arm-template.md

## 特殊定制

* 82 行，替换了一个不适用链接：`[Resource Manager templates reference](/templates/)` => `[Resource Manager templates reference](https://github.com/Azure/azure-quickstart-templates/)`

* 168-169 行，添加 Azure CLI 2 的登录说明：`[!INCLUDE [azure-cli-2-azurechinacloud-environment-parameter](../../includes/azure-cli-2-azurechinacloud-environment-parameter.md)]`

* 199 行，纠正 **Deploy to Azure** 发布模板模式：`![Deploy to Azure](./media/application-gateway-create-gateway-arm-template/deploytoazure.png)` => `[![Deploy to Azure](./media/application-gateway-create-gateway-arm-template/deploytoazure.png)](https://portal.azure.cn/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2F101-application-gateway-public-ip%2Fazuredeploy.json)`

* 图片：application-gateway-create-gateway-arm-template/deploytoazure.png 和 application-gateway-create-gateway-arm-template/ibiza1.png 保留旧版本。

    理由：deploytoazure.png 目前的最新版本是 Github 上 **Deploy to Azure** 的截图，然而 Github 上的发布链接是 Azure 国际版的，所以不能使用这个截图。而 ibiza1.png，Azure 中国目前的门户依旧使用旧版的发布模板 UI，所以需要保留旧版的截图。

* 205 行，滚回旧版发布模板 UI，`Select **I agree to the terms and conditions stated above** and click **Purchase**.` => `Click **Legal terms**, and then click **Create**.`