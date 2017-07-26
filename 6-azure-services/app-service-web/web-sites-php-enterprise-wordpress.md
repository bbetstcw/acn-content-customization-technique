# web-sites-php-enterprise-wordpress.md

## 特殊定制

* 27 行，替换 ClearDB 相关内容，`This requirement is available through [ClearDB in the Azure Marketplace][cdbnstore].` => `You can use **MySQL Database on Azure**.`

* 28-29 行，删除 ClearDB 相关内容。

* 46 行，替换 ClearDB 相关内容，`using CDBR High Availability router to route to MySQL across regions` => `using MySQL Cluster CGE`

* 50 行，删除 ClearDB 相关内容，删除 `[ClearDB high-availability routers (CDBRs)][cleardbscale] (shown left) or`

* 52-54 行，添加关于在 Multi-region deployment 必须使用 IaaS 虚拟机的说明。

* 56 行，删除应用市场模板的相关内容，删除 `[Memcache Cloud](http://azure.microsoft.com/gallery/store/garantiadata/memcached/), [MemCachier](http://azure.microsoft.com/gallery/store/memcachier/memcachier/), or one of the other caching offerings in the [Azure Store](http://azure.microsoft.com/gallery/store/)`

* 58 行，替换 ClearDB 相关内容，`using CDBR High Availability router for MySQL` => `using MySQL Cluster CGE`

* 67 行，删除 SendGrid 相关内容，删除 `[SendGrid][storesendgrid] and the`

* 86 行，删除应用市场模板的相关内容，删除 `[Memcache Cloud](/gallery/store/garantiadata/memcached/), [MemCachier](/gallery/store/memcachier/memcachier/), or one of the other caching offerings in the [Azure Store](/gallery/store/)`

* 87 行，删除 ClearDB 相关内容，删除 `[ClearDB High Availability Routing][cleardbscale]. If you choose to host and manage your own MySQL installation, you should consider` 和 `for scale-out.`

* 102-104 行，替换应用市场模板的相关内容，替换成手动本地配置。

* 139 行，替换应用市场模板的相关内容，`Purchase a new database from the [Azure Marketplace][cdbnstore]` => `Create a database in "MySQL Database on Azure"`

* 144 行，替换应用市场模板的相关内容，`**Web + Mobile** > **Azure Marketplace** > **Web Apps** > **Web app + SQL** (or **Web app + MySQL**) > **Create**` => `**Web + Mobile** > **Web Apps** > **Create**`

* 162 行，删除应用市场模板的相关内容，删除 `or you can use one of the other caching offerings from the <a href="/gallery/store/">Azure Store</a>`

* 163 行，替换 Azure CDN 链接，`[Use the Content Distribution Network](../cdn/cdn-create-new-endpoint.md)` => `[Use the Content Distribution Network][cdn]`

* 164 行，删除应用市场模板的相关内容，删除 `Enable <a href="https://azure.microsoft.com/marketplace/partners/sendgrid/sendgrid-azure/">SendGrid</a> by using the Azure Store.`

* 173-174 行，删除 ClearDB 相关内容。

* 177-178, 179-180 行，删除不适用链接。

* 182-183 行，删除 "Try App Service" 相关内容。