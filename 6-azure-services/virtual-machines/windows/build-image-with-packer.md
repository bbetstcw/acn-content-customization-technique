# build-image-with-packer.md

## 特殊定制

* 79 行，添加 cloud_environment_name 参数，添加 ```| *cloud_environment_name* | It's `AzureChinaCloud` |```

* 114 行，添加 cloud_environment_name 参数，添加 `"cloud_environment_name": "AzureChinaCloud",`

* 320 行，删除 Ansible 相关内容，删除 `Ansible,`