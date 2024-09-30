---
title: Setting Up an Azure Web Application Environment
---
This document explains the process of setting up an Azure web application environment. The process involves creating the Azure web application, adding SQL databases, and setting up a virtual machine environment if needed.

The flow starts by checking if the configuration specifies an Azure website. If it does, the system creates the website and the necessary SQL databases. If not, it proceeds to create a virtual machine environment. This involves validating the configuration, determining the appropriate storage account, and creating the virtual machine with the specified settings. If a virtual machine with the same name already exists, it uses the existing one.

# Flow drill down

```mermaid
graph TD;
      34bdad5288d3f560524b7055aea2caf891f55d68a9b1a5851ab828350e8a7ec1(New-AzureWebApplicationEnvironment):::mainFlowStyle --> a8886c76288625415faa4600ae554f89da3dbf0b29a2fb1b60a6ef21e5a7b00b(Add-AzureSQLDatabases)

34bdad5288d3f560524b7055aea2caf891f55d68a9b1a5851ab828350e8a7ec1(New-AzureWebApplicationEnvironment):::mainFlowStyle --> 2916dd89fbde49cea47c60f57c262090786f7412b09b77728b45500f860755b4(New-AzureVMEnvironment):::mainFlowStyle

2916dd89fbde49cea47c60f57c262090786f7412b09b77728b45500f860755b4(New-AzureVMEnvironment):::mainFlowStyle --> dbca9083a9047e96732b0b4d2c705ea115393be67e6b23ab7e55bbfc1b164ffa(Add-AzureVM):::mainFlowStyle


      classDef mainFlowStyle color:#000000,fill:#7CB9F4
classDef rootsStyle color:#000000,fill:#00FFF4
classDef Style1 color:#000000,fill:#00FFAA
classDef Style2 color:#000000,fill:#FFFF00
classDef Style3 color:#000000,fill:#AA7CB9
```

<SwmSnippet path="/PublishScripts/Publish-WebApplication.ps1" line="162">

---

## Creating the Azure Web Application Environment

The <SwmToken path="PublishScripts/Publish-WebApplication.ps1" pos="162:2:4" line-data="function New-AzureWebApplicationEnvironment">`New-AzureWebApplicationEnvironment`</SwmToken> function is responsible for setting up the Azure web application environment. It first checks if the configuration specifies an Azure website. If so, it creates the website and associated SQL databases. If not, it proceeds to create a virtual machine environment.

```powershell
function New-AzureWebApplicationEnvironment
{
    [CmdletBinding()]
    param
    (
        [Parameter(Mandatory = $true)]
        [Object]
        $Config,

        [Parameter (Mandatory = $false)]
        [AllowNull()]
        [Hashtable]
        $VMPassword,

        [Parameter (Mandatory = $false)]
        [AllowNull()]
        [Hashtable[]]
        $DatabaseServerPassword
    )
   
    $VMInfo = $null
```

---

</SwmSnippet>

<SwmSnippet path="/PublishScripts/AzureWebAppPublishModule.psm1" line="1882">

---

## Adding Azure SQL Databases

The <SwmToken path="PublishScripts/AzureWebAppPublishModule.psm1" pos="1882:2:4" line-data="function Add-AzureSQLDatabases">`Add-AzureSQLDatabases`</SwmToken> function creates SQL databases based on the provided configuration. It ensures that each database is created with the correct settings and retrieves the connection string for each database, which is then used for deployment.

```powershell
function Add-AzureSQLDatabases
{
    [CmdletBinding()]
    param
    (
        [Parameter(Mandatory = $true, ValueFromPipeline = $true)]
        [PSCustomObject]
        $DatabaseConfig,

        [Parameter(Mandatory = $false)]
        [AllowNull()]
        [Hashtable[]]
        $DatabaseServerPassword,

        [Parameter(Mandatory = $false)]
        [Switch]
        $CreateDatabase = $true
    )

    begin
    {
```

---

</SwmSnippet>

<SwmSnippet path="/PublishScripts/AzureWebAppPublishModule.psm1" line="1206">

---

## Creating the Azure VM Environment

The <SwmToken path="PublishScripts/AzureWebAppPublishModule.psm1" pos="1206:2:4" line-data="function New-AzureVMEnvironment">`New-AzureVMEnvironment`</SwmToken> function sets up a new virtual machine environment. It validates the configuration, determines the appropriate storage account, and creates the virtual machine with the specified settings. If a virtual machine with the same name already exists, it uses the existing one.

```powershell
function New-AzureVMEnvironment
{
    [CmdletBinding()]
    param
    (
        [Parameter(Mandatory = $true)]
        [Object]
        $CloudServiceConfiguration,

        [Parameter(Mandatory = $false)]
        [AllowNull()]
        [Hashtable]
        $VMPassword
    )

    Write-VerboseWithTime ('New-AzureVMEnvironment: Start')

    if ($CloudServiceConfiguration.location -and $CloudServiceConfiguration.affinityGroup)
    {
        throw 'New-AzureVMEnvironment: Malformed configuration file. Has both location and affinityGroup'
    }
```

---

</SwmSnippet>

<SwmSnippet path="/PublishScripts/AzureWebAppPublishModule.psm1" line="909">

---

## Adding Azure Virtual Machines

The <SwmToken path="PublishScripts/AzureWebAppPublishModule.psm1" pos="909:2:4" line-data="function Add-AzureVM">`Add-AzureVM`</SwmToken> function creates a new Azure virtual machine with the specified configuration. It sets up the VM configuration, including the size, image, and endpoints, and optionally adds the <SwmToken path="PublishScripts/Publish-WebApplication.ps1" pos="34:4:4" line-data="View the WebDeploy license terms:  http://go.microsoft.com/fwlink/?LinkID=389744 ">`WebDeploy`</SwmToken> extension. The function then creates the VM and returns its URL.

```powershell
function Add-AzureVM
{
    [CmdletBinding()]
    param
    (
        [Parameter(Mandatory = $true)]
        [String]
        $UserName,

        [Parameter(Mandatory = $true)]
        [String]
        $UserPassword,

        [Parameter(Mandatory = $true)]
        [String]
        $VMName,

        [Parameter(Mandatory = $true)]
        [String]
        $VMSize,

```

---

</SwmSnippet>

&nbsp;

*This is an auto-generated document by Swimm AI 🌊 and has not yet been verified by a human*

<SwmMeta version="3.0.0" repo-id="Z2l0aHViJTNBJTNBV2hvT3dlc1doYXQtTmV0NDglM0ElM0FTd2ltbS1EZW1v" repo-name="WhoOwesWhat-Net48"><sup>Powered by [Swimm](/)</sup></SwmMeta>
