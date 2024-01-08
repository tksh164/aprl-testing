# Testing for APRL ST-5

[APRL ST-5](https://azure.github.io/Azure-Proactive-Resiliency-Library/services/storage/storage-account/#st-5---enable-soft-delete-for-recovery-of-data)

## Deploy

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#view/Microsoft_Azure_CreateUIDef/CustomDeploymentBlade/uri/https%3A%2F%2Fraw.githubusercontent.com%2Ftksh164%2Faprl-testing%2Fmain%2Fservices%2Fstorage%2Fstorage-account%2Ftest%2Fst-5%2Ftemplate.json)

## Targets

- Soft delete for blobs
    - **gpv2stdsdelbloben**: Storage account - General purpose v2, Standard LRS, Soft delete for blobs ENABLED
    - **gpv2stdsdelblobdi**: Storage account - General purpose v2, Standard LRS, Soft delete for blobs DISABLED
    - **bblobprmsdelbloben**: Storage account - Block blob storage, Premium LRS, Soft delete for blobs ENABLED
    - **bblobprmsdelblobdi**: Storage account - Block blob storage, Premium LRS, Soft delete for blobs DISABLED

- Soft delete for containers
    - **gpv2stdsdelconen**: Storage account - General purpose v2, Standard LRS, Soft delete for containers ENABLED
    - **gpv2stdsdelcondi**: Storage account - General purpose v2, Standard LRS, Soft delete for containers DISABLED
    - **bblobprmsdelconen**: Storage account - Block blob storage, Premium LRS, Soft delete for containers ENABLED
    - **bblobprmsdelcondi**: Storage account - Block blob storage, Premium LRS, Soft delete for containers DISABLED

- Soft delete for file shares
    - **gpv2stdsdelshareen**: Storage account - General purpose v2, Standard LRS, Soft delete for file shares ENABLED
    - **gpv2stdsdelsharedi**: Storage account - General purpose v2, Standard LRS, Soft delete for file shares DISABLED
    - **fileprmsdelshareen**: Storage account - File storage, Premium LRS, Soft delete for file shares ENABLED
    - **fileprmsdelsharedi**: Storage account - File storage, Premium LRS, Soft delete for file shares DISABLED

## Expected result

### Should include

- Soft delete for blobs DISABLED
    - **gpv2stdsdelblobdi**: Storage account - General purpose v2, Standard LRS, Soft delete for blobs DISABLED
    - **bblobprmsdelblobdi**: Storage account - Block blob storage, Premium LRS, Soft delete for blobs DISABLED

- Soft delete for containers DISABLED
    - **gpv2stdsdelcondi**: Storage account - General purpose v2, Standard LRS, Soft delete for containers DISABLED
    - **bblobprmsdelcondi**: Storage account - Block blob storage, Premium LRS, Soft delete for containers DISABLED

- Soft delete for file shares DISABLED
    - **gpv2stdsdelsharedi**: Storage account - General purpose v2, Standard LRS, Soft delete for file shares DISABLED
    - **fileprmsdelsharedi**: Storage account - File storage, Premium LRS, Soft delete for file shares DISABLED

### Should not be included

- Soft delete for blobs ENABLED
    - **gpv2stdsdelbloben**: Storage account - General purpose v2, Standard LRS, Soft delete for blobs ENABLED
    - **bblobprmsdelbloben**: Storage account - Block blob storage, Premium LRS, Soft delete for blobs ENABLED

- Soft delete for containers ENABLED
    - **gpv2stdsdelconen**: Storage account - General purpose v2, Standard LRS, Soft delete for containers ENABLED
    - **bblobprmsdelconen**: Storage account - Block blob storage, Premium LRS, Soft delete for containers ENABLED

- Soft delete for file shares ENABLED
    - **gpv2stdsdelshareen**: Storage account - General purpose v2, Standard LRS, Soft delete for file shares ENABLED
    - **fileprmsdelshareen**: Storage account - File storage, Premium LRS, Soft delete for file shares ENABLED
