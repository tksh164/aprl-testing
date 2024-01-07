# Testing for APRL ST-3

[APRL ST-3](https://azure.github.io/Azure-Proactive-Resiliency-Library/services/storage/storage-account/#st-3---ensure-performance-tier-is-set-as-per-workload)

## Deploy

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#view/Microsoft_Azure_CreateUIDef/CustomDeploymentBlade/uri/https%3A%2F%2Fraw.githubusercontent.com%2Ftksh164%2Faprl-testing%2Fmain%2Fservices%2Fstorage%2Fstorage-account%2Ftest%2Fst-3%2Ftemplate.json)

## Targets

- Storage account: General purpose v2 - Standard LRS
- Storage account: General purpose v2 - Standard GRS
- Storage account: General purpose v2 - Standard RA-GRS
- Storage account: General purpose v2 - Standard ZRS
- Storage account: General purpose v2 - Standard GZRS
- Storage account: General purpose v2 - Standard RA-GZRS
- Storage account: General purpose v2 - Premium LRS
- Storage account: General purpose v2 - Premium ZRS
- Storage account: General purpose v1 - Standard LRS
- Storage account: General purpose v1 - Standard GRS
- Storage account: General purpose v1 - Standard RA-GRS
- Storage account: General purpose v1 - Standard ZRS
- Storage account: General purpose v1 - Premium LRS
- Storage account: Blob storage - Standard LRS
- Storage account: Blob storage - Standard GRS
- Storage account: Blob storage - Standard RA-GRS
- Storage account: Block blob storage - Premium LRS
- Storage account: Block blob storage - Premium ZRS
- Storage account: File storage - Premium LRS
- Storage account: File storage - Premium ZRS

## Expected result

- Should include

    - Storage account: General purpose v1 - Standard LRS
    - Storage account: General purpose v1 - Standard GRS
    - Storage account: General purpose v1 - Standard RA-GRS
    - Storage account: General purpose v1 - Standard ZRS
    - Storage account: General purpose v1 - Premium LRS
    - Storage account: Blob storage - Standard LRS
    - Storage account: Blob storage - Standard GRS
    - Storage account: Blob storage - Standard RA-GRS

- Should not be included

    - Storage account: General purpose v2 - Standard LRS
    - Storage account: General purpose v2 - Standard GRS
    - Storage account: General purpose v2 - Standard RA-GRS
    - Storage account: General purpose v2 - Standard ZRS
    - Storage account: General purpose v2 - Standard GZRS
    - Storage account: General purpose v2 - Standard RA-GZRS
    - Storage account: General purpose v2 - Premium LRS
    - Storage account: Block blob storage - Premium LRS
    - Storage account: Block blob storage - Premium ZRS
    - Storage account: File storage - Premium LRS
    - Storage account: File storage - Premium ZRS
