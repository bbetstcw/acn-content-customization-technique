# app-service-web-tutorial-hyper-scale-app.md

## 特殊定制

* 65-67 行，添加 Azure CLI 2 的登录说明：`[!INCLUDE [azure-cli-2-azurechinacloud-environment-parameter](../../includes/azure-cli-2-azurechinacloud-environment-parameter.md)]`

* 226, 243, 250, 359 行，`Europe` => `China North`

* 254 行，`myWestEuropeEndpoint` => `myChinaNorthEndpoint`

* 266, 267, 277, 282, 296, 326, 333, 340 行，`Asia` => `China East`

* 270, 273 行，`$cacheName-asia` => `$cacheName-east`

* 279, 286 行，`myAppServicePlanAsia` => `myAppServicePlanEast`

* 286, 289, 294, 300, 330, 337, 352 行，`$appName-asia` => `$appName-east`

* 307, 314 行，`myuniqueappname-asia` => `myuniqueappname-east`

* 314, 321 行，`azure-asia` => `azure-east`

* 337, 344 行，`$appIdAsia` => `$appIdEast`

* 344 行，`myAsiaEndpoint` => `myEastEndpoint`