# AutoRest Configuration for Storage

> see https://aka.ms/autorest

``` yaml
require: 
  - $(this-folder)/../readme.azure.md
  - $(repo)/specification/storage/resource-manager/readme.enable-multi-api.md
  - $(repo)/specification/storage/resource-manager/readme.md

subject-prefix: ''
title: StorageManagementClient
module-version: 0.0.1
skip-model-cmdlets: true
profile: 
  - hybrid-2019
```