# remote-state/backend

> __@deprecated__ please use git repo [iac-tf-az-cloudtrain-modules](https://github.com/msgoat/iac-tf-az-cloudtrain-modules) instead!

Creates all Azure resources to manage Terraform state remotely.

All Terraform state is persisted in an Azure Storage account with the following capabilities:

* storage account type is `General Purpose v2 (GPv2)` which is the recommended default
* default encryption using AES 256 bit encryption with Microsoft-manages keys
* zone-redundant storage (ZRS) which copies data synchronously across three availability zones in the given region
* only HTTPS access is allowed with minimum TLS version 1.2

All resources allocated by this Terraform module are owned by a dedicated resource group
created by this module.

Originally developed for msg's `Cloud Training Program` and `Cloud Expert Program`.

> Still work in progress! Provided AS IS without any warranties!

## Input Variables

see [variables.tf](variables.tf)

## Output Values

see [outputs.tf](outputs.tf)

# To discuss

* Encryption could be improved with customer managed keys but adds complexity of managing an `Azure Key Vault` as well
