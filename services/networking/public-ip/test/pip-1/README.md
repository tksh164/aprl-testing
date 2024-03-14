# Testing for APRL PIP-1

[APRL PIP-1](https://azure.github.io/Azure-Proactive-Resiliency-Library/services/networking/public-ip/#pip-1---use-standard-sku)

## Deploy

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#view/Microsoft_Azure_CreateUIDef/CustomDeploymentBlade/uri/https%3A%2F%2Fraw.githubusercontent.com%2Ftksh164%2Faprl-testing%2Fmain%2Fservices%2Fnetworking%2Fpublic-ip%2Ftest%2Fpip-1%2Ftemplate.json)

## Targets

| Name | Resource Type | SKU | Tier | IP version | Allocation method | Zone |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| basic-ipv4-dynamic | Public IP address | Basic | Regional | IPv4 | Dynamic | n/a (No Zone) |
| basic-ipv4-static | Public IP address | Basic | Regional | IPv4 | Static | n/a (No Zone) |
| basic-ipv6-dynamic | Public IP address | Basic | Regional | IPv6 | Dynamic | n/a (No Zone) |
| | | | | | | | | | |
| standard-regional-ipv4-static-nozone | Public IP address | Standard | Regional | IPv4 | Static | No Zone |
| standard-regional-ipv4-static-zonal | Public IP address | Standard | Regional | IPv4 | Static | Zonal |
| standard-regional-ipv4-static-zoneredundant | Public IP address | Standard | Regional | IPv4 | Static | Zone-redundant (Zone 1, 2, 3) |
| standard-regional-ipv6-static-nozone | Public IP address | Standard | Regional | IPv6 | Static | No Zone |
| standard-regional-ipv6-static-zonal | Public IP address | Standard | Regional | IPv6 | Static | Zonal |
| standard-regional-ipv6-static-zoneredundant | Public IP address | Standard | Regional | IPv6 | Static | Zone-redundant (Zone 1, 2, 3) |
| | | | | | | | | | |
| standard-global-ipv4-static | Public IP address | Standard | Global  | IPv4 | Static | n/a |
| standard-global-ipv6-static | Public IP address | Standard | Global | IPv6 | Static | n/a |

## Expected result

### Should include

| Name | Resource Type | SKU | Tier | IP version | Allocation method | Zone |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| basic-ipv4-dynamic | Public IP address | Basic | Regional | IPv4 | Dynamic | n/a (No Zone) |
| basic-ipv4-static | Public IP address | Basic | Regional | IPv4 | Static | n/a (No Zone) |
| basic-ipv6-dynamic | Public IP address | Basic | Regional | IPv6 | Dynamic | n/a (No Zone) |
| | | | | | | | | | |
| standard-regional-ipv4-static-nozone | Public IP address | Standard | Regional | IPv4 | Static | No Zone |
| standard-regional-ipv4-static-zonal | Public IP address | Standard | Regional | IPv4 | Static | Zonal |
| standard-regional-ipv6-static-nozone | Public IP address | Standard | Regional | IPv6 | Static | No Zone |
| standard-regional-ipv6-static-zonal | Public IP address | Standard | Regional | IPv6 | Static | Zonal |

### Should not be included

| Name | Resource Type | SKU | Tier | IP version | Allocation method | Zone |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| standard-regional-ipv4-static-zoneredundant | Public IP address | Standard | Regional | IPv4 | Static | Zone-redundant (Zone 1, 2, 3) |
| standard-regional-ipv6-static-zoneredundant | Public IP address | Standard | Regional | IPv6 | Static | Zone-redundant (Zone 1, 2, 3) |
| | | | | | | | | | |
| standard-global-ipv4-static | Public IP address | Standard | Global  | IPv4 | Static | n/a |
| standard-global-ipv6-static | Public IP address | Standard | Global | IPv6 | Static | n/a |
