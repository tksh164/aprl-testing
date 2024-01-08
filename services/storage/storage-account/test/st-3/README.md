# Testing for APRL ST-3

[APRL ST-3](https://azure.github.io/Azure-Proactive-Resiliency-Library/services/storage/storage-account/#st-3---ensure-performance-tier-is-set-as-per-workload)

## Deploy

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#view/Microsoft_Azure_CreateUIDef/CustomDeploymentBlade/uri/https%3A%2F%2Fraw.githubusercontent.com%2Ftksh164%2Faprl-testing%2Fmain%2Fservices%2Fstorage%2Fstorage-account%2Ftest%2Fst-3%2Ftemplate.json)

## Targets

| Name | Resource Type | Kind | SKU |
| ---- | ---- | ---- | ---- |
| gpv2stdlrs | Storage account | General purpose v2 | Standard LRS |
| gpv2stdgrs | Storage account | General purpose v2 | Standard GRS |
| gpv2stdragrs | Storage account | General purpose v2 | Standard RA-GRS |
| gpv2stdzrs | Storage account | General purpose v2 | Standard ZRS |
| gpv2stdgzrs | Storage account | General purpose v2 | Standard GZRS |
| gpv2stdragzrs | Storage account | General purpose v2 | Standard RA-GZRS |
| gpv2prmlrs | Storage account | General purpose v2 | Premium LRS |
| gpv2prmzrs | Storage account | General purpose v2 | Premium ZRS |
| | | | | | | |
| gpv1stdlrs | Storage account | General purpose v1 | Standard LRS |
| gpv1stdgrs | Storage account | General purpose v1 | Standard GRS |
| gpv1stdragrs | Storage account | General purpose v1 | Standard RA-GRS |
| gpv1stdzrs | Storage account | General purpose v1 | Standard ZRS |
| gpv1prmlrs | Storage account | General purpose v1 | Premium LRS |
| | | | | | | |
| blobstdlrs | Storage account | Blob storage | Standard LRS |
| blobstdgrs | Storage account | Blob storage | Standard GRS |
| blobstdragrs | Storage account | Blob storage | Standard RA-GRS |
| | | | | | | |
| blockblobprmlrs | Storage account | Block blob storage | Premium LRS |
| blockblobprmzrs | Storage account | Block blob storage | Premium ZRS |
| | | | | | | |
| fileprmlrs | Storage account | File storage | Premium LRS |
| fileprmzrs | Storage account | File storage | Premium ZRS |

## Expected result

### Should include

General purpose v1 and Blob storage are upgradeable to General purpose v2.

| Name | Resource Type | Kind | SKU |
| ---- | ---- | ---- | ---- |
| gpv1stdlrs | Storage account | General purpose v1 | Standard LRS |
| gpv1stdgrs | Storage account | General purpose v1 | Standard GRS |
| gpv1stdragrs | Storage account | General purpose v1 | Standard RA-GRS |
| gpv1stdzrs | Storage account | General purpose v1 | Standard ZRS |
| gpv1prmlrs | Storage account | General purpose v1 | Premium LRS |
| | | | | | | |
| blobstdlrs | Storage account | Blob storage | Standard LRS |
| blobstdgrs | Storage account | Blob storage | Standard GRS |
| blobstdragrs | Storage account | Blob storage | Standard RA-GRS |

### Should not be included

| Name | Resource Type | Kind | SKU |
| ---- | ---- | ---- | ---- |
| gpv2stdlrs | Storage account | General purpose v2 | Standard LRS |
| gpv2stdgrs | Storage account | General purpose v2 | Standard GRS |
| gpv2stdragrs | Storage account | General purpose v2 | Standard RA-GRS |
| gpv2stdzrs | Storage account | General purpose v2 | Standard ZRS |
| gpv2stdgzrs | Storage account | General purpose v2 | Standard GZRS |
| gpv2stdragzrs | Storage account | General purpose v2 | Standard RA-GZRS |
| gpv2prmlrs | Storage account | General purpose v2 | Premium LRS |
| gpv2prmzrs | Storage account | General purpose v2 | Premium ZRS |
| | | | | | | |
| blockblobprmlrs | Storage account | Block blob storage | Premium LRS |
| blockblobprmzrs | Storage account | Block blob storage | Premium ZRS |
| | | | | | | |
| fileprmlrs | Storage account | File storage | Premium LRS |
| fileprmzrs | Storage account | File storage | Premium ZRS |
