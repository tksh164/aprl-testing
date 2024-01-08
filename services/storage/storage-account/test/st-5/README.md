# Testing for APRL ST-5

[APRL ST-5](https://azure.github.io/Azure-Proactive-Resiliency-Library/services/storage/storage-account/#st-5---enable-soft-delete-for-recovery-of-data)

## Deploy

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#view/Microsoft_Azure_CreateUIDef/CustomDeploymentBlade/uri/https%3A%2F%2Fraw.githubusercontent.com%2Ftksh164%2Faprl-testing%2Fmain%2Fservices%2Fstorage%2Fstorage-account%2Ftest%2Fst-5%2Ftemplate.json)

## Targets

| Name | Resource Type | Kind | SKU | Soft delete for blobs | Soft delete for containers | Soft delete for file shares |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| gpv2stdsdelbdicdi | Storage account | General purpose v2 | Standard LRS | Disabled | Disabled | Enabled |
| gpv2stdsdelbdicen | Storage account | General purpose v2 | Standard LRS | Disabled | Enabled | Enabled |
| gpv2stdsdelbencdi | Storage account | General purpose v2 | Standard LRS | Enabled | Disabled | Enabled |
| gpv2stdsdelbencen | Storage account | General purpose v2 | Standard LRS | Enabled | Enabled | Enabled |
| | | | | | | |
| gpv2stdsdelsharedi | Storage account | General purpose v2 | Standard LRS | Disabled | Disabled | Disabled |
| gpv2stdsdelshareen | Storage account | General purpose v2 | Standard LRS | Disabled | Disabled | Enabled |
| | | | | | | |
| bblobprmsdelbdicdi | Storage account | Block blob storage | Premium LRS | Disabled |Disabled  | n/a |
| bblobprmsdelbdicen | Storage account | Block blob storage | Premium LRS | Disabled | Enabled | n/a |
| bblobprmsdelbencdi | Storage account | Block blob storage | Premium LRS | Enabled | Disabled | n/a |
| bblobprmsdelbencen | Storage account | Block blob storage | Premium LRS | Enabled | Enabled | n/a |
| | | | | | | |
| fileprmsdelsharedi | Storage account | File storage | Premium LRS | n/a | n/a | Disabled |
| fileprmsdelshareen | Storage account | File storage | Premium LRS | n/a | n/a | Enabled |

## Expected result

### Should include

| Name | Resource Type | Kind | SKU | Soft delete for blobs | Soft delete for containers | Soft delete for file shares |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| gpv2stdsdelbdicdi | Storage account | General purpose v2 | Standard LRS | Disabled | Disabled | Enabled |
| gpv2stdsdelbdicen | Storage account | General purpose v2 | Standard LRS | Disabled | Enabled | Enabled |
| gpv2stdsdelbencdi | Storage account | General purpose v2 | Standard LRS | Enabled | Disabled | Enabled |
| | | | | | | |
| gpv2stdsdelsharedi | Storage account | General purpose v2 | Standard LRS | Disabled | Disabled | Disabled |
| gpv2stdsdelshareen | Storage account | General purpose v2 | Standard LRS | Disabled | Disabled | Enabled |
| | | | | | | |
| bblobprmsdelbdicdi | Storage account | Block blob storage | Premium LRS | Disabled |Disabled  | n/a |
| bblobprmsdelbdicen | Storage account | Block blob storage | Premium LRS | Disabled | Enabled | n/a |
| bblobprmsdelbencdi | Storage account | Block blob storage | Premium LRS | Enabled | Disabled | n/a |
| | | | | | | |
| fileprmsdelsharedi | Storage account | File storage | Premium LRS | n/a | n/a | Disabled |

### Should not be included

| Name | Resource Type | Kind | SKU | Soft delete for blobs | Soft delete for containers | Soft delete for file shares |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| gpv2stdsdelbencen | Storage account | General purpose v2 | Standard LRS | Enabled | Enabled | Enabled |
| | | | | | | |
| bblobprmsdelbencen | Storage account | Block blob storage | Premium LRS | Enabled | Enabled | n/a |
| | | | | | | |
| fileprmsdelshareen | Storage account | File storage | Premium LRS | n/a | n/a | Enabled |
