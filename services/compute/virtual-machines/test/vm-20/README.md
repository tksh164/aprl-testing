# Testing for APRL VM-20

[APRL VM-20](https://azure.github.io/Azure-Proactive-Resiliency-Library/services/compute/virtual-machines/#vm-20---enable-vm-insights)

## Deploy

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#view/Microsoft_Azure_CreateUIDef/CustomDeploymentBlade/uri/https%3A%2F%2Fraw.githubusercontent.com%2Ftksh164%2Faprl-testing%2Fmain%2Fservices%2Fcompute%2Fvirtual-machines%2Ftest%2Fvm-20%2Ftemplate.json)

## Targets

| # | Resource Type | OS | VM Insights | Installed Agents | DCR |
| ---- | ---- | ---- | ---- | ---- | ---- |
| 1 | Virtual machine | Windows | Enabled (Performance & Service Map) | Azure Monitor agent<br/>Dependency agent | Yes  |
| 2 | Virtual machine | Windows | Enabled (Performance only) | Azure Monitor agent | Yes |
| 3 | Virtual machine | Windows | Disabled | Azure Monitor agent | Yes |
| | | | | | |
| 4 | Virtual machine | Windows | Enabled | Microsoft Monitoring agent<br/>Dependency agent | n/a  |
| 5 | Virtual machine | Windows | Disabled | Microsoft Monitoring agent | n/a |
| | | | | | |
| 6 | Virtual machine | Windows | Disabled | None | n/a |

## Expected result

### Should include

VM Insights is disabled (not enabled).

| # | Resource Type | OS | VM Insights | Installed Agents | DCR |
| ---- | ---- | ---- | ---- | ---- | ---- |
| 3 | Virtual machine | Windows | Disabled | Azure Monitor agent | Yes |
| 5 | Virtual machine | Windows | Disabled | Microsoft Monitoring agent | n/a |
| 6 | Virtual machine | Windows | Disabled | None | n/a |

### Should not be included

VM Insights is enabled.

| # | Resource Type | OS | VM Insights | Installed Agents | DCR |
| ---- | ---- | ---- | ---- | ---- | ---- |
| 1 | Virtual machine | Windows | Enabled (Performance & Service Map) | Azure Monitor agent<br/>Dependency agent | Yes  |
| 2 | Virtual machine | Windows | Enabled (Performance only) | Azure Monitor agent | Yes |
| 4 | Virtual machine | Windows | Enabled | Microsoft Monitoring agent<br/>Dependency agent | n/a  |

## TODO

- Add Linux machines
