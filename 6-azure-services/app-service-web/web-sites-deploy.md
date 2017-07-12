# web-sites-deploy.md

## 特殊定制

* 30 行，删除 Cloud Sync 相关内容，删除 `or OneDrive/Dropbox`，`3 different types` => `2 different types`

* 32, 65-82 行，删除 Cloud Sync 相关内容。

* 33 行，删除 TFTS 和 Bitbucket 连续发布的相关内容，删除 `Bitbucket, and Visual Studio Team Services`

* 85 行，删除 TFTS 和 Bitbucket 连续发布的相关内容，删除 `[Visual Studio Team Services](http://www.visualstudio.com/),` 和 `or [BitBucket](https://bitbucket.org/),`

* 99 行，删除 TFTS 和 Bitbucket 连续发布的相关内容，删除 `Bitbucket, and Visual Studio Team Services`, `[Azure Portal](https://portal.azure.cn)` => `Kudu`（连续发布只能通过 Kudu 和 Webhook 设置）

* 154 行，添加 VS 登录说明：`[!INCLUDE [azure-visual-studio-login-guide](../../includes/azure-visual-studio-login-guide.md)]`