# web-sites-php-mysql-deploy-use-ftp.md

## 特殊定制

* 22-24 行，添加开发差异说明：`[!INCLUDE [azure-sdk-developer-differences](../../includes/azure-sdk-developer-differences.md)]`

* 35-36 行，删除 "Try App Service" 相关内容。

* 43-45 行，替换应用市场模板的相关内容，**Web app + MySQL** 在 Azure 中国的应用市场里是没有的，所以 MySQL 只能手动创建。

* 195-199 行，替换获取 MySQL 连接信息的方法，由于 MySQL 是手动创建的，相应的连接信息获取方法也需要改变。