# cache-web-app-howto.md

## 特殊定制

* 31-32 行，添加开发差异说明：`[!INCLUDE [azure-sdk-developer-differences](../../includes/azure-sdk-developer-differences.md)]`

* 34-35 行，添加 VS 登录说明：`[!INCLUDE [azure-visual-studio-login-guide](../../includes/azure-visual-studio-login-guide.md)]`

* 55-56 行，删除 Visual Studio subscriber benefits 相关内容。

* 699-701 行，添加 ARM 模板可能需要编辑的说明。

* 711 行，替换新 ARM 模板发布的门户 UI，`![Deploy to Azure][cache-deploy-to-azure-step-1]` => `[![Deploy to Azure](media/cache-web-app-howto/deploybutton.png)](https://portal.azure.cn/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2F201-web-app-redis-cache-sql-database%2Fazuredeploy.json)`

* 714-715 行，删除新 ARM 模板发布的门户 UI。

* 715 行，替换新 ARM 模板发布的门户 UI，`scroll to the end of the page, read the terms and conditions, and check the **I agree to the terms and conditions stated above** checkbox.` => `select **Legal terms**, read the terms and conditions, and click the **Purchase** button.`

* 715 行，替换新 ARM 模板发布的门户 UI，`**Purchase**` => `**Create**`