# app-service-continuous-deployment.md

## 特殊定制

* 20 行，删除 TFS 和 Bitbucket 连续发布的相关内容，删除 `BitBucket,` 和 `and [Visual Studio Team Services (VSTS)](https://www.visualstudio.com/team-services/)`

* 30-49 行，替换成使用 Kudu 和 Webhook 设置连续发布的步骤。

* 81-84 行，删除 "Try App Service" 相关内容。