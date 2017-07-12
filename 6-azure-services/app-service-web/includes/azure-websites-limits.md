# azure-websites-limits.md

## 特殊定制

* 4 行，删除 Logic App 相关内容。

* 7 行，删除应用服务环境的相关内容，删除 `(50 in ASE)`

* 8 行，替换应用服务环境的相关内容，`500 GB<sup>4,5</sup>` => `250 GB<sup>4,5</sup>`

* 21 行，替换应用服务环境的相关内容，`Once every 5 minutes<sup>8</sup>` => `50 times per day<sup>8</sup>`

* 33, 38 行，添加 Azure 中国不支持应用服务环境的说明，添加 `However, Azure China currently does not support App Service Environment yet.`

* 35 行，删除应用服务环境的相关内容，删除 `More storage options are available in [App Service Environment](../articles/app-service-web/app-service-web-configure-an-app-service-environment.md#storage)`