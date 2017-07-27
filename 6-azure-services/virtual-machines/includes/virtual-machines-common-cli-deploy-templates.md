# virtual-machines-common-cli-deploy-templates.md

## 特殊定制

* 33 行，删除 Visual Studio Subscriber benefit 相关内容，删除 `but you do have an MSDN subscription, you can activate your [MSDN subscriber benefits](https://azure.microsoft.com/pricing/member-offers/msdn-benefits-details/). Or`

* 114-115, 121-122 行，删除不适用的镜像。

* 126-206 行，替换命名，`coreo-westu` => `coreo-china`

* 444-480, 702-752, 762-765, 1117-1160 行，使用 `--template-file` 代替 `--template-uri`，因为这个模板需要编辑才适用于 Azure 中国。

* 488-490 行，添加 ARM 模板可能需要编辑的说明。